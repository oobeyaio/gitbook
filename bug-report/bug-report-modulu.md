---
description: >-
  Takımlarınızın yazılım geliştirme sürecinde oluşan hata kayıtlarını takip
  etmenizi sağlar.
hidden: true
icon: bug
---

# Bug Report Modülü

Oobeya Bug Report modülü, Jira ve Azure Boards gibi proje yönetimi araçları üzerinden toplanan verilerle çalışarak takımlarınızın yazılım geliştirme sürecinde oluşan hata kayıtlarını takip etmenizi sağlar. Organizasyon düzeyinde açık ve kapalı bug'lara dair detaylı bir görünürlük sunar. Bu sayede yazılım kalitesini artırmaya yönelik veriye dayalı kararlar alabilir, darboğazları erken aşamada tespit edebilirsiniz.

### Genel Özellikler

* Tüm organizasyon için merkezi bir rapor görünümü&#x20;
* Takım bazlı filtreleme ve analiz
* Zaman aralıklarına göre görünüm (günlük, haftalık, aylık, çeyreklik)
* Açık bug trendlerini görselleştirme
* Önem Derecesi (Severity) dağılımı
* Takım bazlı bug dağılımı
* Detaylı bug listesi (Work item, Assignee, Project, Status, vb.)

***

### Ön Gereksinimler (Admin Ayarları)

Bug Report modülünün doğru çalışabilmesi için **Admin Paneli** üzerinden bazı temel konfigürasyonlar yapılmalıdır.

#### 1. Category Mapping Settings

`Administration > AgileSpace` altında, **Bug Fixing** kategorisine karşılık gelen iş tipleri (örn. Bug, Defect, Problem, Incident, Error) belirlenmelidir.

{% hint style="warning" %}
Bu tanımlama yapılmadığı takdirde, ilgili iş tipleri bug olarak sınıflandırılamaz ve rapora yansımaz.
{% endhint %}

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption><p>Category Mapping</p></figcaption></figure>

#### 2. Severity Mapping

Bug'ların önem derecelerini belirlemek için Jira ve Azure Boards sisteminizdeki severity alanlarını Oobeya'nın sınıfları ile eşleştirin.

* **Jira için**: `Priority` alanından `Highest`, `High`, `Medium`, `Low`, vb.
* **Azure için**: Sayısal olarak sıralanmış severity seviyeleri ile (1 - Critical, 2 - High, vb.)

Değişiklikler yapıldığında geçmiş veriler yeniden analiz edilir.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption><p>Severity Mapping</p></figcaption></figure>

***

### Dashboard Bileşenleri

#### 1. Open Bugs Over Time

Zaman içinde açık kalan bug'ların seviyelerine göre (_Blocker, Critical, High, Medium, Low_) trendini gösterir.

* **İnteraktif grafik**: Üzerine gelindiğinde her haftalık/aylık dilimdeki bug sayıları önem derecesine göre detaylı görüntülenir.
* **Zaman filtresi**: Son 7 gün, Son 30 gün, Aylık, Çeyreklik seçimi, özel tarih aralığı gibi esnek zaman filtreleri.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>Open Bugs Over Time</p></figcaption></figure>

***

#### 2. Bug Severity Summary

Bug'ların önem derecelerine göre dağılımını gösterir.

<figure><img src="../.gitbook/assets/image (18).png" alt="" width="375"><figcaption><p>Bug Severity</p></figcaption></figure>

***

#### 3. Bug Distribution by Team

Hangi takımda kaç bug olduğu ve hangi takımların daha fazla bug açtığı analiz edilir.

* Pie chart görünümü
* Yüksek sayıda bug barındıran takımların kolayca tespiti

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption><p>Bug Distribution By Team</p></figcaption></figure>

***

#### 4. Bug Details

Tüm bug'ların detaylarını içerir:

* Work item ID
* Özet
* Atanan kişi (Assignee)
* Proje ve takım
* Tip, Severity, Durum, Tarihler

<figure><img src="../.gitbook/assets/Screenshot 2025-09-05 at 17.33.18.png" alt=""><figcaption><p>Bug Details Table</p></figcaption></figure>

***

### SSS (Sıkça Sorulan Sorular)

<details>

<summary>Bu modül tüm kullanıcılar tarafından kullanılabilir mi?</summary>

Evet, Bug Report Dashboard organizasyon seviyesinde açılır. Ancak kullanıcılar sadece kendi takımlarını filtreleyerek analiz yapabilir.

</details>

<details>

<summary>Severity seviyeleri neden doğru görünmüyor?</summary>

Admin Panel'deki severity mapping ayarlarını kontrol edin. Jira ya da Azure Boards’taki alanlar doğru eşlenmemiş olabilir.

</details>

<details>

<summary>Bug sayısı ile Jira/Azure’daki sayı farklı. Neden?</summary>

Kategori eşlemesi ya da iş tipi hariç tutulması nedeniyle bazı bug'lar dashboard'a dahil edilmemiş olabilir.

</details>

***

### Sonuç

Bug Report modülü, hata yönetimini kolaylaştırmak ve yazılım kalitesini iyileştirmek isteyen takımlar için güçlü bir analiz aracıdır. Doğru yapılandırmalarla birlikte kullanıldığında, hata yoğunlukları, çözüm süreleri ve riskli bölgeler kolayca görselleştirilebilir.
