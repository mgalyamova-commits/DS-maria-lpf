# README — Мария (точка входа)

## Для нового агента (прочитай первым)

Ты — одна из веток системы Марии. При первом запуске:

1. Прочитай этот README полностью — здесь архитектура всех файлов.
2. Найди свою ветку в разделе «Инструкции для веток» ниже.
3. Прочитай промпт/регламент своей ветки — это твой формат, тон и алгоритм общения.
4. Часовой пояс: Новосибирск (UTC+7).
5. **Если твоя работа предполагает создание, изменение или удаление файлов репозитория** (не только чтение памяти) — обязательно прочитай [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md) перед первой такой операцией в сессии. Это отдельный от LPF-регламента слой: технические правила работы с инструментами и файлами репо, не про психологию пользователя.

## Дневник и система

- Дневник — полный: https://docs.google.com/document/d/12fbyaF7DKJoaTclh9CYsvFm7R3XKloCA8XF4Ia12hlo/edit?usp=sharing
- Локальная копия (телеметрия, извлечённая из дневника): [telemetry/history.md](telemetry/history.md) — количественная, и [telemetry/diary-2026-08.md](telemetry/diary-2026-08.md) — качественная («дневник-жилетка»: эмоциональные триггеры, паттерны).
- Портянка — общий стек: https://docs.google.com/document/d/1XIYibQrkKr6JaPnPV4WIVIU0So9_6CJjE66ALgkN8MQ/edit?usp=sharing
- Локальная копия в этом репозитории: [docs/portyanka-obshiy-stek.md](docs/portyanka-obshiy-stek.md)
- Журнал изменений: https://docs.google.com/document/d/1P5ptocDn25WRFzxRwICazdkscM3_AeFxVmzuLlbqENw/edit?usp=sharing
- Недельные сводки: https://docs.google.com/document/d/1h1b43BbLAIWWT9ykQqVYpTcFa3ZRzM9mCXv_TbNSzqE/edit?usp=sharing

## Отношения

- Отношения — журнал: https://docs.google.com/document/d/1ogoywxPUFNscCEKruDP8Frjxfm2uylyqiBG_PIXbSk8/edit?usp=sharing
- Отношения — правила: https://docs.google.com/document/d/162aGilVGIerCuCGZ-lQDeIEtaiCfh2UzM-bbg2fu2W0/edit?usp=sharing
- Локальная копия в этом репозитории: [docs/otnosheniya-pravila.md](docs/otnosheniya-pravila.md)

## Обучение (сводные)

- FPF: https://docs.google.com/document/d/1R0eRwKaD_OdD8tEA8A_iyUIs61hd_VmBkD7g72uMnqg/edit?usp=sharing
- Управление наукой: https://docs.google.com/document/d/1vLG08OByB-xItNeSFWigNdSeFCRLTqpbN2PCK2kBDvA/edit?usp=sharing
- Распожаризация: https://docs.google.com/document/d/1Pt2jb2IK24_5ha-b8GPvtS7vSeBNV5vmKjVo9ynIwAI/edit?usp=sharing
- IWE / Экзокортекс: https://docs.google.com/document/d/1GxLtviWkBs1-Vqz4aUQkx5vIy91Hsej5nuShSqGsnA4/edit?usp=sharing

## Регламент

- LPF-регламент v2.6: https://docs.google.com/document/d/1o4T4FCQfg0WEY1x2CPUPWRAjy6h17K2Qj_GQPIhIYn4/edit?usp=sharing
- Локальная копия в этом репозитории: [docs/lpf-reglament-v2.5.md](docs/lpf-reglament-v2.5.md) (путь файла не менялся с версии 2.5, содержимое внутри обновлено до v2.6)

## Промпты веток

- Дневник (Жилетка / Друг с битой / Пледик): [prompts/dnevnik-prompt.md](prompts/dnevnik-prompt.md) — локальная копия, источник Google Docs: https://docs.google.com/document/d/1uhe0DLEdSUQEARvXzrpvEOYtYQ6-p1AT7M7R8mii4R0/edit
- Хаб: отдельного промпта нет, работает напрямую от LPF-регламента.

## Технический слой (для агентов, работающих с файлами репо)

- [automation/agent-workflow-rules.md](automation/agent-workflow-rules.md) — операционные правила работы с файлами и инструментами репозитория. Отдельно от LPF-регламента (тот — про психологию Марии) и от промптов веток (те — про тон и формат общения). Читать перед любой записью/удалением файла.
- [automation/repo-map.md](automation/repo-map.md) — манифест структуры репозитория («что где лежит»), без правил поведения.

## Инструкции для веток

### Хаб (основной чат)
- LPF-регламент v2.6: [docs/lpf-reglament-v2.5.md](docs/lpf-reglament-v2.5.md)
- При запуске: прочитай README, затем LPF-регламент.
- Твои задачи: телеметрия, рабочий график, портянка, чекины, команды агенту.

### Дневник (Жилетка / Друг с битой / Пледик)
- Промпт: [prompts/dnevnik-prompt.md](prompts/dnevnik-prompt.md)
- При запуске: прочитай README, затем LPF-регламент (раздел «Правила несмешивания» и «Episteme-карточки»), потом промпт по ссылке выше. Это твой формат, тон, лексикон и алгоритм общения. Затем запроси у Марии телеметрию (сон, энергия, ёмкость, контекст дня, было ли отключение Дневника из-за технических проблем и когда).
- Сюда идут: состояние, эмоции, жалобы, отношения.
- Сюда НЕ идут: статусы задач, детали проектов, рабочий график.

### Проектные чаты (Мотоферма, Химозин, ЦПИ, Хелснет, Тандем, ГПБ/МБС, OpenBio и др.)
- При запуске: прочитай README, затем LPF-регламент (раздел «Правила несмешивания»).
- Сюда идут: детали и статусы задач проекта.
- Сюда НЕ идут: эмоции → в Дневник.

### Треки обучения (FPF, Управление наукой, Распожаризация, IWE/Экзокортекс)
- При запуске: прочитай README, затем сводную заметку своего трека (см. раздел «Обучение (сводные)» выше).
- Сюда идут: учебный материал, конспекты, вопросы по теме.
- Сюда НЕ идут: рабочие задачи → в проектные чаты.

## FPF

- FPF-базовые_правила: https://drive.google.com/file/d/12Il9fbFOH299f2LsF0Xf8QunHupK6vEI/view?usp=sharing

## Трекеры

- Трекер ритма обучения: https://docs.google.com/document/d/15jqH561SQ2if0wKB0LI3-y9qDsr9IuicPscRn8E1nUg/edit?usp=sharing
