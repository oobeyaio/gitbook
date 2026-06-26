---
hidden: true
icon: trophy
---

# Gamification (Oyunlaştırma)

Oobeya’nın **Gamification** modülü, mühendislik ekiplerinin performansını artırmak için puan tabanlı rekabetçi bir yapı sunar. Takımların ilerlemelerini görselleştirir, motivasyonu artırır ve başarıları görünür kılar. Bu özellik ile ligler oluşturabilir, performans metriklerini tanımlayabilir, takımlar arasında puanları karşılaştırabilir ve yüksek performansı ödüllendirebilirsiniz.

<figure><img src="../.gitbook/assets/image (459).png" alt="Oobeya Gamification Module"><figcaption><p>Oobeya Gamification Module</p></figcaption></figure>

***

### 📌 Temel Kavramlar

* **League (Lig)**: Takımların performans metriklerine göre puan topladığı yarışma yapısıdır.
* **Round (Tur)**: Belirli aralıklarla puan hesaplamalarının yapıldığı dönemlerdir (örn. haftalık, iki haftalık ve aylık).
* **Referees (Hakemler)**: Otomatik hesaplamalara ek olarak manuel puanlamayı denetleyen, sonuçları güncelleme ve onaylama hakkına sahip kullanıcılardır.
* **Points (Puanlar)**: Belirlenen eşik değerlerine göre takımlara otomatik veya manuel olarak verilen sayısal değerlerdir.

***

### ⚙️ Nasıl Çalışır?

<figure><img src="../.gitbook/assets/image (460).png" alt=""><figcaption><p>Create New League - step by step</p></figcaption></figure>

#### 1. Lig Oluşturma (League Setup)

**Gamification > Leagues Management > New League** adımından yeni bir lig oluşturabilirsiniz.

Gerekli alanlar:

* **Lig Adı** ve **Açıklama**
* **Hakemler**: En az 1, en fazla 5 kullanıcı seçilmelidir.
* **Puanlama Aralığı**: Haftalık, iki haftalık, aylık
* **Başlangıç / Bitiş Tarihi** _(isteğe bağlı)_
* **Lig Logosu** _(isteğe bağlı)_

> ⚠️ Bitiş tarihi girilirse, başlangıç tarihinden en az 28 gün sonra ve en fazla 365 gün içinde olmalıdır. Bitiş tarihi boş bırakılırsa lig süresiz olarak devam eder.

***

#### 2. Metrik Seçimi (Metric Selection)

<figure><img src="../.gitbook/assets/image (461).png" alt=""><figcaption><p>Metric Selection</p></figcaption></figure>

Lig kapsamında puanlanacak performans metriklerini seçin. Kategoriler:

* **Proje Yönetimi** (Örn. Lead Time, Predictability)
* **Geliştirme** (Örn. Rework Rate, Coding Efficiency)
* **Kod İnceleme**
* **Kod Kalitesi**
* **Güvenlik**
* **Semptomlar**

> Bu adımda seçilen metrikler, **otomatik puanlama** için kullanılacaktır.

***

#### 3. KPI Puanlama (KPI Scoring)

<figure><img src="../.gitbook/assets/image (462).png" alt=""><figcaption><p>KPI Scoring</p></figcaption></figure>

Her metrik için puanlama eşikleri tanımlayın. Örnek:

* Cycle Time < 3 gün → 3 puan
* 3–10 gün arası → 1 puan
* 10 gün → 0 puan

> Eşiklerin mantıksal tutarlılığı kullanıcı sorumluluğundadır.

***

#### 4. Manuel KPI'lar (İsteğe Bağlı) (Manual KPIs)

<figure><img src="../.gitbook/assets/image (463).png" alt=""><figcaption><p>Manual KPIs</p></figcaption></figure>

Manuel olarak hakemler tarafından puanlanacak özel KPI’ları tanımlayın.

Her KPI için:

* Etiket (Ad)
* Açıklama
* Maksimum Puan

***

#### 5. Takım Seçimi (Team Selection)

<figure><img src="../.gitbook/assets/image (464).png" alt=""><figcaption><p>Team Selection</p></figcaption></figure>

Lige dahil olacak takımları belirleyin. Sadece ilgili metriklerde verisi olan takımlar seçilmelidir.

***

#### 6. Son Kontrol ve Başlatma (Final Review)

Tüm ayarları gözden geçirin ve **Lig Oluştur** butonu ile süreci başlatın.

***

### 🔄 Round (Tur) Yönetimi

Her lig, seçilen zaman aralığında otomatik olarak bir tur **(round)** oluşturur.

Round'lar o ligin hakemleri tarafından yönetilebilir **--> League Management > Manage Rounds**

<figure><img src="../.gitbook/assets/image (465).png" alt=""><figcaption><p>Manage Rounds</p></figcaption></figure>

#### Round Özellikleri:

<figure><img src="../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>

* **Hesaplama Tarihi (Round Date)**: Puanların hesaplandığı tarihtir.
* **Round Durumları (State)**:
  * `Sonraki Tur İçin Planlandı (Scheduled for the next round)`
  * `İşleniyor (In Progress)`
  * `Onay Bekliyor (Pending Approval)`
  * `Onaylandı (Approved)`
  * `Hata (Failed)`
  * `İptal Edildi (Cancelled)`

Hakemler, tur puanlarını **inceleyip onaylayabilir** veya gerekirse düzenleme yapabilir.

***

### ✏️ Puan Güncelleme (Update Scores)

<figure><img src="../.gitbook/assets/image (467).png" alt=""><figcaption><p>Update Scores for a round</p></figcaption></figure>

Her KPI için hakemler:

* Gerçekleşen metrik değerini görebilir. (Value)
* Otomatik hesaplanan puanı kontrol edebilir. (Calculated Score)
* Gerekirse puanı manuel olarak düzenleyebilir. (Update)
* “Onayla” butonu ile puanı sabitleyebilir.&#x20;

> Tüm otomatik puanlar tekrar sağ üstte yer alan **Yeniden Hesapla (Recalculate)** butonu ile güncellenebilir.

***

### 📊 Lider Tablosu (Leaderboard)

<figure><img src="../.gitbook/assets/image (469).png" alt=""><figcaption><p>Leaderboard</p></figcaption></figure>

Lider tablosu, takımların toplam puanlarına göre sıralamasını gösterir:

* Zaman içindeki ilerlemeyi izleyin.
* Geçmiş turlara dönük detaylara ulaşın.
* Hangi takımın hangi metrikten puan kazandığını görün.

***

### 🔐 Yetkilendirme

Aşağıdaki işlemleri yalnızca yetkili kullanıcılar gerçekleştirebilir:

* Lig oluşturma ve düzenleme. (Role Gamification Admin)
* Metrik ve puanlama kurallarını tanımlama.  (Role Gamification Admin)
* Round sonuçlarını onaylama. (League Referees)

<figure><img src="../.gitbook/assets/image (471).png" alt=""><figcaption><p>Manage user roles</p></figcaption></figure>
