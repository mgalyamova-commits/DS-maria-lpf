# Здоровье — индекс документов на Google Drive

> Индекс медицинских документов Марии: анализы, заключения, выписки, снимки, назначения. Сами файлы — на Google Drive, папка `LPF-files/zdorove/` (id `1IOQ9P6NbOOHSoMZPeKPyGcrO2Nh21EeZ`), внутри — подпапки по годам (`2024/`, `2025/`, `2026/` …; ветка создаёт подпапку года при первом документе этого года). В репозиторий документы не пишутся — только эта таблица и выжимка в `istoriya.md` / `analizy.md` / `karta.md`.
>
> Создан 03.10.2026 (`iwe-development/log.md`, Запись 12). Общий порядок работы с файлами — `prompts/slot.md`, раздел «Файлы слота»; отличие этого домена — подпапки по годам и тип документа в имени.
>
> **Имя файла на Drive:** `<ГГГГ-ММ-ДД>-<тип>-<что>.<расширение>`, дата — дата документа (не дата загрузки). Тип: `analiz`, `zaklyuchenie`, `vypiska`, `snimok`, `naznachenie`, `spravka`. Пример: `2026-09-28-snimok-mrt-plecho.pdf`. Дата в документе не читается — `0000-00-00` не ставить: спросить Марию.
>
> **Как документ попадает сюда.** Мария кидает файл (или весь архив разом, с любыми именами) в `LPF-files/_vhod`. Ветка «Здоровье» разбирает пачками по 10–15 документов: читает, определяет дату, тип, врача или лабораторию → таблица в чат → после «да» Марии переименовывает, переносит в папку года, ставит строку сюда и выжимку в нужный файл домена. Скан или фото не читается с Drive — попросить Марию загрузить этот документ прямо в чат. Снимки МРТ/КТ (диски, DICOM) агент не читает: хранится файл, в индекс идёт заключение к нему.
>
> **Колонка «Выжимка»** — куда ушла суть документа: `istoriya` / `analizy` / `karta` / `context` / «нет» (только хранится).
>
> **Подпапки по годам** (id папок на Drive): `2026/` — `1MnjikIJdae82Q_c_hjGtQmW_Xps9c1L4`; `2024/` — `1ybFjA1BX41ZGL7T2BQMqKB6VL2WJ3bnr`; `2023/` — `1Uv1ZeRYF-cv3QxqJ-xfY1-UZ03HvGTAu`; `2021/` — `15CfoRyDRtfhDMHuCt8UazeUd2_AEjzNL`; `2015/` — `1qwft3vanVUGPgbdPxDzAczNV3izzqA7R`; `2011/` — `1D6KWO1_LnqyDaGSPiUQA-_T6wUqM2r6B` (все созданы 03.10.2026).
>
> **Разбор архива ЦНМТ** (начат 03.10.2026): в `_vhod` лежало 54 файла `cnmt-result-*.pdf`; строки ниже — от новых к старым. Пачка 1 (13 документов, 2011 — февраль 2024) разнесена 03.10.2026.

| Дата документа | Имя файла | Тип | Что это, одной строкой | Врач / клиника / лаборатория | Ссылка на Drive | Выжимка |
|---|---|---|---|---|---|---|
| 02.10.2026 | `2026-10-02-zaklyuchenie-travmatolog-plecho.pdf` | zaklyuchenie | Консультация травматолога-ортопеда по травме левого плеча: диагноз, ограничения, лекарства, направление к физиотерапевту | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1Am_7FeMi-eOFJNuxyesM6BTVuMJX_PCz/view | context |
| 26.02.2024 | `2024-02-26-zaklyuchenie-terapevt-davlenie.pdf` | zaklyuchenie | Приём терапевта: диагнозы под вопросом (I10, K21.9), план обследования | Малов А. С., терапевт, ЦНМТ | https://drive.google.com/file/d/1HrkyAdmTlj2-AJnQZFhW_qI0z5diN6TY/view | istoriya |
| 20.02.2024 | `2024-02-20-zaklyuchenie-travmatolog-koleno.pdf` | zaklyuchenie | Правое колено: 3-я процедура УВТ, ортез, Мукосат | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1MI-f8OIgJwh-YT9sussmcnTxnfPimN5b/view | istoriya |
| 13.02.2024 | `2024-02-13-zaklyuchenie-travmatolog-koleno.pdf` | zaklyuchenie | Правое колено: 2-я процедура УВТ, 2-я пункция с гиалуронатом | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1gwGthWkluILzAsMzCt8_R2EX0atvxzjZ/view | istoriya |
| 06.02.2024 | `2024-02-06-zaklyuchenie-travmatolog-koleno.pdf` | zaklyuchenie | Правое колено: 1-я процедура УВТ, 1-я пункция с гиалуронатом | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1nFpu1kBm1yJ5B4VarDdUUGVE9UBMitsY/view | istoriya |
| 10.01.2024 | `2024-01-10-zaklyuchenie-travmatolog-koleno.pdf` | zaklyuchenie | Правое колено: диагноз по МРТ 05.01.24, план лечения (тутор, ортез, лекарства, гиалуронат, УВТ) | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1jQnKmxAzcVrWvVeJsQNM284HCbJXjy8O/view | istoriya, karta |
| 03.01.2024 | `2024-01-03-zaklyuchenie-travmatolog-koleno.pdf` | zaklyuchenie | Правое колено: первичный приём, направление на МРТ | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/19c7Oi3tObjNpWnnX_IjB6gqmWLAOtehj/view | istoriya |
| 04.10.2023 | `2023-10-04-snimok-rentgen-grudnaya-kletka.pdf` | snimok | Протокол рентгенографии грудной клетки и рёбер слева | Нагель Ю. А., ЦНМТ | https://drive.google.com/file/d/1Vrbgqjj3Lh0coqCIrec0OVdKVAFCJne9/view | istoriya |
| 04.10.2023 | `2023-10-04-zaklyuchenie-travmatolog-ushib-grudnoy-kletki.pdf` | zaklyuchenie | Приём травматолога: ушиб грудной клетки, назначения | Шкуратов О. В., ЦНМТ | https://drive.google.com/file/d/1XMApkfo_dQx7mG_kmk72621wyTh4jvCS/view | istoriya |
| 03.10.2023 | `2023-10-03-zaklyuchenie-uzi-bryushnaya-polost.pdf` | zaklyuchenie | УЗИ органов брюшной полости после падения | Малышева М. В., врач УЗД, ЦНМТ | https://drive.google.com/file/d/1VclU2_X0r0gxNKUD7lgTxoF_-s6Fj78I/view | istoriya, karta |
| 22.05.2021 | `2021-05-22-analiz-pcr-covid.pdf` | analiz | ПЦР на COVID-19 | лаборатория ЦНМТ | https://drive.google.com/file/d/1XVjKMw6iqk33hKG7Y6kHMfyehwneFE1Y/view | analizy |
| 12.12.2015 | `2015-12-12-zaklyuchenie-terapevt-tonzillit.pdf` | zaklyuchenie | Приём терапевта: хронический тонзиллит, обострение; назначения | Субботина О. А., терапевт, ЦНМТ | https://drive.google.com/file/d/1F_obzKJdvTZVBEQeyi2GlwD1fK2uD_1s/view | istoriya, karta |
| 28.05.2011 | `2011-05-28-zaklyuchenie-ginekolog.pdf` | zaklyuchenie | Консультация акушера-гинеколога | Попова Ж. Ю., ЦНМТ | https://drive.google.com/file/d/1pXDwwgjiX6PBBYxWa3sNRrwZXBVW54DC/view | istoriya |
| 23.05.2011 | `2011-05-23-zaklyuchenie-ginekolog.pdf` | zaklyuchenie | Консультация акушера-гинеколога | Попова Ж. Ю., ЦНМТ | https://drive.google.com/file/d/1hmjVZ5dg1U8bJ5JPXEP3Ykm18G4kSlNW/view | istoriya |
