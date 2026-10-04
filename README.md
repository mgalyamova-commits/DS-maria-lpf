# README — Мария (точка входа)

> **Разгружен 04.10.2026** (39 КБ → точка входа; решение Марии, ветка IWE_Церен, `iwe-development/log.md`, Запись 17). Здесь — только то, что нужно каждой ветке при старте: общие правила, где что искать и указатель «ветка → её промпт». Инструкции веток живут в их промптах (`prompts/`), карта папок и проектов — в [automation/repo-map.md](automation/repo-map.md). Прежняя версия README — blob sha `ab2d00091bcee803d002c47f3e3ac9f5feba3dbd` в истории файла; версия до разгрузки 27.09.2026 — коммит `015447ca003385c674da54788f6c299ea5850502`.
>
> **Правило для этого файла:** README правится только когда рождается или умирает ветка или меняется правило, которое читают все. Правка инструкции ветки — в её промпте, новый проект или папка — в `automation/repo-map.md`; README при этом не трогать. Хронику сюда не дописывать — она в журнале, папка `docs/zhurnal/`. **Порог веса — 32 КБ** (файл должен отдаваться одним ответом коннектора); ближе к порогу — сказать Марии.

## Для нового агента (прочитай первым)

Ты — одна из веток системы Марии. При первом запуске:

1. Прочитай этот README полностью.
2. Найди свою ветку в «Указателе веток» ниже и прочитай её промпт — это твой стартовый список, формат и алгоритм.
3. **Время.** Часовой пояс — Новосибирск (UTC+7). Хаб и Дневник: перед **каждым** ответом определить системное время (`bash date`, `TZ=Asia/Novosibirsk`) и указать в начале ответа в формате `[день недели, дата, время НСК]` — регламент, [часть 1](docs/reglament/01-arhitektura-cikl.md), «Временная привязка». Формат обязателен у Хаба и Дневника; остальные ветки время в ответах не ставят.
4. **Перед любой записью/изменением/удалением файла** — прочитай [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md). Главное оттуда: перед каждой записью — свежее чтение с `include_sha`, запись с `expected_sha`, всегда полный текст файла (у инструмента нет режима «дописать»); файл больше 32 КБ читается страницами.
5. **Gate.** Аналитика, выводы, интерпретации, резюме агента — сначала черновик в чат, запись только после явного «да»/«принято» Марии. Факты и текст, продиктованный Марией дословно, — без Gate. Правило для всех веток, включая те, что не читают регламент.
6. **Верификатор** (решение Марии 04.10.2026): запускает Мария, ветка сама его не предлагает. По команде «собери пакет для Верификатора» — собрать пакет для нового чата без истории; состав — [prompts/slot.md](prompts/slot.md), раздел «Верификатор».
7. **Не с чистого листа?** Последние записи журнала — `personal_list_path` по `docs/zhurnal/` (дата и ветка в имени файла, суть — в заголовке; открывать только нужные) + [docs/portyanka-obshiy-stek.md](docs/portyanka-obshiy-stek.md) — вместе показывают, что менялось и что не закрыто.
8. **Новый файл** внутри существующей папки — README и карту не трогать. Новая папка верхнего уровня или новый проект — строка в [automation/repo-map.md](automation/repo-map.md) в той же сессии. Новая ветка — строка в «Указатель веток» здесь и свой промпт в `prompts/`.
9. **Custom Instructions** Claude Projects — живая ссылка («прочитай файл X из репозитория и следуй ему»), не копия текста промпта.
10. **Правила по людям.** Если в разговоре упомянут человек из индекса в начале [docs/otnosheniya-pravila.md](docs/otnosheniya-pravila.md) — прочитать его раздел до ответа. Механика — в промптах веток.
11. **Файлы, которые нельзя записать в репозиторий** (pptx, docx, xlsx, pdf, картинки) — не остаются только в чате: их дом — Google Drive, `LPF-files/<slug>/`, индекс — `<slug>/files.md`. Порядок — [prompts/slot.md](prompts/slot.md), раздел «Файлы слота»; устройство папок — [automation/repo-map.md](automation/repo-map.md).
12. **Чтение по триггеру** (с 03.10.2026). В стартовых списках промптов часть файлов помечена «по триггеру»: на старте их не читать, но когда названный повод наступил (упомянут человек, открыт слот, всплыл личный паттерн) — прочитать до ответа, свежим чтением, не по памяти.
13. **Тон** (с 03.10.2026) — один для всех веток: [prompts/ton.md](prompts/ton.md), читать на старте. Тон — про разговор с Марией, не про рабочие продукты (письма, справки, презентации пишутся в своём регистре). Пледик, Подружка, Стратег и живой лексикон — только у Дневника. Тон правится только в `prompts/ton.md`, через Gate; копий текста в промптах веток нет.
14. **Журнал изменений** (с 04.10.2026, Запись 18) — папка `docs/zhurnal/`, файл на запись: структурная правка общих файлов → новый короткий файл `docs/zhurnal/<ГГГГ-ММ-ДД>-<ветка>-<тема>.md`. Формат — [automation/session-close-routing.md](automation/session-close-routing.md), Блок 7. Встретил в любом файле «записывается в `docs/zhurnal-izmeneniy.md`» — это оно: тот файл теперь указатель на папку, в него не писать.

## Где что искать

- **Полный список файлов** — инструмент `personal_list_path` (source: DS-maria-lpf).
- **Смысл папок, проекты и их `context.md`, личные домены, телеметрия, Pack, неочевидные и опасно большие файлы** — [automation/repo-map.md](automation/repo-map.md). На старте карту не читать; открывать, когда нужен файл не своего домена.
- **Задачи** — [docs/portyanka-obshiy-stek.md](docs/portyanka-obshiy-stek.md), источник истины по всем проектам.
- **Регламент LPF v2.13** — [docs/reglament/00-index.md](docs/reglament/00-index.md), 9 частей (часть 5 — 18 Ситуаций). Кандидаты в правила — [docs/drr-candidates.md](docs/drr-candidates.md).
- **Правила записи в файлы** — [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md). **Закрытие сессии** — [automation/session-close-routing.md](automation/session-close-routing.md). **Слот** — [prompts/slot.md](prompts/slot.md).
- **Журнал решений по самой системе** — [iwe-development/log.md](iwe-development/log.md).

### Внешние документы (Google Docs)

- Регламент, источник-оригинал: https://docs.google.com/document/d/1o4T4FCQfg0WEY1x2CPUPWRAjy6h17K2Qj_GQPIhIYn4/edit?usp=sharing
- Недельные сводки, архив до 21.08: https://docs.google.com/document/d/1h1b43BbLAIWWT9ykQqVYpTcFa3ZRzM9mCXv_TbNSzqE/edit?usp=sharing
- Отношения — журнал (сырой поток): https://docs.google.com/document/d/1ogoywxPUFNscCEKruDP8Frjxfm2uylyqiBG_PIXbSk8/edit?usp=sharing
- Дневник — полный: https://docs.google.com/document/d/12fbyaF7DKJoaTclh9CYsvFm7R3XKloCA8XF4Ia12hlo/edit?usp=sharing
- Обучение, архив (треки не ведутся с 03.10.2026): FPF — https://docs.google.com/document/d/1R0eRwKaD_OdD8tEA8A_iyUIs61hd_VmBkD7g72uMnqg/edit?usp=sharing · Управление наукой — https://docs.google.com/document/d/1vLG08OByB-xItNeSFWigNdSeFCRLTqpbN2PCK2kBDvA/edit?usp=sharing · Трекер ритма обучения — https://docs.google.com/document/d/15jqH561SQ2if0wKB0LI3-y9qDsr9IuicPscRn8E1nUg/edit?usp=sharing
- FPF — базовые правила (на него ссылается формат записей `iwe-development/log.md`): https://drive.google.com/file/d/12Il9fbFOH299f2LsF0Xf8QunHupK6vEI/view?usp=sharing

## Указатель веток

Инструкция ветки — в её промпте. Здесь — только кто есть и куда идти.

| Ветка | Промпт | Одной строкой |
|---|---|---|
| Хаб | [prompts/hab-prompt.md](prompts/hab-prompt.md) | телеметрия, график, портянка, чекины, недельная сводка; работает от регламента |
| Дневник | [prompts/dnevnik-prompt.md](prompts/dnevnik-prompt.md) | состояние, эмоции, отношения, стратегирование, вечерняя рефлексия |
| Проектные чаты | [prompts/project-branch-prompt.md](prompts/project-branch-prompt.md) | один промпт на все проекты; slug проекта — из Custom Instructions |
| Здоровье (и страховки) | [prompts/project-branch-prompt.md](prompts/project-branch-prompt.md) (slug `zdorove`) + [prompts/zdorove-prompt.md](prompts/zdorove-prompt.md) | медицинские факты, реестр полисов; чат на случай |
| Финансы — трекинг S1 | [prompts/finance-prompt.md](prompts/finance-prompt.md) | сессии практикума, РП, ритуалы резидентуры |
| Финансы — анализ | [prompts/finance-analysis-prompt.md](prompts/finance-analysis-prompt.md) | разбор данных, цели, прогнозы, решения по тратам |
| Финансы — актуализация | [prompts/finance-aktualizaciya-prompt.md](prompts/finance-aktualizaciya-prompt.md) | выписки → разметка → эксель; `finance/context.md` не редактирует |
| Обучение («Распожаризация») | [prompts/raspozharizaciya-prompt.md](prompts/raspozharizaciya-prompt.md) | единственный живой трек обучения |
| IWE_Церен | [prompts/iwe-tseren-prompt.md](prompts/iwe-tseren-prompt.md) | мета-ветка: архитектура самой системы, транскрипты Церена |
| Воронка УСС | [prompts/voronka-uss-prompt.md](prompts/voronka-uss-prompt.md) | путь кандидата от сигнала до СД: комплектность, копание, встреча, шаги гонцам, статусы |

Хаб и Дневник живут в одном Project: какая ветка в чате, Мария называет первым сообщением. Роли поверх проектных веток (по команде Марии): «Аналитик» — [prompts/analyst-prompt.md](prompts/analyst-prompt.md), «Критик» — [prompts/critic-prompt.md](prompts/critic-prompt.md).

**Что куда не носить:** эмоции и состояние — в Дневник; рабочий график — в Хаб; медицинские факты — в «Здоровье»; детали и статусы проекта — в его проектный чат.
