В индустрии используется GFS («дед-отец-сын», Grandfather-Father-Son) стратегия хранения бекапов.

В алгоритме дед-отец-сын резервное копирование состоит из трех последовательных шагов:

- «Дед» — полный бекап на начало года.
- «Отец» — полный бекап на начало месяца.
- «Сын» — полный бекап и инкременты раз в неделю.

## Принцип работы

После каждого успешного бекапа запускается процесс удаления устаревших бекапов. Стратегия бекапов GFS не создает отдельно недельные, месячные или годовые бекапы. Этот процесс динамический и зависит от текущих настроек GFS. Процесс удаления бекапов сначала проверяет, что есть необходимое количество недельных бекапов. Далее проверяет наличие/отсутствие месячных и годовых бекапов. После этого принимает решение на удаление устаревших/избыточных бекапов, если такие присутствуют.

Изменение настроек GFS, применяется при следующем успешном бекапе. Если указать хранить меньше каких-либо полных бекапов, чем хранится сейчас, то устаревшие бекапы будут удалены.

Настройки GFS хранят:

- Недельные бекапы — полные и инкрементальные бекапы за указанное количество недель.
- Месячные бекапы — остаются бекапы, созданные на начало месяца. Остаются только полные бекапы за указанное количество календарных месяцев. Инкрементальные бекапы удаляются.
- Годовые бекапы — остаются бекапы, созданные на начало года. Остаются только годовые бекапы за указанное количество лет (включая текущий календарный год). Инкрементальные бекапы удаляются.

## Сценарии использования

Типичным сценарием использования GFS является следование требованиям корпоративных политик или законодательства.

Наиболее часто используемым и рекомендуемым лучшими практиками являются следующие настройки.

- Хранить недельные бекапы: 4 недели.
- Хранить месячные бекапы: 12 месяцев.
- Хранить годовые бекапы: 5 лет.

## Ответы на самые частые вопросы

### Когда происходит «удаление»?

После первого успешного бекапа.

### Может ли быть один бекап одновременно Месячным и Недельным (или Годовым и Месячным)?

Нет. В текущей реализации GFS бекапы имеют уникальные теги «недельный», «месячный» или «годовой».

### Если сейчас 2023, как сохранить годовой бекап за 2022, это сколько Годовых?

Два. Текущий год тоже считается.

### Почему Недельный бекап обязательное поле?

Архитектурное требование. Это необходимо для правильной маркировки бекапов при применении политики хранения.
