---
description: >-
  Dış sistemlerden API aracılığıyla toplanan test sonuçlarını işleyerek, başarı
  oranı, kapsam ve kaçan hatalar (defects) gibi metrikleri hesaplar.
hidden: true
---

# Test Otomasyon Metrikleri ve API Dokümanı

**Automation Tests** bölümü, otomatik test süreçlerinden gelen verilerin analiz edilmesini sağlar.\
Dış sistemlerden API aracılığıyla toplanan test sonuçlarını işleyerek, başarı oranı, kapsam ve kaçan hatalar (defects) gibi metrikleri hesaplar.

{% hint style="info" %}
🔗 Manual testler (Xray) için bkz. [Yeni Test Analizi Oluşturma](yeni-test-analizi-olusturma.md)\
🔗 Global ayarlar için bkz. [Test Analytics – Admin Settings](test-analytics-admin-ayarlari.md)
{% endhint %}

<figure><img src="../.gitbook/assets/image (490).png" alt=""><figcaption><p>Test Automation Dashboard</p></figcaption></figure>

***

### 1. Veri Toplama Yapısı

Otomasyon test sonuçları Oobeya’ya REST API aracılığıyla aktarılır.\
Veriler, dört ana uç (endpoint) üzerinden gönderilir:

<table><thead><tr><th width="301.85211181640625">API</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>/apis/v1/test/external/execution</strong></td><td>Test senaryolarının çalıştırma (execution) bilgilerini gönderir.</td></tr><tr><td><strong>/apis/v1/test/external/defect</strong></td><td>Kaçan (escaped) defect kayıtlarını gönderir.</td></tr><tr><td><strong>/apis/v1/test/external/coverage</strong></td><td>Test coverage (kapsam) verilerini gönderir.</td></tr><tr><td><strong>/apis/v1/test/external/bug</strong></td><td>Test kaynaklı bug kayıtlarını gönderir.</td></tr></tbody></table>

***

### 2. Veri Alanları

#### **Execution Endpoint**

Test koşumlarının (executions) temel bilgilerini içerir.

<table><thead><tr><th width="269.88787841796875">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>scenarioId</code></td><td>Test senaryosunun benzersiz kimliği.</td></tr><tr><td><code>applicationId</code></td><td>Testin ait olduğu uygulama veya modül.</td></tr><tr><td><code>startTime</code>, <code>endTime</code></td><td>Çalıştırma zaman aralığı.</td></tr><tr><td><code>status</code></td><td>PASS / FAIL / SKIPPED durumu.</td></tr><tr><td><code>durationMs</code></td><td>Çalışma süresi (ms).</td></tr><tr><td><code>environment</code>, <code>triggeredBy</code></td><td>Ortam ve testi başlatan kullanıcı.</td></tr><tr><td><code>team</code></td><td>Testi gerçekleştiren takım.</td></tr></tbody></table>

#### **Defect Endpoint**

Test sürecinde kaçan veya sonradan tespit edilen hatalar.

<table><thead><tr><th width="269.97064208984375">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>problemNo</code></td><td>Hata kimliği.</td></tr><tr><td><code>description</code></td><td>Hatanın açıklaması.</td></tr><tr><td><code>detectedAt</code>, <code>resolvedAt</code></td><td>Tespit ve çözüm tarihleri.</td></tr></tbody></table>

#### **Coverage Endpoint**

Kodun ne kadarının otomasyon testleriyle kapsandığını belirtir.

<table><thead><tr><th width="270.311279296875">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>coverageService</code></td><td>Ölçüm yapılan repository veya pipeline.</td></tr><tr><td><code>toolType</code></td><td>Kullanılan test aracı (ör. Jacoco, Jest, NUnit).</td></tr><tr><td><code>coverageRate</code></td><td>Kapsama oranı (%).</td></tr><tr><td><code>totalLines</code>, <code>coveredLines</code></td><td>Kod satırı sayıları.</td></tr></tbody></table>

#### **Bug Endpoint**

Testlerle ilişkili bug kayıtlarını içerir.

<table><thead><tr><th width="188.9273681640625">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>bugId</code></td><td>Hatanın kimliği.</td></tr><tr><td><code>project</code></td><td>Bağlı proje.</td></tr><tr><td><code>assignedTo</code></td><td>Hatanın sorumlusu.</td></tr><tr><td><code>status</code></td><td>Bug durumu (Open, In Progress, Closed).</td></tr></tbody></table>

***

### 3. Automation Dashboard

API verileri işlendiğinde **Automation Dashboard** otomatik olarak oluşur.\
Dashboard üç ana katmandan oluşur:

#### **Üst Panel (Top Widgets)**

<figure><img src="../.gitbook/assets/image (491).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="269.72113037109375">Widget</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Bug Count</strong></td><td>Toplam tespit edilen hata sayısı.</td></tr><tr><td><strong>Executed Scenarios</strong></td><td>Çalıştırılan test senaryosu sayısı.</td></tr><tr><td><strong>Success Rate (%)</strong></td><td>Başarılı testlerin oranı.</td></tr><tr><td><strong>Coverage Rate (%)</strong></td><td>Kodun testlerle kapsandığı oran.</td></tr><tr><td><strong>Execution Time (Total)</strong></td><td>Toplam test yürütme süresi.</td></tr><tr><td><strong>Defect Count</strong></td><td>Tespit edilen kaçan hata sayısı.</td></tr></tbody></table>

#### **Orta Bölüm – Execution Status**

Toplam, başarılı ve başarısız yürütme sayılarını zaman içinde gösterir.

<figure><img src="../.gitbook/assets/image (492).png" alt=""><figcaption></figcaption></figure>

#### **Alt Bölüm – Detay Sekmeleri**

<table><thead><tr><th width="270.148193359375">Sekme</th><th>İçerik</th></tr></thead><tbody><tr><td><strong>Coverage</strong></td><td>Test kapsam raporları.</td></tr><tr><td><strong>Bugs</strong></td><td>Testten kaynaklanan bug listesi.</td></tr><tr><td><strong>Scenarios</strong></td><td>Çalıştırılan test senaryolarının detayları.</td></tr><tr><td><strong>Defects</strong></td><td>Kaçan hatalar (leakage).</td></tr></tbody></table>

Tüm tablolar sağ üstten **Excel olarak dışa aktarılabilir.**

***

### 4. Hesaplanan Metrikler

Automation verileri işlendiğinde aşağıdaki metrikler otomatik olarak hesaplanır:

<table><thead><tr><th width="287.94293212890625">Metrik</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Automation Coverage (%)</strong></td><td>Otomasyona alınan kod oranı.</td></tr><tr><td><strong>Automation Success Rate (%)</strong></td><td>Geçen senaryoların toplam senaryolara oranı.</td></tr><tr><td><strong>Automation Execution Time (ms)</strong></td><td>Ortalama test yürütme süresi.</td></tr><tr><td><strong>Escaped Defects (%)</strong></td><td>Otomasyonun kaçırdığı hataların oranı.</td></tr><tr><td><strong>Test Efficiency (%)</strong></td><td>Başarılı testlerin toplam testlere oranı.</td></tr></tbody></table>

{% hint style="info" %}
Bu metriklerin renk durumu (yeşil/kırmızı), Admin Settings sayfasındaki **Metric Thresholds** değerlerine göre belirlenir.
{% endhint %}

***

### 5. Team Mapping Entegrasyonu

Test Otomasyon analizinden gelen metriklerin takımlara yansıtılması için, ilgili uygulama veya modülün **takım ile ilişkilendirilmesi** gerekmektedir.

**Menü Yolu:**\
`Insights > Teams > Scorecard > Update > Test Projects`

Burada, test otomasyon verisini içeren projeler takımla eşleştirilmelidir.\
Detaylı bilgi için bkz. [Takım Eşlemesi](takim-eslemesi.md)

{% hint style="info" %}
Metrikler yalnızca "Related Team" kolonunda gelen takım bilgileri Oobeya'daki takımlar ile eşleştirilmişse takım seviyesinde hesaplanır.
{% endhint %}

***

### 6. API Yönetimi (Opsiyonel)

#### **Veri Kontrolü**

* **GET** istekleriyle son gönderilen verileri kontrol edebilirsiniz:\
  `/execution/last/{applicationId}`\
  `/defect/last/{applicationId}`\
  `/coverage/last/{applicationId}`\
  `/bug/last/{applicationId}`

#### **Veri Silme**

Gerekirse belirli test kayıtlarını silebilirsiniz:

`DELETE /application/{applicationId}/execution/{id}/scenario/{scenarioId}`\
`DELETE /defect/application/{applicationId}/problem-no/{problemNo}`\
`DELETE /application/{applicationId}/coverage/{id}`\
`DELETE /application/{applicationId}/bug/{id}`

{% hint style="info" %}
Bu işlemler yalnızca “Organization Admin” yetkisine sahip kullanıcılar tarafından yapılmalıdır.
{% endhint %}

***

### 7. Önerilen Kullanım Akışı

1. API Endpoint'lerini Test Otomasyon entegrasyonuna tanımla.
2. Veri gönderimini doğrula → Automation Dashboard kontrol et.
3. Metrikleri gözden geçir → Gerekirse [Admin Settings](test-analytics-admin-ayarlari.md) üzerinden eşik değerlerini düzenle.
4. Takım bazlı görünüm için [Team Mapping](takim-eslemesi.md) bağlantısını tamamla.
