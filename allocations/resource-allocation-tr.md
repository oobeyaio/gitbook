---
hidden: true
icon: chart-pie-simple-circle-dollar
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Resource Allocation (Kaynak Tahsisi)

Oobeya’nın **Resource Allocation** modülü, takımların iş yüklerini ve proje dağılımlarını analiz ederek daha verimli bir kaynak yönetimi sağlar. Takımların kapasiteleri, görev yükleri ve proje öncelikleri doğrultusunda dengeli şekilde çalışmasını destekler.

Bu modül, yöneticilerin&#x20;

* Takım kapasitelerini görselleştirmesine,&#x20;
* **Aşırı** **veya** **yetersiz** **yüklenen** takımları ve takım üyelerini tespit etmesine,
* **Kaynak planlamasını daha sağlıklı yapmasına** yardımcı olur.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-31 at 14.25.10.png" alt=""><figcaption><p>Resource Allocations Module</p></figcaption></figure>

***

### Önkoşullar

Resource Allocation modülünü kullanmadan önce aşağıdaki şartların sağlandığından emin olun:

* [x] **Proje yönetim aracı entegrasyonu aktif durumda olmalı:**\
  Bu modül, Jira veya Azure Boards gibi proje yönetim araçlarına bağlanarak verileri Oobeya'nın AgileSpace modülü üzerinden çeker.&#x20;
* [x] **Projeler AgileSpace üzerinde analiz edilmiş olmalı:**\
  Jira veya Azure Boards projelerinizin AgileSpace modülünde aktif olarak analiz edildiğinden emin olun.
* [x] **Contributors profilleri oluşturulmuş olmalı:**\
  Proje teslimat sürecine dahil olan her kullanıcının Oobeya'da bir katkıcı (contributor) profili olmalıdır.
* [x] **Hesaplar birleştirilmiş (gerekiyorsa) olmalı:**\
  Jira/Azure Boards üzerindeki mükerrer kullanıcı hesapları birleştirilmelidir. Aksi halde hesaplamalarda eksiklikler oluşabilir.
* [x] **Kapsama dahil edilmiş roller seçilmiş olmalı:**\
  Sadece belirli roller (örn. Developer) hesaplamalara dahil edilir. Rolleri `Administration > Resource Allocations` menüsünden yönetebilirsiniz. Detaylar [aşağıda](resource-allocation-tr.md#admin-ayarlari) açıklanmıştır.
* [x] **Gereksiz iş öğesi tipleri hariç tutulmuş olmalı:**\
  Analizin doğruluğunu artırmak için gereksiz iş öğesi tiplerini (örn. soru, yorum) analiz kapsamından hariç turtmak amacıyla `Administration > AgileSpace > Work Item Type Exclusion` bölümünden filtreleme yapabilirsiniz.

***

### Temel Kavramlar

* **Kaynak (Resource)**: Geliştirme süreçlerinde görev alan kişi (örn. yazılım geliştirici, QA, analist).
* **Proje (Project)**: Üzerinde çalışılan işin veya ürünün tanımıdır. Jira ve Azure Boards entegrasyonu ile çalışmaktadır.
* **Dağılım (Tahsis) Oranı (Project Allocation %)**: Bir kaynağın (kişinin) belirli bir projeye tahsis edilmiş efor veya görev (work item) oranını ifade eder.
* **Kaynak Kullanım Oranı (Resource Utilization %)**: Kaynağın tahsis edildiği işin ne kadarını teslim edebildiğini gösterir.

***

### Nasıl Çalışır?

**Genel Bakış (Overview)**

Modül, kurum genelinde veya belirli bir organizasyon birimi için özet bilgiler sunar:

* **Toplam Proje Sayısı** (Total Projects)
* **Toplam Kaynak Sayısı** (Total Resources)
* **Effort Bazlı Kullanım (%)** (Utilization by Effort)
* **İş Sayısına Göre Kullanım (%)** (Utilization by Count)
* **Kaynak Durumu Dağılımı** (Resource Status chart)

Her iki kullanım metriği de **iş yükü dengesizliğini** veya **düşük verimliliği** görsel olarak ortaya koyar.

***

### **1. Kaynak Kullanım Oranı (Utilization %) Hesaplaması**

Kaynak kullanım oranı, bir takımın ve takım üyelerinin planlanan iş yükünün mevcut teslimat kapasitesine göre ne kadar dolu olduğunu gösterir. Şu durumları analiz etmenizi sağlar:

* Takım ve takım üyeleri **az yüklü** mü?
* Takım ve takım üyeleri **ideal seviyede** mi çalışıyor?
* Takım ve takım üyeleri **aşırı mı yüklenmiş?**

#### Formül:

```
Kullanım Oranı (%) = (Planlanan İş Sayısı / Takım Ortalama Kapasitesi) × 100
```

**Takım Ortalama Kapasitesi** ise şu şekilde hesaplanır:

```
Takım Ortalama Kapasitesi = Teslim Edilen İş Sayısı / Katılımcı Sayısı
```

#### Örnek:

* Takım tarafından toplam teslim edilen (delivered) iş miktarı: 100
* Takım üyesi sayısı: 5
* Bir kaynak (örn. Dev-A) için planlanan iş miktarı: 25

→ Takım Ortalama Kapasite = 100 / 5 = 20\
→ Dev-A Kaynak Kullanım Oranı (Utilizaiton) = (25 / 20) × 100 = **%125**

#### Değerlendirme:

| Kullanım Oranı % (default değerler) | Durum                                       |
| ----------------------------------- | ------------------------------------------- |
| ≤ %85                               | Az Yüklenmiş (Underutilized)                |
| %85 – %110                          | İdeal Kullanım (Optimally Utilized)         |
| %110 – %130                         | Hafif Aşırı Yüklenmiş (Slightly Overloaded) |
| > %130                              | Aşırı Yüklenmiş (Overloaded)                |

{% hint style="info" %}
Bu varsayılar eşik değerler, `Administration > Resource Allocations` menüsünden özelleştirilebilir.
{% endhint %}

<figure><img src="../.gitbook/assets/image (473).png" alt=""><figcaption><p>Resource Status</p></figcaption></figure>

***

### 2. Proje Tahsis Oranı (Project Allocation %) **Hesaplaması**

Proje tahsis oranı, bir takım üyesinin (kaynağın) zamanının ve eforunun ne kadarının belirli bir projeye ayrıldığını gösterir.&#x20;

Özellikle birden fazla projede çalışan kişilerin izlenebilmesi için faydalıdır.

<figure><img src="../.gitbook/assets/image (472).png" alt=""><figcaption><p>Project Allocation</p></figcaption></figure>

#### Formül:

```
Proje Tahsis Oranı (%) =
(Kişinin Bu Projede Planlanan İş Sayısı / Tüm Projelerde Planlanan Toplam İş Sayısı) × 100
```

#### Örnek:

* Ayşe’nin Proje A’daki planlanan iş miktarı: 5
* Ayşe’nin tüm projelerdeki toplam planlanan iş miktarı: 10

→ Proje Dağılımı = (5 / 10) × 100 = **%50**

Bu, Ayşe’nin zamanının %50’sini Proje A’ya ayırdığı anlamına gelir.

***

### Ek Bilgiler

* Veriler AgileSpace (Oobeya’nın Agile analiz modülü) üzerinden alınır.
* Sadece seçili roller (örn. Developer) hesaplamalara dahil edilir. Bu roller `Administration > Resource Allocations` üzerinden düzenlenebilir.
* Modülde **İş Sayısı (Item Count)** ve **Effort (story points ya da süre tahmini)** arasında geçiş yapılabilir.
* Doğru analiz sonuçları için Oobeya'da kullanıcı profilleri (contributor profile) oluşturulmalı ve gerekiyor ise hesap birleştirme (account merge) işlemleri tamamlanmalıdır.

***

### Admin Ayarları

Oobeya, kaynak kullanım raporlarını esnek biçimde yapılandırabilmeniz için yöneticilere özel ayarlar sunar. Bu ayarlar sayesinde “kullanım durumlarının” nasıl kategorize edileceğini belirleyebilir ve belirli rollerin hesaplamalara dahil edilip edilmeyeceğini yönetebilirsiniz.

***

#### 1. Resource Allocation Thresholds (Eşik Değer Ayarları)

Bu eşik değerleri, kaynakların hangi oranlarda **yetersiz kullanılmış**, **optimal**, **hafif aşırı yüklenmiş** ya da **aşırı yüklenmiş** olarak sınıflandırılacağını tanımlar:

| Kategori                | Açıklama                                                                                            | Varsayılan (%) |
| ----------------------- | --------------------------------------------------------------------------------------------------- | -------------- |
| **Underutilized**       | Kaynak kullanım oranı bu değerin altında ise “yetersiz kullanılıyor” kabul edilir.                  | 85             |
| **Optimally Utilized**  | Bu değer aralığında kalan kaynaklar “optimum kullanılıyor” olarak işaretlenir.                      | 110            |
| **Slightly Overloaded** | Bu sınırın üzerindeki ancak aşırı yüklenmemiş kaynaklar “hafif aşırı yüklü” olarak sınıflandırılır. | 130            |
| **Overloaded**          | %130’dan daha yüksek oranlar “aşırı yüklenmiş” olarak kabul edilir.                                 | >130           |

> Her bir eşik değerinin yanında bulunan (i) ikonları, kullanıcıya kısa açıklamalar sunmak için bilgilendirici ipuçları içerir.

* **Reset**: Varsayılan değerlere geri döner.
* **Save**: Yapılan değişiklikleri kalıcı olarak kaydeder.

***

#### 2. Allocation Roles (Rol Bazlı Hariç Tutma)

Bu ayar, hangi kullanıcı rollerinin Resource Allocation modülünde **analize dahil edileceğini** belirlemenizi sağlar.

* Örneğin: Sadece `Developer` rolü seçiliyse, yalnızca bu role sahip kullanıcıların iş yükü ve kapasite verileri değerlendirmeye alınır.
* Böylece analiz dışı bırakılması gereken roller (örneğin: QA, analist, yönetici, destek vb.) kapsam dışı kalır.

**Kullanım Senaryosu:**\
Bir proje yöneticisi, yalnızca yazılımcıların verimini ölçmek istiyorsa, `Developer` rolü dışındaki katkıları hariç tutarak daha anlamlı sonuçlar elde edebilir.

{% hint style="info" %}
Bu ayar tüm organizasyonu etkiler ve yalnızca **yönetici yetkisine sahip** kullanıcılar tarafından değiştirilebilir.
{% endhint %}
