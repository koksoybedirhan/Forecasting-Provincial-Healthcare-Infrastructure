# SAUCIS makalesi veri setleri (son surumler)

Makale: Forecasting Provincial Healthcare Infrastructure and Budget Allocation in Turkey Using Machine Learning and TOPSIS

Bu klasorde makalede kullanilan veri setlerinin en guncel surumleri bulunur. Dosyalar orijinal konumlarindan kopyalanmistir, orijinallere dokunulmamistir. Ham kaynaklar `ham-kaynaklar/` altindadir.

| Dosya | Orijinal konum | Aciklama |
|---|---|---|
| `01_saglik-altyapisi-il_2002-2024_uzun-format.csv` | `yenicalisma/all_data24.csv` | Il bazli hastane sayisi, yatak, nufus, personel (6 kategori x devlet/ozel/universite), 2002-2024, 81 il. Uzun format (57.753 satir). TUIK Biruni. |
| `02_saglik-altyapisi-il_2002-2024_model-girdisi-genis-format.csv` | `yenicalisma/model_giris.csv` | 01 numarali dosyadan uretilen genis format (1.863 satir = 81 il x 23 yil). IFM modellerinin dogrudan girdisi. |
| `03_nufus-il_2025-2030_IFM-dogrusal-ekstrapolasyon.csv` | `yenicalisma/nufus_projeksiyonu_2025_2030.csv` | IFM (altyapi tahmini) modulunde kullanilan il nufusu 2025-2030 (486 satir). Son 10 yilin dogrusal trendinden uretilmis. |
| `04_TOPSIS-girdisi_2025-2030_nufus-yas-hekim-yatak-tahminleri.csv` | `yenicalismatopsis/2025_2030_tum_hedefler_final_tahmin.csv` | TOPSIS modulunun girdisi (486 satir). Nufus: 2025 gercek ADNKS, 2026-2030 TUIK bias-correction. Yas 0-14, 65+, hekim ve yatak orani tahmin degerleridir. |
| `05_nufus-yas-gruplari-il_2007-2025_0-14-ve-65plus.csv` | `yenicalismatopsis/2025nufus-yas.csv` | Il bazli yas grubu nufuslari 2007-2025 (TUIK, ham cok satirli format). TOPSIS yas kriterleri icin. |
| `06_hekim-sayisi-1000-kisi-basina-il_2002-2024.csv` | `yenicalismatopsis/1000kisibasinahekim.csv` | 1000 kisi basina hekim sayisi, il bazli, 2002-2024 (TUIK, pivot format). |
| `07_hastane-yatagi-100bin-kisi-basina-il_2002-2024.csv` | `yenicalismatopsis/100binkisibasinahastaneyatak.csv` | 100 bin kisi basina hastane yatagi, il bazli, 2002-2024 (TUIK, pivot format). |
| `08_saglik-harcamasi-turkiye_1999-2024_temiz.xlsx` | `yenicalismabutce/99-24saglikbutcesi_temiz.xlsx` | Turkiye genel saglik harcamasi, yillik, 1999-2024 (TL). Butce modulunun girdisi. |
| `09_USDTRY-aylik-gecmis_1999-2024_Investing.csv` | `yenicalismabutce/usd-try.csv` | Aylik USD/TRY kuru gecmisi, 1999-2024 (Investing.com). |
| `10_USDTRY-aylik_2025-2030_gercek-ve-tahmin.csv` | `yenicalismabutce/usdtry_aylik_tahmin_2026_2030.csv` | Aylik USD/TRY 2025-2030 (72 satir). 'kaynak' sutunu Gercek / Interpolasyon etiketli. |
| `ham-kaynaklar/ham_hastane-sayisi-il_2002-2024.csv` | `yenicalisma/hamveriler/02-24veriler/hastane.csv` | 01 numarali dosyanin ham girdisi: hastane sayisi. |
| `ham-kaynaklar/ham_hastane-yatak-sayisi-il_2002-2024.csv` | `yenicalisma/hamveriler/02-24veriler/yatak.csv` | 01 numarali dosyanin ham girdisi: yatak sayisi. |
| `ham-kaynaklar/ham_saglik-personeli-il_2002-2024.csv` | `yenicalisma/hamveriler/02-24veriler/personel.csv` | 01 numarali dosyanin ham girdisi: personel. |
| `ham-kaynaklar/ham_il-nufus_2002-2022.csv` | `yenicalisma/hamveriler/02-24veriler/nufüs.csv` | 01 numarali dosyanin ham girdisi: il nufusu 2002-2022. |
| `ham-kaynaklar/ham_il-nufus_2023-2024.csv` | `yenicalisma/hamveriler/02-24veriler/nufus2324.csv` | 01 numarali dosyanin ham girdisi: il nufusu 2023-2024 (guncel surum). |
| `ham-kaynaklar/ham_TUIK-il-nufus-projeksiyonu_2023-2030.xls` | `yenicalisma/hamveriler/tuik23-30tahmin/Yıllara Göre İl Nüfusları.xls` | TUIK orijinal il nufus projeksiyonu 2023-2030. |
| `ham-kaynaklar/ham_TUIK-il-nufus-projeksiyonu_bias-correction-guncellenmis.xlsx` | `yenicalisma/hamveriler/tuik26-30hesaplanmis/Turkiye_Nufus_Projeksiyon_Guncellenmis.xlsx` | TUIK projeksiyonunun 2024-2025 gercek ADNKS ile guncellenmis hali (TOPSIS nufus kaynagi). |
| `ham-kaynaklar/ham_saglik-harcamasi-turkiye_1999-2024.xls` | `yenicalismabutce/99-24saglikbutcesi.xls` | 08 numarali dosyanin ham hali. |

## Bilinen tutarsizliklar (makale ile dosyalar arasinda)

- Nufus 2025-2030: IFM icin 03 numarali dosya (dogrusal ekstrapolasyon, 486 cift), TOPSIS icin 04 numarali dosya (TUIK bias-correction) kullanilmis. Makale yalnizca TUIK 2025/2030 + dogrusal ekstrapolasyon anlatiyor.
- Saglik harcamasi dosyasi 26 yil iceriyor, makale 25 yaziyor. USD/TRY gecmis dosyasi 311 satir, makale 300 yaziyor.
