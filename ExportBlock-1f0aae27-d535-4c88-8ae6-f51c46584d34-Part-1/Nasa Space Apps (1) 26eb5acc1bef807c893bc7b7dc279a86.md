# Nasa Space Apps (1)

Deep Dive: Immersive Data Stories from Ocean to Sky 

Embiggen Your Eyes!     94 

Sharks from Space

Stellar Stories: Space Weather Through the Eyes of Earthlings

Through the Radar Looking Glass: Revealing Earth Processes with SAR 

Will It Rain On My Parade?

Commercializing Low Earth Orbit (LEO)

Your Home in Space: The Habitat Layout Creator

---

![TEIDE.jpeg](Nasa%20Space%20Apps%20(1)%2026eb5acc1bef807c893bc7b7dc279a86/TEIDE.jpeg)

[https://en.wikipedia.org/wiki/Synthetic-aperture_radar](https://en.wikipedia.org/wiki/Synthetic-aperture_radar)

# Sar verileri neye benzer?

## 📡  SAR Verileri Nasıl Üretilir?

- Uydu, **mikrodalga radar darbeleri** gönderir.
- Bu darbeler yeryüzünden **yansıyıp geri döner**.
- Uydu, geri dönen sinyalleri kaydeder → **görüntüye dönüştürülür**.

Bu yüzden SAR görüntüleri aslında **yansıyan radar enerjisinin şiddetini** gösterir, gözümüzle gördüğümüz renkleri değil.

---

## 🎨  SAR Görüntülerinin Görünümü

- SAR görüntüleri genellikle **siyah–beyaz veya gri tonlamalı** olur.
- **Parlak alanlar:** Radar sinyalini çok iyi yansıtan yüzeyler (ör. binalar, kayalar, metal yapılar).
- **Koyu alanlar:** Radar sinyalini soğuran veya düzgün yüzeyler (ör. durgun su, asfalt).

  Örnek:

- Bir şehir görüntüsünde **binalar bembeyaz parlar**.
- Bir göl veya deniz yüzeyi **simsiyah görünür**.
- Orman ve tarım alanları **gri ve benekli (speckle) dokular** şeklindedir.

## 👩🏼‍💻 SAR Verilerinin Kullanımı

- **Ham hali** biraz “gürültülü” ve benekli görünür (speckle noise).
- İşlenince (filtreleme, dB dönüşümü, renk kompozitleri):
    - VV → gri ton,
    - VH → renkli ton,
    - VV/VH oranı → renk kompozit haritalar (ör. kırmızı–yeşil–mavi) yapılabilir.

Yani son hali **optik uydu görüntüsüne benzemese de** çok güçlü bir analiz aracı olur.

![Ekran Resmi 2025-09-13 19.54.54.png](Nasa%20Space%20Apps%20(1)%2026eb5acc1bef807c893bc7b7dc279a86/Ekran_Resmi_2025-09-13_19.54.54.png)

![Ekran Resmi 2025-09-13 19.55.07.png](Nasa%20Space%20Apps%20(1)%2026eb5acc1bef807c893bc7b7dc279a86/Ekran_Resmi_2025-09-13_19.55.07.png)

### 2. SAR Verilerinin Polarizasyon Türleri

SAR sistemlerinde gönderilen ve alınan elektromanyetik dalgaların polarizasyonu, yüzeyden yansıyan sinyalin yapısını doğrudan etkiler. Bu sayede farklı yüzey özellikleri ayırt edilebilir:

- **HH (Horizontal–Horizontal)**
    - Yatay polarizasyonlu gönderim ve yatay alım.
    - Özellikle düzgün yüzeylerde (örneğin tarım alanları, su yüzeyleri) güçlü sinyal yansıması sağlar.
    - Metalik yüzeylerde daha belirgin kontrast verir.
- **VV (Vertical–Vertical)**
    - Dikey gönderim ve dikey alım.
    - Dikey yapıdaki unsurlar (binalar, dağ yamaçları) için hassastır.
    - Yüksek çözünürlüklü şehir haritalama çalışmalarında tercih edilir.
- **HV / VH (Cross-Polarized)**
    - Çapraz polarizasyon (yatay gönderim–dikey alım veya tersi).
    - Bitki örtüsü, orman yapısı ve yüzey pürüzlülüğü hakkında kritik bilgi sağlar.
    - Örneğin orman biyokütle hesaplamalarında kullanılır, çünkü dallar ve yapraklardan gelen saçılmayı yakalar.

👉 Uzman gözüyle baktığımızda: Haritalama çalışmasında tek polarizasyon yerine **çoklu polarizasyon (dual-pol veya quad-pol)** kullanıldığında, hem yüzeyin geometrik özellikleri hem de dielektrik özellikleri hakkında daha güvenilir çıkarımlar yapılır.

### 3. SAR Veri Ürün Türleri

Bir SAR misyonunda toplanan ham sinyaller, farklı işleme seviyelerinde ürünlere dönüştürülür. Bu ürünler haritalama projelerinde farklı amaçlara hizmet eder:

- **RAW (Ham Veri)**
    - Uydu radar anteninden doğrudan alınan işlenmemiş sinyallerdir.
    - Kullanıcı doğrudan bu veriyi işleyemez; yüksek düzeyde uzmanlık ve işleme algoritmaları gerekir.
- **SLC (Single Look Complex)**
    - Genlik ve faz bilgisini kompleks sayılar halinde içerir.
    - İnterferometri (InSAR) ve farklı zamanlarda çekilmiş görüntülerle yüzey hareketi ölçümleri için kritik öneme sahiptir.
    - Yer kabuğu deformasyonları, deprem sonrası yer değişimleri bu ürünle incelenir.
- **GRD (Ground Range Detected)**
    - Genlik bilgisini içerir, faz bilgisi yoktur.
    - Radar görüntüsü coğrafi olarak düzeltilmiştir.
    - Haritalama, afet izleme ve görselleştirme için en yaygın kullanılan üründür.
    - Örneğin Sentinel-1 verilerinde kamuya açık en çok indirilen veri tipidir.
- **Geocoded / Orthorectified Data**
    - Harita koordinat sistemine oturtulmuş ve topoğrafya etkileri düzeltilmiş veridir.
    - Coğrafi Bilgi Sistemleri (GIS) ortamında doğrudan kullanılabilir.
    - Özellikle arazi örtüsü sınıflandırmaları ve tematik haritalar için tercih edilir.

👉 Profesyonel kullanımda şu ayrımı yapmak önemlidir: **Bilimsel araştırmalar ve hassas deformasyon ölçümleri** için SLC tercih edilirken, **şehir planlama ve geniş ölçekli haritalama projeleri** için GRD ve ortorektifiye veriler kullanılır.

**Faydalı projeler**

[https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/asturexplorers/?tab=project](https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/asturexplorers/?tab=project)

[https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/team-io/?tab=project](https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/team-io/?tab=project)