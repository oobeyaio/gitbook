---
description: >-
  Geliştirici aktivitelerini görselleştirerek iş yükü dengesizliklerini ve
  sağlıksız çalışma pratiklerini tespit etmenizi sağlar.
hidden: true
---

# Aktivite Isı Haritası (Activity Heatmap)

Oobeya **Activity Heatmap** modülü, yazılım geliştirme ekiplerinin günlük aktivitelerini görselleştirerek, **iş yükü dağılımını**, **katkı çeşitliliğini** ve **geliştirici deneyimini** analiz etmeyi sağlar. Commit, Pull Request (code review), kod değişiklikleri ve yorumları gibi çeşitli aktiviteleri skorlayarak zaman içindeki eğilimleri ısı haritası formatında sunar.

Bu modül sayesinde:

* Aşırı yüklenmiş veya düşük katkı sağlayan geliştiriciler belirlenebilir.
* Dengesiz iş yükü dağılımları tespit edilir.
* Takım içinde adil görev paylaşımı teşvik edilir.

***

### 1. Genel Özellikler

* Günlük, haftalık, aylık, çeyreklik veya özel tarih aralığında analiz
* PR, commit, kod satır değişiklikleri ve kod gözden geçirme yorum aktivitelerinin takibi
* Geliştirici bazında renkli ısı haritası görünümü
* Geliştirici İş Günlüğü (Work Log) ile detaylı süreç katkı analizi
* Takım seçimi ve rol bazlı filtreleme
* Çalışma günü filtresi (Admin Panel > General Settings üzerinden yapılandırılır)

<figure><img src="../.gitbook/assets/image (481).png" alt=""><figcaption><p>Activity Heatmap Genel Görünüm</p></figcaption></figure>

***

### 2. Skor Hesaplama Mekanizması

**Activity Heatmap** modülünde geliştirici aktiviteleri farklı katkı türlerinden alınan verilerle hesaplanır ve normalize edilerek ısı haritasında görselleştirilir.

#### 2.1. Günlük Normalizasyon & Z-Skor:

1. Her günün en yüksek skor alan geliştiricisi %100 referans olarak alınır.
2. Diğer geliştiriciler bu maksimum değere oranlanır → `rank_ratio`
3. Günlük katkılar normalize edilir.
4. Tüm geliştiricilerin ortalama oranı ve standart sapması hesaplanır.
5. Bu oranlar **z-skoruna** çevrilerek 0–100 aralığına normalize edilir.
6. Isı haritasında bu skorlar renk tonlarına dönüştürülür.

#### 2.2. Aktivite Bazlı Skor Formülleri:

**2.2.1. Commit Aktiviteleri:**

```
COMMIT_SCORE = (COMMITS × commit_coeff) +
               (LINES_ADDED × added_coeff) +
               (LINES_DELETED × deleted_coeff) +
               (LINES_EDITED × edited_coeff)
```

**2.2.2. Pull Request Aktiviteleri:**

```
PR_OPEN_SCORE        = PRs Created × pr_open_coeff
PR_REVIEW_SCORE      = PR Reviews × pr_review_coeff
PR_APPROVAL_SCORE    = PR Approvals × pr_approve_coeff
PR_NEEDS_WORK_SCORE  = PR Needs Work × pr_needs_work_coeff
PR_COMMENT_SCORE     = PR Comments × pr_comment_coeff
```

**2.2.3. Toplam Skor:**

```
TOTAL_RANK_SCORE = COMMIT_SCORE + PR_OPEN_SCORE + PR_REVIEW_SCORE +
                   PR_APPROVAL_SCORE + PR_NEEDS_WORK_SCORE + PR_COMMENT_SCORE
```

**2.2.4. Isı Haritasına Yansıtma:**

* Normalize edilen skorlar renk tonlarına dönüştürülür.
* Koyu renkler yüksek aktiviteyi, açık renkler düşük aktiviteyi gösterir.

{% hint style="info" %}
Bu mekanizma sayesinde ekipler arasında **adil karşılaştırmalar** yapılabilir, farklı aktivite türlerinin etkisi organizasyon ihtiyaçlarına göre ayarlanabilir ve sonuçlar görsel olarak kolayca takip edilebilir.
{% endhint %}

***

### 3. Admin Panel Ayarları

Farklı faaliyetlere ağırlık değerleri atanır. Bu katsayılar, her bir faaliyet türünün genel ısı haritası skorunu ve sıcaklık görselleştirmesini nasıl etkilediğini belirler.

**Konum:** `Administration > Activity Heatmap`

#### Katsayı (Coefficient) Ayarları

Her aktivite türü için, katkının toplam skor üzerindeki ağırlığını belirleyebilirsiniz.

<table><thead><tr><th width="211.52728271484375">Aktivite</th><th width="395.47412109375">Açıklama</th><th>Varsayılan</th></tr></thead><tbody><tr><td>Commits</td><td>Yapılan commit sayısı</td><td>2.0</td></tr><tr><td>Lines Added</td><td>Eklenen kod satırı</td><td>0.1</td></tr><tr><td>Lines Deleted</td><td>Silinen kod satırı</td><td>0.1</td></tr><tr><td>Lines Edited</td><td>Değiştirilen kod satırı</td><td>0.1</td></tr><tr><td>PRs Created</td><td>Açılan PR sayısı</td><td>1.0</td></tr><tr><td>PR Reviews</td><td>Yapılan kod incelemeleri</td><td>1.5</td></tr><tr><td>PR Approvals</td><td>Onaylanan PR sayısı</td><td>0.25</td></tr><tr><td>PR Needs Work</td><td>Geri gönderilen PR sayısı</td><td>0.5</td></tr><tr><td>PR Comments</td><td>PR’lerde yapılan yorum sayısı</td><td>1.0</td></tr></tbody></table>

<figure><img src="https://your-link.com/activity_heatmap_admin.png" alt=""><figcaption><p>Admin Panel – Activity Coefficients</p></figcaption></figure>

***

### 4. Dashboard Bileşenleri

**Activity Heatmap Dashboard**, geliştiricilerin günlük aktivitelerini farklı açılardan analiz edebilmeniz için birden fazla bileşenden oluşur. Her bileşen, katkı türlerini, zaman içindeki eğilimleri ve ekip içindeki dağılımları farklı perspektiflerden görselleştirir.

#### 4.1. Etkinlik Isı Haritası (Activity Heatmap)

**Activity Heatmap**, geliştiricilerin günlük aktivitelerini görselleştiren temel bileşendir. Her hücre, bir geliştiricinin belirli bir gündeki katkı skorunu temsil eder.

* **Renk Yoğunluğu**: Hücrenin rengi, geliştiricinin o günkü performans seviyesini yansıtır. Daha koyu tonlar yüksek aktiviteyi, daha açık tonlar düşük aktiviteyi gösterir.
* **Normalize Edilmiş Skorlar**: Günlük skorlar, o günün en yüksek katkısına göre normalize edilerek %0–%100 aralığına dönüştürülür. Bu sayede farklı günler ve geliştiriciler arasında adil bir karşılaştırma yapılabilir.
* **Zaman Filtreleri**: Günlük, haftalık, aylık ya da özel tarih aralıklarına göre analiz yapılabilir.

{% hint style="info" %}
Activity Heatmap, ekiplerin iş yükü dengesizliklerini görsel olarak fark etmesini ve potansiyel aşırı yüklenmeleri ya da düşük katılımları hızlıca tespit etmesini sağlar.
{% endhint %}

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>Activity Heatmap</p></figcaption></figure>

#### 4.2. Geliştirici İş Günlüğü (Developer Work Log)

**Developer Work Log**, seçilen tarih aralığında her geliştiricinin günlük aktivitelerini ayrıntılı olarak listeler. Isı haritası üzerinde görülen skorların arka planındaki ham verileri tablo formatında sunar.

Bu bölümde:

* **Geliştirici bazında toplam skor** (normalize edilmiş)
* **Toplam aktivite sayıları** (commit, PR, yorum vb.)
* **Günlük katkı hücreleri** ile her gün için yapılan aktiviteler ve bu aktivitelerin puan karşılıkları

görüntülenir.

{% hint style="info" %}
Amaç, sadece genel skorlara bakmakla kalmayıp, her bir geliştiricinin hangi günlerde daha aktif olduğunu ve hangi katkı türlerinde yoğunlaştığını ayrıntılı şekilde analiz etmektir.
{% endhint %}

<figure><img src="../.gitbook/assets/image (483).png" alt=""><figcaption><p>Developer Work Log</p></figcaption></figure>

#### 4.3. Filtreler

**Activity Heatmap** modülü, daha odaklı ve anlamlı analizler yapabilmeniz için çeşitli filtreleme seçenekleri sunar:

* **Çalışma Günleri (Working Days)**: Skorların yalnızca şirketinizin tanımlı çalışma günleri (örn. Pazartesi–Cuma) üzerinden hesaplanmasını sağlar. Bu ayar, **Admin > General Settings** bölümünden yapılandırılır.
* **Takım Seçimi (Team Selection)**: Bir veya birden fazla takım seçilerek, ısı haritasında yalnızca bu takımlara ait aktiviteler görüntülenebilir.
* **Rol Filtresi (Role Filter)**: Organizasyon içindeki belirli roller (örn. Developer, QA) seçilerek, sadece bu rollerin aktiviteleri analizlere dahil edilir. Bu sayede doğrudan geliştirme dışındaki katkılar hariç tutulabilir.
* **Aktivite Türü (Activity Type)**: İstenilen aktivite türleri (Commit, PR açma, Review, Yorum vb.) seçilerek, ısı haritası sadece bu aktiviteler üzerinden görüntülenebilir.

{% hint style="info" %}
Bu filtreler sayesinde ekipler, belirli zaman aralıklarında, belirli roller veya aktiviteler özelinde, çok daha net ve hedefli içgörüler elde edebilir.
{% endhint %}

<figure><img src="../.gitbook/assets/image (482).png" alt="" width="461"><figcaption><p>Modül Filtreleri</p></figcaption></figure>

***

### 5. Veri Kaynakları

**Activity Heatmap** modülü, geliştirici aktivitelerini hesaplamak için farklı yazılım geliştirme araçlarından ve katkı türlerinden veri toplar.

* **Commits**: Git repository’lerindeki commit kayıtları  (_Azure DevOps, GitHub, GitLab, Bitbucket, Gitea_)
* **Kod Değişiklikleri**: Eklenen, silinen ve düzenlenen satır sayıları
* **Pull Requestler**: Açılan PR’lar (GitHub, GitLab, Bitbucket, Azure Repos vb.)
* **Kod İncelemeleri (Reviews)**: Yapılan kod incelemeleri, onaylanan veya geri gönderilen PR’lar
* **Yorumlar (Comments)**: Pull request üzerinde yapılan yorumlar
* **Developer Profiles**: Yalnızca Oobeya’da tanımlı geliştirici profillerinin aktiviteleri hesaplamaya dahil edilir.

{% hint style="info" %}
Bu kaynaklardan gelen veriler, admin panelde tanımlanan katsayılarla ağırlıklandırılarak toplam skora dönüştürülür.
{% endhint %}

***

### 6. Önerilen Kullanımlar

**Activity Heatmap** modülü, ekip aktivitelerinin daha adil, dengeli ve verimli hale getirilmesi için farklı senaryolarda kullanılabilir:

<table><thead><tr><th width="218.51544189453125">Senaryo</th><th>Kazanım</th></tr></thead><tbody><tr><td><strong>Sprint Değerlendirmeleri</strong></td><td>Sprint sonunda geliştiricilerin katkı yoğunluklarını analiz ederek daha sağlıklı retrospektifler yapılmasını sağlar.</td></tr><tr><td><strong>İş Yükü Dengesi</strong></td><td>Aşırı yüklenen veya düşük katılım gösteren ekip üyelerini belirleyerek görev dağılımını dengeler.</td></tr><tr><td><strong>Katılım ve Motivasyon</strong></td><td>Düzenli olarak düşük katkı yapan geliştiricileri tespit ederek motivasyon artırıcı aksiyonlar alınmasını sağlar.</td></tr><tr><td><strong>PR İnceleme Kültürü</strong></td><td>Kod inceleme, yorum ve onay aktiviteleri üzerinden ekiplerin review kültürünü ölçmeye yardımcı olur.</td></tr><tr><td><strong>Performans İyileştirme</strong></td><td>Ekiplerin iş birliği ve katkı çeşitliliğini izleyerek eğitim ve koçluk ihtiyaçlarını ortaya çıkarır.</td></tr></tbody></table>

{% hint style="info" %}
Bu modül yalnızca bireysel performans ölçümü için değil, aynı zamanda ekiplerin **katılım seviyesini** ve **iş yükü dengesini** izlemek için de güçlü bir takım yönetimi aracıdır.
{% endhint %}

***

### 7. SSS (Sıkça Sorulan Sorular)

<details>

<summary>Neden bazı geliştiriciler hiç görünmüyor?</summary>

Sadece Oobeya platformunda kayıtlı ve aktif takımlara atanmış geliştiricilerin aktiviteleri analiz edilir.

</details>

<details>

<summary>Skorlar neye göre belirleniyor?</summary>

Her aktiviteye ait katkı, admin paneldeki katsayılarla çarpılarak toplanır. Bu skor günlük normalize edilir.

</details>

<details>

<summary>Çalışma günü filtresi ne işe yarar?</summary>

Hafta sonu gibi çalışma günü dışındaki günlerin analiz dışında tutulmasını sağlar.

</details>
