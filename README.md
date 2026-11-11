# YANKI-TR: Türkçe Haberlerde Yanıltıcı Teyidin Ölçülmesi ve Azaltılması

**TÜBİTAK 2209-A Üniversite Öğrencileri Araştırma Projeleri Destekleme Programı – Araştırma Önerisi (2026)**

> Türkçe Haberlerde Aynı Kökenden Türeyen İçeriklerin Yarattığı Yanıltıcı Teyit: Büyük Dil Modeli Tabanlı Doğrulamada Kaynak Kökeni Takibiyle Azaltılması

| | |
|---|---|
| **Proje yürütücüsü** | Tolga Kaya |
| **Danışman** | Prof. Dr. Mehmet Tekerek |
| **Kurum** | Ankara Üniversitesi |
| **Süre** | 12 ay |
| **Bütçe** | 11.500 TL |

## Dosyalar

| Dosya | Açıklama |
|---|---|
| [`Tolga_Kaya_2209A_Yanki_TR.pdf`](Tolga_Kaya_2209A_Yanki_TR.pdf) | Araştırma önerisi (okumak için) |
| [`Tolga_Kaya_2209A_Yanki_TR.docx`](Tolga_Kaya_2209A_Yanki_TR.docx) | Araştırma önerisi (düzenlenebilir Word sürümü) |

## Problem

Bir iddia on farklı sitede yer aldığında çoğu zaman “teyit edilmiş” kabul edilir. Oysa bu sitelerin çoğu aynı ajans bülteninden ya da birbirinden kopyalamış olabilir. Bu durum **dairesel raporlama** olarak adlandırılır: kaynak sayısı artar ama bağımsız kanıt sayısı artmaz. Büyük dil modeli (BDM) tabanlı doğrulama sistemleri belgeler arasındaki bu köken ilişkisini dikkate almadığından, karar vericiye **yanıltıcı teyit** sunabilir.

## Araştırma Soruları ve Hipotezler

- **AS1:** Dairesel raporlama, BDM tabanlı doğrulama sistemlerinin “teyit edildi” kararlarını ne ölçüde yanıltmaktadır?
- **AS2:** Kaynakları ham sayıları yerine bağımsız kök sayılarıyla değerlendirmek yanıltıcı teyidi azaltmakta mıdır?
- **AS3:** İddia düzeyinde doğal dil çıkarımı (NLI) denetimi atıf kesinliğini artırmakta mıdır?

| Hipotez | Beklenti | Test |
|---|---|---|
| **H1** | Köken analizi, yanıltıcı teyit oranını standart RAG’e göre en az %30 azaltır | McNemar |
| **H2** | NLI denetimi atıf kesinliğini en az 15 yüzde puanı artırır | Eşleştirilmiş bootstrap |
| **H3** | Bu iyileşme, gerçek teyitleri tanıma başarısını 5 puandan fazla düşürmez | Daha kötü olmama (non-inferiority) |

## Yöntem

- **Veri seti (YANKI-TR):** Teyit ve Doğruluk Payı tarafından incelenmiş 240 iddia, yaklaşık 1.800 belge; belgeler arası köken ilişkileri elle etiketlenir. Buna ek olarak 400 belgelik kontrollü bir sentetik yankı seti oluşturulur.
- **Köken çizgesi:** Açık atıf, metin benzerliği (MinHash) ve yayın zamanı kullanılarak belgeler yönlü döngüsüz bir çizgede (DAG) modellenir; destekleyici kaynaklar bağımsız kök sayısıyla değerlendirilir.
- **Deney deseni:** 2×2 faktöriyel desen (köken analizi açık/kapalı × NLI denetimi açık/kapalı).
- **Güvenilirlik damgası:** Çıktılar NATO Admiralty sistemine uyarlanmış A–F / 1–6 damgalarıyla raporlanır.

## İş Paketleri

| İP | İş paketi | Ay |
|---|---|---|
| 1 | YANKI-TR gerçek iddia setinin oluşturulması ve etiketlenmesi | 1–3 |
| 2 | Sentetik yankı setinin üretilmesi | 3–4 |
| 3 | Getirme ve köken çizgesi modülleri | 4–6 |
| 4 | Sorgu üretimi ve Türkçe NLI denetimi | 5–7 |
| 5 | Brifing, güvenilirlik damgası ve bütünleştirme | 7–8 |
| 6 | Deneyler, hipotez testleri ve hata analizi | 9–12 |

## Beklenen Çıktılar

- Türkçe haberler için köken etiketli ilk açık test seti (YANKI-TR)
- Açık kaynak deney yazılımı
- En az bir hakemli bildiri ve bir dergi makalesi

---

Bu depo, TÜBİTAK 2209-A formatında hazırlanmış araştırma önerisini içermektedir. Proje kodu ve veri seti, proje yürütüldükçe bu depoya eklenecektir.
