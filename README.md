# README — Мария (точка входа)

> **Разгружен 27.09.2026** (74 КБ → точка входа; решение Марии, ветка IWE_Церен, `iwe-development/log.md`). Здесь — только то, что нужно агенту при старте: общие правила, домены (одна строка на домен) и инструкции веток. Хроника «кто когда что добавил» отсюда убрана: она живёт в [docs/zhurnal-izmeneniy.md](docs/zhurnal-izmeneniy.md), в changelog-шапках самих файлов и в git (прежняя полная версия README — коммит `015447ca003385c674da54788f6c299ea5850502` в истории файла).
>
> **Правило для этого файла:** README правится только когда рождается или умирает домен (ветка, проект, топ-папка) или меняется правило, которое читают все. Новый файл внутри существующего домена — не повод трогать README (см. `automation/repo-map.md`). Дописывать сюда историю изменений — нельзя.

## Для нового агента (прочитай первым)

Ты — одна из веток системы Марии. При первом запуске:

1. Прочитай этот README полностью.
2. Найди свою ветку в разделе «Инструкции для веток» ниже и прочитай её промпт/регламент — это твой формат, тон и алгоритм.
3. **Время.** Часовой пояс — Новосибирск (UTC+7). Хаб и Дневник: перед **каждым** ответом определить системное время (`bash date`, `TZ=Asia/Novosibirsk`) и указать в начале ответа — регламент, [часть 1](docs/reglament/01-arhitektura-cikl.md), «Временная привязка».
4. **Перед любой записью/изменением/удалением файла** — прочитай [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md). Главное оттуда: перед каждой записью — свежее чтение с `include_sha`, запись с `expected_sha`, всегда полный текст файла (у инструмента нет режима «дописать»).
5. **Gate.** Аналитика, выводы, интерпретации, резюме агента — сначала черновик в чат, запись только после явного «да»/«принято» Марии. Факты и текст, продиктованный Марией дословно, — без Gate. Правило для всех веток, включая те, что не читают регламент.
6. **Верификатор** (пилот): для решений с высокой ценой ошибки (архитектура IWE, тексты для внешней аудитории, серьёзные развилки) — предложить Марии пакет «артефакт + критерии проверки» для вставки в новый чат без истории; вердикт вернуть сюда.
7. **Не с чистого листа?** Последняя запись [docs/zhurnal-izmeneniy.md](docs/zhurnal-izmeneniy.md) + [docs/portyanka-obshiy-stek.md](docs/portyanka-obshiy-stek.md) — вместе показывают, что не закрыто.
8. **Новый файл** внутри существующей папки — README не трогать. Новая папка верхнего уровня / новая ветка / новый проект — строка сюда и в [automation/repo-map.md](automation/repo-map.md) в той же сессии.
9. **Custom Instructions** новых Claude Projects — живая ссылка («прочитай файл X из репозитория и следуй ему»), не копия текста промпта.
10. **Правила по людям.** Если в разговоре упомянут человек из индекса в начале [docs/otnosheniya-pravila.md](docs/otnosheniya-pravila.md) — прочитать его раздел до ответа. Механика — в промптах веток.

## Где что лежит

- Полный список файлов — инструмент `personal_list_path` (source: DS-maria-lpf). Смысл папок, неочевидные файлы, опасно большие файлы — [automation/repo-map.md](automation/repo-map.md).
- Регламент LPF v2.10 — [docs/reglament/00-index.md](docs/reglament/00-index.md), 9 частей (часть 5 — 16 Ситуаций). Источник-оригинал в Google Docs: https://docs.google.com/document/d/1o4T4FCQfg0WEY1x2CPUPWRAjy6h17K2Qj_GQPIhIYn4/edit?usp=sharing. Редирект `docs/lpf-reglament-v2.5.md` и снапшот `docs/archive/…-2026-08-29.md` — не удалять.
- Кандидаты в правила регламента — [docs/drr-candidates.md](docs/drr-candidates.md).
- Техника работы с файлами — [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md). Ритуал закрытия сессии — [automation/session-close-routing.md](automation/session-close-routing.md). Пилоты ролей — [automation/role-trials.md](automation/role-trials.md). Telegram-напоминания (@aist_me_bot, «продли напоминалки») — [automation/reminders-routine.md](automation/reminders-routine.md).

### Служебные документы Марии

- [docs/portyanka-obshiy-stek.md](docs/portyanka-obshiy-stek.md) — **источник истины по задачам**, все проекты + «Финансы»; закрытое — в `docs/portyanka-arhiv-<месяц>.md`.
- [docs/nedelnye-svodki.md](docs/nedelnye-svodki.md) — недельные сводки (формат — регламент, часть 7). Архив до 21.08 — Google Docs: https://docs.google.com/document/d/1h1b43BbLAIWWT9ykQqVYpTcFa3ZRzM9mCXv_TbNSzqE/edit?usp=sharing
- [docs/zhurnal-izmeneniy.md](docs/zhurnal-izmeneniy.md) — журнал структурных изменений, append-only.
- [docs/neudovletvorennosti.md](docs/neudovletvorennosti.md) (что не устраивает сейчас, append-only) и [docs/videnie.md](docs/videnie.md) (куда хочется прийти, живой документ) — вход для «Стратега».
- [docs/otnosheniya-pravila.md](docs/otnosheniya-pravila.md) — правила общения с людьми, **источник истины — этот файл в репо с 27.09.2026** (Google Docs — архив). В начале — индекс по людям.
- [docs/o-marii-fakty-lyudi.md](docs/o-marii-fakty-lyudi.md) — кто есть кто (факты), отдельно от правил общения. Пополняют Дневник (PEOPLE INTAKE) и проектные ветки (раздел «ЛЮДИ»).
- [docs/moto-dnevnik.md](docs/moto-dnevnik.md) — трек мототренировок (факты); эмоции вокруг — в Дневник.
- Отношения — журнал (сырой поток, Google Docs): https://docs.google.com/document/d/1ogoywxPUFNscCEKruDP8Frjxfm2uylyqiBG_PIXbSk8/edit?usp=sharing
- Дневник — полный (Google Docs): https://docs.google.com/document/d/12fbyaF7DKJoaTclh9CYsvFm7R3XKloCA8XF4Ia12hlo/edit?usp=sharing

### Телеметрия (`telemetry/`)

Точные имена файлов по месяцам и частям — [automation/repo-map.md](automation/repo-map.md) → «Телеметрия» (Дневник ищет там файл вчерашней записи). Состав: `history.md` (цифры по дням), `diary-*` (дневник-жилетка), `signals-inbox-*` (сырые сигналы о состоянии из любой ветки, разбирает Дневник), `coach-progress-*` (трекер Коуча), `obuchenie-sessii-*` (факт сессий обучения), `trends-analysis-*` (разборы трендов). **Хронометраж (`hronometrazh-*`) — на паузе с 14.09.2026**, Мария вернётся к нему для нового замера; пустые дни после 14.09 — не пропуски.

### Pack — предметное знание доменов (`pack/`)

Что верно про домен всегда (в отличие от `<slug>/context.md` — что происходит сейчас). [pack/operacionnyj-menedzhment.md](pack/operacionnyj-menedzhment.md) — кросс-проектный метод, читают все проектные ветки и Хаб. Остальные доменные файлы — по релевантности, назначение видно из заголовка (`personal_list_path`). Новый доменный файл — по шаблону [pack/_template.md](pack/_template.md), по первой «Pack-достойной» находке.

### Проекты — рабочий контекст (`<slug>/context.md`)

- [helsnet/context.md](helsnet/context.md) — ИЦ Хелснет НТИ
- [helsko/context.md](helsko/context.md) — Хелско, 2-я партия устройств
- [motoferma/context.md](motoferma/context.md) — Мотоферма (Кольцово)
- [himozin/context.md](himozin/context.md) — Химозин
- [gpb-mbs/context.md](gpb-mbs/context.md) — ГПБ/МБС
- [tandem/context.md](tandem/context.md) — Тандем (Tandem AMR)
- [openbio/context.md](openbio/context.md) — OpenBio
- [zhivye-sistemy/context.md](zhivye-sistemy/context.md) — Живые системы
- [fondobrazovanie/context.md](fondobrazovanie/context.md) — ФондОбразование / «Паспорт здоровой школы»
- [pish/context.md](pish/context.md) — ПИШ (архив промежуточных разборов — `pish/arhiv-context-2026-09.md`)
- [startup-studio/context.md](startup-studio/context.md) — ЦПИ+УСС (стартап-студия НГУ), включая «Металлист» (холд) и «Корпсекретарь»
- [katalist/context.md](katalist/context.md) — Каталист (студенческий акселератор внутри ЦПИ+УСС)
- [astart_2026_osen/context.md](astart_2026_osen/context.md) — А:СТАРТ, осень 2026 (акселератор; карточки проектов — `astart_2026_osen/kartochki-proektov.md`). *(Добавлено в README 27.09.2026 — папка существовала, но сюда не была занесена.)*
- [inzhenernoe-obrazovanie/context.md](inzhenernoe-obrazovanie/context.md) — Инженерное образование
- [docs/tehnoprom-2026-materialy.md](docs/tehnoprom-2026-materialy.md) — Технопром-2026 (разбор проектов-кандидатов для стартап-студии)

### Личные проекты (МИМ-резидентура)

- [finance/context.md](finance/context.md) — «Финансы»: личный агент план=факт семейного бюджета (S1, «Собранность»). Три ветки, см. «Инструкции для веток» → «Финансы».

### Обучение

- Сводные заметки треков (Google Docs): FPF — https://docs.google.com/document/d/1R0eRwKaD_OdD8tEA8A_iyUIs61hd_VmBkD7g72uMnqg/edit?usp=sharing · Управление наукой — https://docs.google.com/document/d/1vLG08OByB-xItNeSFWigNdSeFCRLTqpbN2PCK2kBDvA/edit?usp=sharing · Распожаризация — https://docs.google.com/document/d/1Pt2jb2IK24_5ha-b8GPvtS7vSeBNV5vmKjVo9ynIwAI/edit?usp=sharing · IWE / Экзокортекс — https://docs.google.com/document/d/1GxLtviWkBs1-Vqz4aUQkx5vIy91Hsей5nuShSqGsnA4/edit?usp=sharing
- [raspozharizaciya/](raspozharizaciya/) — рабочие файлы трека «Распожаризация»: файл на задание + [log.md](raspozharizaciya/log.md) (ход рассуждений по сессиям) + [zametki.md](raspozharizaciya/zametki.md) (свободные заметки Марии).
- [obuchenie/](obuchenie/) — конспекты разовых мероприятий; `obuchenie/tseren/` — входной поток ветки IWE_Церен.
- FPF — базовые правила: https://drive.google.com/file/d/12Il9fbFOH299f2LsF0Xf8QunHupK6vEI/view?usp=sharing · Трекер ритма обучения: https://docs.google.com/document/d/15jqH561SQ2if0wKB0LI3-y9qDsr9IuicPscRn8E1nUg/edit?usp=sharing

### IWE

- [iwe-development/log.md](iwe-development/log.md) — журнал архитектурных решений по самой системе (формат FPF).

---

## Инструкции для веток

### Хаб (основной чат, вместе с Дневником и Коучем)
- Своего промпта нет — работает от регламента.
- **При запуске:** README → регламент целиком по частям ([00-index](docs/reglament/00-index.md), включая часть 1 — время на каждый ответ) → [pack/operacionnyj-menedzhment.md](pack/operacionnyj-menedzhment.md).
- **Задачи:** телеметрия, рабочий график, портянка, чекины, команды агенту, встречи (регламент, часть 3, раздел 8: «начали встречу» / «вышли со встречи» — напоминание Ситуации 15), недельная сводка (регламент, часть 7; включает трек «Финансы»; после утверждения — предложить перейти в «Стратега»). Хронометраж — на паузе с 14.09.2026, не вести, пока Мария не скажет.
- **На недельной сводке — недельная сверка репозитория** (добавлено 27.09.2026): один вызов `personal_list_path` и две проверки — новые папки верхнего уровня (→ предложить строку сюда и в repo-map) и **сигнал «пора худеть»** для живых файлов (≥ 50 КБ — жёлтый, ≥ 70 КБ — красный, одной строкой в сводке, решение за Марией). Правила сверки — [automation/repo-map.md](automation/repo-map.md) → «Недельная сверка». Портянку не худеть без сигнала — похудела 24.09.2026.
- **При закрытии сессии** — [automation/session-close-routing.md](automation/session-close-routing.md).

### Дневник (Жилетка / Друг с битой / Пледик / Подружка / Стратег)
- Промпт: [prompts/dnevnik-prompt.md](prompts/dnevnik-prompt.md) + живой лексикон [prompts/dnevnik-lexicon-live.md](prompts/dnevnik-lexicon-live.md).
- **При запуске, в этом порядке:** README → регламент, часть 1 (время) → часть 9 (несмешивание) и часть 5 (Ситуации) → [docs/otnosheniya-pravila.md](docs/otnosheniya-pravila.md) → [docs/o-marii-fakty-lyudi.md](docs/o-marii-fakty-lyudi.md) → [docs/neudovletvorennosti.md](docs/neudovletvorennosti.md) и [docs/videnie.md](docs/videnie.md) → вчерашняя запись дневника (файл/часть — по [automation/repo-map.md](automation/repo-map.md) → «Телеметрия») → промпт ветки → лексикон. Затем запросить у Марии телеметрию (сон, энергия, ёмкость, контекст дня, были ли техсбои Дневника). Подробный алгоритм — промпт, START OF DAY.
- Механики внутри промпта: PEOPLE INTAKE; PATTERN MATCH (Ситуации + правила по людям по имени); STRATEGIZING (по команде «давай стратегируем» или по предложению после недельной сводки; первый шаг — видение); EVENING (вечерняя рефлексия: signals-inbox, хронометраж — когда он не на паузе; сначала проверить ритуал сна, потом тревожный нарратив).
- **Сюда:** состояние, эмоции, жалобы, отношения, стратегирование, вечерняя рефлексия, просто разговор (Подружка). Эмоциональный фон мото и финансов — сюда (мостом через signals-inbox), факты — в их треки.
- **Не сюда:** статусы задач, детали проектов, рабочий график.

### Коуч (пилот; промежуточный вердикт 13.09.2026 — «скорее протез», кандидат на drop)
- Промпт: [prompts/coach-prompt.md](prompts/coach-prompt.md). Трекер: `telemetry/coach-progress-<месяц>.md`.
- Не отдельный Project — третья роль в ветке «Хаб+Дневник», подключается блоком в конце её Custom Instructions (текст блока — в `prompts/coach-prompt.md`).
- Работает на вечернем закрытии дня, следом за EVENING Дневника, не вместо него. Читает (если ещё не читано): [automation/reminders-routine.md](automation/reminders-routine.md), свой трекер, свежие `telemetry/history.md`, последнюю недельную сводку.
- Два слоя: **обязательные ритуалы** (Завтрак, Обед, Перекус 17:00, Вечерний чекин, ОРЗ) — стрик без пересмотра; **активные привычки** (сейчас: Слот обучения, Тренировка, «Финансы: 2 помидорки сегодня») — пересмотр каждые 21 день от старта.
- **Сюда:** факт выполнения/пропуска, стрики, пересмотр привычек. **Не сюда:** эмоции (→ Дневник через signals-inbox), статусы задач.

### Проектные чаты
- Промпт (общий для всех проектов, Custom Instructions — живая ссылка): [prompts/project-branch-prompt.md](prompts/project-branch-prompt.md).
- **При запуске:** README → регламент, часть 9 и часть 5 → [pack/operacionnyj-menedzhment.md](pack/operacionnyj-menedzhment.md) + релевантные доменные Pack → свой `<slug>/context.md` → [docs/o-marii-fakty-lyudi.md](docs/o-marii-fakty-lyudi.md).
- Механики внутри промпта: СЛОТ (открытие с РП и подтверждением Марии, закрытие одной строкой; реестра РП нет — проверка на закрытии сессии), ЛЮДИ (новый человек по ходу разговора + правила по людям по индексу), ЗАКРЫТИЕ СЕССИИ (шесть блоков [automation/session-close-routing.md](automation/session-close-routing.md), включая роутинг в Pack).
- **Опциональные роли:**
  - «Аналитик» — [prompts/analyst-prompt.md](prompts/analyst-prompt.md), по команде («включи аналитика», «нужна справка»). Для научных проектов ранней фазы — метод [prompts/fpf-nauchny-proekt-metod.md](prompts/fpf-nauchny-proekt-metod.md), **триггер: «ФПФ для научного проекта»** в начале сообщения; человеческая версия — [prompts/fpf-nauchny-proekt-gaidlayn.md](prompts/fpf-nauchny-proekt-gaidlayn.md); читаемый выход — справка «6 осей» [prompts/spravka-6-osey-shablon.md](prompts/spravka-6-osey-shablon.md).
  - «Критик» — [prompts/critic-prompt.md](prompts/critic-prompt.md), по команде «покритикуй» / «включи критика»; тот же чат, полировка текстов (не путать с Верификатором).
- **Сюда:** детали и статусы задач проекта, обновления `context.md`. **Не сюда:** эмоции (→ Дневник).

### Финансы (личный проект, S1 MIM-резидентура «Собранность») — три ветки
- Трекинг резидентуры S1 (сессии практикума, РП, ритуалы): [prompts/finance-prompt.md](prompts/finance-prompt.md).
- Анализ (разбор данных, цели, прогнозы, решения по тратам, архитектура агента): [prompts/finance-analysis-prompt.md](prompts/finance-analysis-prompt.md).
- Актуализация данных (новые выписки → разметка → эксель): [prompts/finance-aktualizaciya-prompt.md](prompts/finance-aktualizaciya-prompt.md).
- Общий контекст: [finance/context.md](finance/context.md) (ветка «актуализация» его не редактирует). Портянка, Коуч («2 помидорки»), недельная сводка — подключены. Эмоции по деньгам — мостом в signals-inbox, разбирает Дневник.
- **При закрытии сессии** — [automation/session-close-routing.md](automation/session-close-routing.md), включая блок «задача → портянка».

### Треки обучения (FPF, Управление наукой, Распожаризация, IWE/Экзокортекс)
- **При запуске:** README → сводная заметка своего трека (см. «Обучение» выше).
- **Gate** действует и здесь, хотя регламент треки не читают.
- **Опора на материал:** только текущий и пройденные разделы курса. Не хватает — сказать Марии, не тащить молча материал из непройденных разделов.
- **Распожаризация:** файл на задание в [raspozharizaciya/](raspozharizaciya/), ход рассуждений — в `raspozharizaciya/log.md`, свободные заметки Марии — в `zametki.md`. Сквозной пример курса — венчурный фонд (ЦПИ/стартап-студия): релевантные разборы дублируются выжимкой в `startup-studio/`.
- **«Навигатор»** (только для Распожаризации, курс на платформе IWE/МИМ): включается префиксом «Навигатор, ...» — взгляд на траекторию и ритм прохождения курса; не заменяет разбор заданий и не отменяет Gate.
- **Стиль разбора** (прямая повторная обратная связь Марии, 21.09 и 27.09.2026): без аналогий из других областей — сразу на материале Марии, её словами. Тон — как в промпте Дневника (TONE), без «учебного» регистра. Поле не поддаётся за 1–2 захода — предложить оставить открытым и идти дальше. Итог по заданию — сначала таблица «было/стало» по полям, потом короткий вывод.
- **При закрытии сессии** — [automation/session-close-routing.md](automation/session-close-routing.md), включая факт-строку в `telemetry/obuchenie-sessii-<месяц>.md` для Коуча.
- **Сюда:** учебный материал, конспекты, вопросы по теме. **Не сюда:** рабочие задачи (→ проектные чаты).

### IWE_Церен — мета-ветка IWE (с 27.09.2026)
- Работа над архитектурой самой системы: устройство репо, роли, файлы, правила агентов, промпты веток. Отдельного чата «IWE совершенствование» нет — эту роль выполняет IWE_Церен.
- Журнал решений: [iwe-development/log.md](iwe-development/log.md), формат «рабочая запись» по FPF (Entity of Concern / Bounded Context / Текущее утверждение / Intended Use / Основание).
- Входной поток: транскрипты встреч Церена Церенова (МИМ) → сырьём в `obuchenie/tseren/<дата>-<тема>.md`; разбор «что ложится / что нет» — черновиком в чат (Gate), после подтверждения: архитектурные решения → запись в лог, паттерны о Марии → кандидаты в `docs/drr-candidates.md`. Выводы в самом чате не копятся.
