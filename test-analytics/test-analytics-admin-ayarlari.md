---
hidden: true
---

# 2. Test Analytics – Admin Settings

**Test Analytics** modülünde, test yönetim araçları projelerinden gelen verilerin doğru şekilde analiz edilmesi için belirli alanların Oobeya standartlarıyla eşleştirilmesi gerekir.\
Bu ayarlar, şirket genelinde uygulanır ve tüm test analizlerinde geçerli olur.

{% hint style="info" %}
Yeni test analizi oluşturma adımları için bkz. [Yeni Test Analizi Oluşturma](yeni-test-analizi-olusturma.md)
{% endhint %}

***

### 1. Otomatik Yeniden Analiz (Automated Reanalysis)

Bu özellik aktif edildiğinde, Oobeya test projelerinizi belirli aralıklarla tarar ve değişiklik tespit edildiğinde otomatik yeniden analiz başlatır.\
Bu sayede test sonuçları her zaman güncel kalır.

<table><thead><tr><th width="188.60479736328125">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Enabled</strong></td><td>Otomatik yeniden analiz özelliğini aktif/pasif eder.</td></tr><tr><td><strong>Reanalysis Period</strong></td><td>Tarama sıklığını belirler (ör. 1 saat, 6 saat, 12 saat, günlük).</td></tr></tbody></table>

***

### 2. Field Mapping

Bu bölüm, test yönetim araçlarındaki alanların Oobeya’nın standart test alanlarıyla eşleştirilmesini sağlar.\
Doğru eşleştirme yapılmadığında metrikler eksik veya hatalı hesaplanabilir.

<table><thead><tr><th width="189.9361572265625">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Related Team Field</strong></td><td>Her bir test veya execution kaydının hangi takıma ait olduğunu belirten alandır. Örneğin <code>Payment BE</code> yazıyorsa, bu test Oobeya tarafında “Payment BE” takımıyla eşleştirilebilir. Bu alan sayesinde takım skor kartlarında metrikler doğru takımlara filtrelenir.</td></tr><tr><td><strong>Failure Reason Field</strong> (özelleştirme gerektirir)</td><td>Proje yönetim araçlarındaki (Jira, Azure Boards) Bug tipi workitem’larda hatanın kaynağını belirlemek için kullanılan dropdown alanıdır (custom bir alan da olabilir). Oobeya bu alanı kullanarak hata nedenlerini kategorize eder ve gruplar. Örneğin: <em>Geliştirme Hatası</em>, <em>Entegrasyon Hatası</em>, <em>Veri Kaynağı Problemi</em> gibi.</td></tr><tr><td><strong>Related Test Field</strong></td><td>Bir bug workitem’ın hangi test senaryosu ile ilişkili olduğunu belirleyen alandır. Bazı durumlarda bu ilişki doğrudan linked issue’lar üzerinden veya Xray Run kayıtlarından da tespit edilir.</td></tr><tr><td><strong>Related Test Execution Field</strong></td><td>Bir bug workitem’ın hangi test execution (koşum) ile ilişkili olduğunu belirtir. “Related Test Field” ile birlikte, hatanın hangi test akışından geldiğini netleştirmek için kullanılır.</td></tr><tr><td><strong>UAT Defect Field</strong> (özelleştirme gerektirir)</td><td>Upper project içindeki workitem’larda bulunan, “Bu test UAT’ten geri döndü mü?” bilgisini tutan custom field’dır. Eğer bu alanda “Evet” seçilmişse, execution’a bağlı workitem UAT aşamasından geri dönmüş sayılır ve Oobeya bu bilgiyi UAT Defect olarak yakalar.</td></tr><tr><td><strong>Problem No Field</strong> (özelleştirme gerektirir)</td><td>Dış sistemlerden “Leakage Defects” endpoint’i aracılığıyla gönderilen hataların test yönetim aracı (XRay) tarafındaki karşılığıdır. Upper project’te bulunan <code>Problem No</code> alanı ilişkilendirilir. API üzerinden gelen kayıtlar <code>problemNo</code> parametresine göre eşleştirilerek ilgili workitem’a bağlanır.</td></tr></tbody></table>

{% hint style="warning" %}
Alan eşleştirmeleri değiştirildiğinde, tüm mevcut analizler yeni konfigürasyonla yeniden işlenir.
{% endhint %}

***

### 3. Metric Thresholds

Test performans göstergeleri için global eşik değerleri tanımlayın.\
Bu eşik değerler, takımların durumlarını **Team Scorecard** ve **Organization Overview** ekranlarında belirlemek için kullanılır.

<table><thead><tr><th width="252.6505126953125">Metrik</th><th width="363.598876953125">Açıklama</th><th align="center">Varsayılan</th></tr></thead><tbody><tr><td><strong>Test Efficiency (%)</strong></td><td>Başarılı testlerin toplam testlere oranı.</td><td align="center">75</td></tr><tr><td><strong>Escaped Defects (%)</strong></td><td>Canlı ortamda kaçan hataların oranı.</td><td align="center">40</td></tr><tr><td><strong>Automation Coverage (%)</strong></td><td>Otomasyona alınmış testlerin oranı.</td><td align="center">0</td></tr><tr><td><strong>Automation Success (%)</strong></td><td>Otomasyon testlerinin başarı oranı.</td><td align="center">0</td></tr><tr><td><strong>Automated Execution Time (ms)</strong></td><td>Otomasyon testlerinin ortalama süresi.</td><td align="center">0</td></tr><tr><td><strong>Execution Threshold (%)</strong></td><td>Test yürütme sıklığı veya tamamlanma oranı.</td><td align="center">0</td></tr></tbody></table>

{% hint style="info" %}
Bu değerler, tüm organizasyon genelinde referans alınır ve takım performansını karşılaştırmada kullanılır.
{% endhint %}

***

### 4. Type Selection for UAT Defects

Bu ayar, test sürecinde tespit edilen **UAT hatalarını (bugs)** doğru şekilde filtrelemek için kullanılır.

<table><thead><tr><th width="228.096923828125">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>UAT Defect Work Types</strong></td><td>Proje yönetimi araçlarında (Jira, Azure DevOps) hata takibi için kullanılacak iş tiplerini belirler (ör. Story, Task, Bug, Defect).</td></tr></tbody></table>

<figure><img src="https://docs.oobeya.io/assets/test-analytics-uat-defects.png" alt=""><figcaption><p>UAT Defect Tip Seçimi</p></figcaption></figure>

{% hint style="info" %}
Bu eşleştirme, Test Analytics Dashboard üzerindeki “Defect Rate” metriğinin doğru hesaplanması için gereklidir.
{% endhint %}

***

### Önerilen Konfigürasyon Akışı

1. Test yönetim aracı (XRay vb.) için veri kaynağı (data source) ekleyin.
2. Admin panelde Field Mapping tanımlarını yapın.
3. Admin panelde Metric Threshold değerlerini belirleyin.
4. Yeni bir analiz oluşturun → [Yeni Test Analizi Oluşturma](yeni-test-analizi-olusturma.md)
5. Takım eşleştirmesini tamamlayın → Team Mapping
