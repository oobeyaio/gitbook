---
description: >-
  Oobeya Test Analytics modülü, test yönetimi araçları üzerinde yürütülen test
  süreçlerini analiz ederek test verimliliğini, hata oranlarını ve ekip
  performansını ölçmeyi sağlar.
hidden: true
---

# 1. Yeni Test Analizi Oluşturma

**Test Analytics** modülü, Jira Xray gibi test yönetimi araçları üzerinde yürütülen test süreçlerini analiz ederek test verimliliğini, hata oranlarını ve ekip performansını ölçmeyi sağlar.\
Bu sayfa Oobeya'da yeni bir test projesi analizi oluşturma sürecini adım adım açıklar.

{% hint style="info" %}
Başlamadan önce test yönetim aracı entegrasyonunun tamamlandığından emin olun.\
Ayrıntılar için bkz. [Xray Veri Kaynağı Ekleme](../integrations/all-integrations/code-quality-addons/xray-integration.md)
{% endhint %}

***

### Test Analytics Başlatma

**Menü Yolu:**\
`Analytics > Test Analytics`

Yeni bir test projesi analizi oluşturmak için "**New Project"** butonuna tıklayın.\
Bu işlem, 5 adımlı bir konfigürasyon akışını başlatır:

1. Project Selection
2. UAT Status Mapping
3. Team Selection
4. Status Mapping
5. Final Review

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>Create Test Analytics</p></figcaption></figure>

***

### 1. Proje Seçimi (Project Selection)

Bu adımda test yönetim aracınızdaki analiz etmek istediğiniz test projelerini seçebilirsiniz.

<table><thead><tr><th width="241.62823486328125">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Data Source</strong></td><td>Daha önce oluşturduğunuz Xray veri kaynağını seçin.</td></tr><tr><td><strong>Project Category</strong></td><td>Analiz etmek istediğiniz test kategorisini belirtin (örneğin: All Projects veya belirli kategori).</td></tr><tr><td><strong>Projects</strong></td><td>Analiz kapsamına dahil edilecek test projelerini seçin.</td></tr></tbody></table>

***

### 2. UAT Status Mapping

Bu aşamada, test süreçlerinizde **UAT (User Acceptance Test)** durumlarının tanımlandığı projeleri eşleştirirsiniz.

| Alan               | Açıklama                                                                                      |
| ------------------ | --------------------------------------------------------------------------------------------- |
| **Upper Projects** | Test yönetim aracı içinde UAT süreçlerini içeren üst projeyi seçin.                           |
| **Test Mapping**   | UAT aşamasını temsil eden test durumunu girin (örneğin: `UAT`, `Acceptance`, `Ready for QA`). |

***

### 3. Takım Seçimi (Team Selection)

Test projelerinde yer alan test aktivitelerini Oobeya’daki takımlarla eşleştirin.\
Sol paneldeki proje veya organizasyon hiyerarşisinden ekiplerinizi seçip sağ panele taşıyabilirsiniz.

<table><thead><tr><th width="200.60028076171875">Alan</th><th>Açıklama</th></tr></thead><tbody><tr><td><strong>Available Teams</strong></td><td>Oobeya üzerindeki tüm takımlar.</td></tr><tr><td><strong>Selected Teams</strong></td><td>Analiz kapsamında ilişkilendirilecek Oobeya takımları.</td></tr></tbody></table>

{% hint style="info" %}
Bu eşleşme, analiz sonrası takım bazlı metriklerin hesaplanabilmesi için gereklidir.\
Detaylar için bkz. [Team Mapping & Scorecard Entegrasyonu](takim-eslemesi.md)
{% endhint %}

***

### 4. Status Mapping

Test durumlarınızı, Oobeya’nın standart aşamalarıyla eşleştirin.\
Bu sayede analiz sırasında testlerin durumu doğru sınıflandırılır.

<table><thead><tr><th width="192.3499755859375">Oobeya Durumu</th><th>Örnek Xray Durumları</th></tr></thead><tbody><tr><td><strong>To Do</strong></td><td>To Do, Selected for Development, Backlog</td></tr><tr><td><strong>In Progress</strong></td><td>In Progress, UAT</td></tr><tr><td><strong>Done</strong></td><td>Done, Closed, Resolved</td></tr><tr><td><strong>Rejected</strong></td><td>Cancelled, Invalid</td></tr></tbody></table>

{% hint style="info" %}
Her satırda birden fazla durum seçilebilir. Bu eşleştirme, test aşamalarının analizlerde doğru gruplandırılmasını sağlar.
{% endhint %}

***

### 5. Final Review

Yapılandırmayı tamamladıktan sonra, tüm seçili bilgileri gözden geçirebilirsiniz.

<table><thead><tr><th width="249.53240966796875">Bölüm</th><th>İçerik</th></tr></thead><tbody><tr><td><strong>Test Info</strong></td><td>Veri kaynağı, proje, kategori, üst proje ve test mapping bilgileri</td></tr><tr><td><strong>Teams</strong></td><td>Analize dahil edilen takımlar listesi</td></tr><tr><td><strong>Status Mapping Review</strong></td><td>Tüm test durumlarının Oobeya standardına göre eşleştirilmiş hali</td></tr></tbody></table>

✅ **Done** butonuna bastığınızda analiz işlemi başlar.\
Veri işlendikten sonra sonuçlar **Test Analytics Dashboard**’da görüntülenir.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>Test Analytics Dashboard</p></figcaption></figure>

***

### Sonraki Adımlar

* Analiz sonuçlarını doğru yorumlamak için [Test Analytics Admin Settings](test-analytics-admin-ayarlari.md) sayfasındaki ayarları yapılandırın.
* Takım bazlı metrikleri görmek için [Team Mapping & Scorecard dokümanı](takim-eslemesi.md)na göz atın.
