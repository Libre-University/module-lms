# module-lms

LibreUniversity **Öğrenme Yönetim Sistemi (LMS)** modülü: ders sayfaları, materyal, duyuru, ödev ve Jitsi tabanlı canlı ders ([MODULES.md §3](https://github.com/Libre-University/docs/blob/main/MODULES.md), [FR-03](https://github.com/Libre-University/docs/blob/main/FUNCTIONAL_REQUIREMENTS.md)).

Bu repo, `platform-api` uygulamasına kurulan bağımsız bir Django uygulama paketidir (`libre-university-lms`). Şube ve kayıt bilgisini `module-obs`'in genel servis API'sinden, canlı ders altyapısını `adapters` reposundaki Jitsi adapterinden alır ([ADR-0010](https://github.com/Libre-University/docs/blob/main/docs/adr/0010-develop-modules-as-separate-packages.md)).

## Ne İş Yapar?

- Şube başına ders sayfası ve haftalık izlence
- Materyal paylaşımı (PDF, video, bağlantı, metin)
- Duyuru ve tartışma forumu
- Ödev tanımı ve teslimi, geç teslim işaretleme
- Jitsi canlı ders: yetkili başlatma, JWT ile moderatör/katılımcı rolleri
- İleride: kayıtların VOD olarak izlenceye eklenmesi, online sınav

## Sahip Olduğu Veriler

`CoursePage`, `LearningMaterial`, `Assignment`, `AssignmentSubmission`, `LiveSession` ([DATA_MODEL.md](https://github.com/Libre-University/docs/blob/main/DATA_MODEL.md)).

## Fazlara Göre İşler

| Faz | Bu repoda yapılacaklar |
| --- | --- |
| Faz 0 | Modül şablonundan iskelet, CI, LMS iş kurallarının kabul kriterleri olarak yazılması |
| Faz 1 | Bu repoda iş yok (çekirdek platform bekleniyor) |
| Faz 2 | `CoursePage` ve `LearningMaterial` temeli, şube erişim kuralları |
| Faz 3 | Duyuru, forum, ödev teslimi, Jitsi canlı ders (MVP'nin LMS akışları) |
| Faz 4+ | VOD kayıt hattı, online sınav, intihal denetimi entegrasyonu |

Ayrıntılı ve işaretlenebilir liste: [ROADMAP.md](ROADMAP.md). Fazlar [ana yol haritası](https://github.com/Libre-University/docs/blob/main/ROADMAP.md) ile hizalıdır. Açık işler için `phase:*` etiketlerine bakın.

## Katkı

Katkı rehberi, davranış kuralları ve güvenlik politikası organizasyon genelinde [`.github`](https://github.com/Libre-University/.github) reposundadır. Mimari kararlar [`docs`](https://github.com/Libre-University/docs) reposundaki ADR'lerle alınır.

## Lisans

Lisans kararı [ADR-0002](https://github.com/Libre-University/docs/blob/main/docs/adr/0002-prefer-agpl-3-or-later-license.md) ile kesinleştirilecektir (öneri: AGPL-3.0-or-later).
