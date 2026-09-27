# module-lms Yol Haritası

İş kuralları: [DATA_MODEL.md › LMS](https://github.com/Libre-University/docs/blob/main/DATA_MODEL.md). Canlı ders akışı: [UML.md](https://github.com/Libre-University/docs/blob/main/UML.md).

## Faz 0: Hazırlık (davet öncesi)

- [ ] `platform-api` modül şablonundan paket iskeleti (`libre-university-lms`)
- [ ] CI: ruff, mypy, pytest (modül test düzeneğiyle), migration kontrolü
- [ ] LMS iş kurallarının Given/When/Then kabul kriterleri olarak yazılması
- [ ] `module-obs` ile bağımlılık sözleşmesi taslağı (şube ve kayıt sorguları)

## Faz 2: Temel

- [ ] `CoursePage`: şube başına en fazla bir aktif sayfa
- [ ] `LearningMaterial` ve dosya servisi entegrasyonu
- [ ] Yalnızca kayıtlı öğrencinin şube içeriğini görmesi

## Faz 3: MVP LMS Akışları

- [ ] Haftalık izlence, duyuru, forum
- [ ] `Assignment`, `AssignmentSubmission`, geç teslim işaretleme
- [ ] `LiveSession`: `LiveClassroom` portu üzerinden, yalnızca yetkili akademisyenin başlatması
- [ ] Canlı ders sağlayıcısının seçilebilmesi: Jitsi (gömülü) veya BigBlueButton ([#4](https://github.com/Libre-University/module-lms/issues/4))
- [ ] Bildirim entegrasyonu (yeni materyal, ödev hatırlatma)

## Faz 4+

- [ ] Jitsi (Jibri) ve BigBlueButton kayıtlarının ortak modelle izlenceye eklenmesi
- [ ] Online sınav ve soru bankası
- [ ] Açık kaynak intihal denetimi entegrasyonu
