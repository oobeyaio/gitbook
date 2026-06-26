---
hidden: true
---

# Code Quality Index (TCQI & PCQI) \[TR]

### **Genel Bakış**

Oobeya’daki **Code Quality Index** metrikleri, yazılım projelerinizin ve ekiplerinizin kod kalitesini **0–5 arası tek bir skorla** ifade eder.\
Bu metrikler, **SonarQube** verilerini kullanır ve **ISO/IEC 25010** yazılım kalite modelinin nitelikleri ile uyumludur.

* **Project Code Quality Index (PCQI)**: Proje seviyesinde kod kalitesini ölçer.
* **Total Code Quality Index (TCQI)**: Bir ekibin tüm projelerinin kod kalitesini ağırlıklı ortalama ile hesaplar.

Bu sayede hem **tek bir projeye** hem de **tüm ekibe** ait kod kalitesi trendlerini kolayca izleyebilirsiniz.

***

### **Hangi Veriler Kullanılır?**

Oobeya, SonarQube entegrasyonu ile aşağıdaki verileri toplar:

1. **Security** – Güvenlik açıkları ve zafiyetlerin kod üzerindeki etkisi
2. **Reliability** – Hata/bozulma olasılığı, kurtarılabilirlik, istisnalar
3. **Maintainability** – Bakım kolaylığı, modülerlik, okunabilirlik
4. **Unit Test Coverage** – Birim test kapsam yüzdesi
5. **Duplication** – Tekrarlayan kod oranı
6. **Complexity** – Döngüsel (cyclomatic) ve bilişsel (cognitive) karmaşıklık

***

### **1. PCQI (Project Code Quality Index)**

#### **Tanım**

**PCQI**, tek bir projenin kod kalitesini yukarıdaki altı bileşen üzerinden hesaplar. Skor **0–5 aralığında** normalize edilir.

***

#### **Hesaplama Adımları**

**1. Alt Metriklerin Hesaplanması**

**Security / Reliability / Maintainability:**

* Yüksek, orta, düşük eforlu sorunlar katsayılarla çarpılır, kod satır sayısına (LOC) bölünür, kalite ölçeği hesaplanır, rating’in tavan puanı ile çarpılır, minimum puan ile karşılaştırılır. Çıkan sonuç ilgili metrik skorudur.
* Rating (A–E) değerine göre **tavan puan (CeilingScore)** ve **taban puan (MinScore)** uygulanır.
  * **CeilingScore**: A=5, B=4, C=3, D=2, E=1
  * **MinScore**: A=2.5, B=2.0, C=1.5, D=1.0, E=0.0

```
LineEffort = [(HighEffort * HighCoeff) + (MediumEffort * MediumCoeff) + (LowEffort * LowCoeff)] / LOC 

ScaleScore = max(0, 1 - LineEffort) 

SeverityScore = max(CeilingScore(Rating) * ScaleScore, MinScore(Rating))
```

**Unit Test Coverage:**

Unit test Coverage yüzdesi, ağırlığı ile çarpılır.

```
CoverageScore = CoverageRate * CoverageWeight
```

**Duplication:**

%25 tekrar oranı eşiği baz alınır, üzeri doğrudan sıfır (0) olarak kabul edilir.

```
DuplicationScore = max(0, (1 - (DuplicationRate / 0.25)) * DuplicationWeight)
```

**Complexity:**

Döngüsel ve bilişsel karmaşıklık değerleri fonksiyon başına normalize edilir, hedef değer **FD=20** ile karşılaştırılır. İki skorun ortalaması alınır.

* **FD (Function Default)**: 20
* **CyWeight:** 5
* **CoWeight**: 5

```
ComplexityScore = statistics.mean([
  max(0, CyWeight * (1 - ((Cyclomatic / FunctionCount) / FD))),
  max(0, CoWeight * (1 - ((Cognitive / FunctionCount) / FD)))
])
```

***

**2. Alt Metriklerin Ortalaması**

Tüm alt metrikler **0–5** aralığında normalize edilir ve aritmetik ortalama alınarak PCQI skoru elde edilir:

```
PCQI = Ortalama(SecurityScore, ReliabilityScore, MaintainabilityScore, CoverageScore, DuplicationScore, ComplexityScore)
```

***

#### **PCQI Skor Yorumlama**

<table><thead><tr><th width="158.79229736328125">PCQI Skoru</th><th width="154.36083984375">Durum</th><th>Önerilen Aksiyon</th></tr></thead><tbody><tr><td>4.5 – 5.0</td><td>Mükemmel</td><td>Süreçleri koruyun ve iyi uygulamaları yaygınlaştırın.</td></tr><tr><td>3.5 – 4.4</td><td>İyi</td><td>Belirli alanlarda iyileştirme fırsatlarını değerlendirin.</td></tr><tr><td>2.5 – 3.4</td><td>Orta</td><td>Hedefli iyileştirmeler yapın.</td></tr><tr><td>0 – 2.4</td><td>Kritik</td><td>Güvenlik, bakım kolaylığı, test kapsamı alanlarında acil aksiyon alın.</td></tr></tbody></table>

***

### **2. TCQI (Team Code Quality Index)**

#### **Tanım**

**TCQI**, bir ekibin tüm projelerinin PCQI skorlarının, proje büyüklükleri (LOC) ile ağırlıklandırılmış ortalamasıdır. Bu sayede küçük ve büyük projeler adil şekilde karşılaştırılır.

***

#### **Hesaplama Adımları**

1. Her proje için **PCQI** hesaplanır.
2. Her proje PCQI değeri, proje LOC değeri ile çarpılır.
3. Elde edilen değerler toplanır ve ekibin toplam LOC’una bölünür:

```
TCQI = [ ∑(PCQI_project * LOC_project) ] / ∑(LOC_team)
```

***

**Örnek Hesaplama**

<table><thead><tr><th width="165.05755615234375">Proje</th><th width="109.272705078125">PCQI</th><th width="175.86090087890625">LOC</th><th>Ağırlıklı Değer</th></tr></thead><tbody><tr><td>A</td><td>4.0</td><td>100,000</td><td>400,000</td></tr><tr><td>B</td><td>3.0</td><td>50,000</td><td>150,000</td></tr><tr><td><strong>Toplam</strong></td><td></td><td>150,000</td><td><strong>TCQI = 3,67</strong></td></tr></tbody></table>

***

#### **TCQI Skor Yorumlama**

<table><thead><tr><th width="156.457763671875">TCQI Skoru</th><th width="185.997314453125">Durum</th><th>Önerilen Aksiyon</th></tr></thead><tbody><tr><td>4.5 – 5.0</td><td>Mükemmel</td><td>Takım genelinde kalite çok yüksek, mevcut süreçleri koruyun.</td></tr><tr><td>3.5 – 4.4</td><td>İyi</td><td>Belirli projelerde küçük iyileştirmeler planlayın.</td></tr><tr><td>2.5 – 3.4</td><td>Orta</td><td>Düşük skorlu projelere odaklanın.</td></tr><tr><td>0 – 2.4</td><td>Kritik</td><td>Ekip genelinde kalite sorunları var, acil aksiyon alın.</td></tr></tbody></table>

***

### **İyileştirme Önerileri**

* **Security / Reliability / Maintainability**: Kritik ve büyük sorunları çözün, kod inceleme süreçlerini güçlendirin.
* **Coverage**: Test kapsamını artırın (%80+ hedeflenmeli).
* **Duplication**: Kod tekrarını %25’in altına indirin.
* **Complexity**: Fonksiyon başına karmaşıklığı 20’nin altında tutun.

***



