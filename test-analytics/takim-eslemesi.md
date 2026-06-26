---
description: >-
  Oobeya’nın Test Analytics modülünden gelen analiz sonuçlarının doğru takımlara
  aktarılmasını sağlar.
hidden: true
---

# 3. Takım Eşlemesi (Team Mapping)

**Takım Eşlemesi**, Oobeya’nın Test Analytics modülünden gelen analiz sonuçlarının doğru takımlara aktarılmasını sağlar.\
Bu sayede her takımın test verimliliği, hata oranı ve UAT başarı oranı gibi metrikleri kendi **Team Helth > Scorecard** ekranında görüntülenebilir.

{% hint style="info" %}
Önce [Yeni Test Analizi Oluşturma](yeni-test-analizi-olusturma.md) adımlarını tamamlayın. Bu analiz tamamlanmadan takım eşlemesi yapılamaz.
{% endhint %}

***

### 1. Takım Eşleme Erişim Noktası

Takım eşleştirmesi aşağıdaki yollardan yapılabilir:

* **Test Analytics > Create Test > Team Selection** adımında (analiz sırasında)\
  veya
* **Insights > Teams > Scorecard > Update** adımı üzerinden (analiz sonrası)

<figure><img src="../.gitbook/assets/image (488).png" alt=""><figcaption><p>Analiz sonrasında Takım x Test Projesi ilişkilendirme</p></figcaption></figure>

***

### 2. Test Projelerini Oobeya Takımlarıyla Eşleştirme

Bu adımda, analiz edilen test projeleri ilgili Oobeya takımlarıyla ilişkilendirilir.\
Eşleştirme tamamlandığında metrikler takım bazında hesaplanır.

<table><thead><tr><th width="227.1884765625">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Left Panel</strong></td><td>Test yönetim aracından gelen test projelerinin listesi.</td></tr><tr><td><strong>Right Panel</strong></td><td>Oobeya organizasyonundaki mevcut takımlar.</td></tr><tr><td><strong>Arrows (⇄)</strong></td><td>Seçilen projeyi ilgili takıma taşır veya kaldırır.</td></tr></tbody></table>

{% hint style="info" %}
💡 Birden fazla Xray projesi aynı takıma bağlanabilir.\
Örneğin: “Mobile Tests” ve “Web Tests” projeleri aynı “QA Team” altında birleştirilebilir.
{% endhint %}

***

### 3. Analiz Sonuçlarının Takımlara Yansıtılması

Eşleştirme tamamlandıktan sonra analiz sonuçları, otomatik olarak ilgili takımın **Scorecard** ekranına yansır.

**Team Scorecard > Test Analytics Bölümü:**



<table data-full-width="true"><thead><tr><th width="174.31787109375">Metrik</th><th>Açıklama</th><th>Hesaplama Mantığı / Formül</th></tr></thead><tbody><tr><td><strong>Test Efficiency Rate</strong></td><td>Testlerin hata yakalama başarısını ölçer.</td><td><code>(Manual Defects + Automation Defects) / (Manual Defects + Automation Defects + UAT Defects)</code></td></tr><tr><td><strong>Escaped Defects (Leakage) Rate</strong></td><td>Testlerden kaçıpta üst ortama/prod’a giden hata oranı.</td><td><code>Production Defects / (Manual + Automation + UAT + Production Defects)</code></td></tr><tr><td><strong>Automation Coverage Rate</strong></td><td>Kod tabanının ne kadarının test otomasyonu ile kapsandığını gösterir.</td><td><code>Covered Lines / Total Lines</code></td></tr><tr><td><strong>Automation Success Rate</strong></td><td>Otomasyon testlerinin başarı oranı.</td><td><code>Passed Test Runs / Total Test Runs</code></td></tr><tr><td><strong>Automation Execution Time</strong></td><td>Otomasyon testlerinin toplam çalışma süresi.</td><td><code>Sum(Execution Duration - Automation)</code></td></tr><tr><td><strong>Manual Execution Time</strong></td><td>Manuel testlerin toplam çalışma süresi.</td><td><code>Sum(Execution Duration - Manual)</code></td></tr><tr><td><strong>Fail Reason Distribution</strong></td><td>Başarısız testlerin sebeplerinin dağılımı (Development Error, Integration Error, Environment Issue, vb.)</td><td>Xray Failure Reason Alanına göre kategorik dağılım</td></tr><tr><td><strong>Test Count</strong></td><td>Seçilen tarih aralığında yürütülen toplam test sayısı.</td><td><code>Count(Tests or Executions)</code></td></tr><tr><td><strong>Test Count (with Bugs)</strong></td><td>Test çalıştırmalarında bug üreten testlerin oranı.</td><td><code>(Tests with bugs / Total Tests)</code></td></tr><tr><td><strong>Bug Resolution Rate</strong></td><td>Açılan test bug’larının kapanma oranı.</td><td><code>Closed Bugs / Total Test Bugs</code></td></tr><tr><td><strong>Bug Resolution Time</strong></td><td>Test bug’larının ortalama çözüm süresi.</td><td><code>Avg(Resolved - Created)</code></td></tr><tr><td><strong>UAT Duration</strong></td><td>UAT aşamasındaki toplam test süresi.</td><td><code>Sum(UAT Execution Duration)</code></td></tr><tr><td><strong>Leakage Root-Cause Mapping</strong></td><td>Kaçan hataların hangi test/çalıştırmadan kaynaklandığını gösterir.</td><td>Related Test Field / Related Execution Field / Linked Issues</td></tr><tr><td><strong>Tester Activity Metrics</strong></td><td>Testçilerin test sayısı, hata yakalama başarısı ve katkı düzeyi.</td><td>Kayıt bazlı hesaplamalar</td></tr><tr><td><strong>Team Test Performance Score</strong></td><td>Takıma ait tüm metriklerden türetilmiş birleşik kalite skoru.</td><td>Oobeya Hesaplama Motoru (Ağırlıklı Metrikler)</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (489).png" alt=""><figcaption><p>Team Scorecard – Test Analytics metrikleri</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (512).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Metrikler yalnızca **Admin Settings > Field Mapping** ve **Metric Thresholds** ayarları tamamlanmışsa hesaplanır.\
Ayrıntılar için bkz. [Test Analytics – Admin Settings](test-analytics-admin-ayarlari.md)
{% endhint %}

{% hint style="info" %}
Metrikler yalnızca "Related Team" kolonunda gelen takım bilgileri Oobeya'daki takımlar ile eşleştirilmişse takım seviyesinde hesaplanır.
{% endhint %}

***

### 4. Analiz Güncellemeleri ve Yeniden Eşleştirme

Eğer yeni Xray projeleri eklendiyse veya takım yapısı değiştiyse:

1. **Test Analytics** sayfasında analiz detayına girin.
2. **Update Analysis** butonuna tıklayın.
3. Gerekli durumlarda **Team Selection** adımını tekrar tamamlayın.

{% hint style="info" %}
Bu işlem mevcut metrikleri korur, sadece yeni takım-proje bağlantılarını günceller.
{% endhint %}

***

### 5. En İyi Uygulamalar (Best Practices)

* Her takımın sahip olduğu test projelerini net olarak belirleyin.
* Takım yapısı değiştiğinde (ör. QA ekibi bölünmesi), analizleri yeniden güncelleyin.
* Gereksiz veri kirliliğini önlemek için yalnızca aktif test projelerini bağlayın.
* **Escaped Defects** metriği için Jira’daki hata kayıtlarının doğru “UAT Defect Field” ile eşleştiğinden emin olun.

***

#### İlgili Dokümanlar

<table><thead><tr><th width="718.41845703125">Konu</th></tr></thead><tbody><tr><td><a href="../integrations/all-integrations/code-quality-addons/xray-integration.md">Xray Veri Kaynağı Ekleme</a></td></tr><tr><td><a href="yeni-test-analizi-olusturma.md">Yeni Test Analizi Oluşturma</a></td></tr><tr><td><a href="test-analytics-admin-ayarlari.md">Test Analytics – Admin Settings</a></td></tr></tbody></table>
