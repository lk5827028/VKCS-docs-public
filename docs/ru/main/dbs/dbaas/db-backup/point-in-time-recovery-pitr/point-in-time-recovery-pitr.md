Point-in-time-recovery (PITR) обеспечивает непрерывное резервное копирование данных таблицы PostgreSQL. Вы можете восстановить таблицу на определенный момент времени в процессе создания виртуальной машины или через интерфейс восстановления из резервной копии. В процессе восстановления на определенный момент времени сохраненная таблица восстанавливается в новую виртуальную машину.

**Важно**

Функция PITR доступна только для баз данных под управлением PostgreSQL.

PITR помогает защитить таблицы PostgreSQL от случайных операций записи или удаления. Благодаря восстановлению на определенный момент времени вам не нужно беспокоиться о создании, обслуживании или планировании резервного копирования по запросу. Например, тестовый сценарий случайно записывает данные в рабочую таблицу PostgreSQL. С помощью PITR вы можете восстановить эту таблицу на любой момент времени.

Подробнее о резервном копировании и восстановлении в PostgreSQL читайте [здесь](https://postgrespro.ru/docs/postgresql/9.6/continuous-archiving).

PITR в VK Cloud Solutions
-------------------------

Для инстанса или кластера PostgreSQL доступно PITR, если для него настроено расписание резервного копирования. Расписание можно настроить при создании инстанса или настроить позже. Обратитесь в техническую поддержку, если не получается настроить расписание на существующем инстансе. Расписание определяет регулярность создания резервных копий.

Для установки расписания нужно:

*   Название расписания;
    
*   Интервал резервного копирования (3, 4, 6, 8, 12, 24 часов);
    
*   Начало выполнения резервной копии (в API указывается в UTC);
    
*   Количество хранимых резервных копий.
    

Например, интервал — 3 часа, время начала —  01:30. Следовательно бэкапы будут выполняться в 01:30, 04:30, 07:30, 10:30, 13:30, 16:30, 19:30 и 22:30 каждые сутки.

Если интервал 24 часа, время начала — 05:07, тогда бэкапы будут выполняться каждые сутки в 05:07.

Время выполнения не точное, резервная копия начнет создаваться в интервале 5 минут от указанного времени.

Независимо от регулярных резервных копий будет также выполняться копирование журналов СУБД для возможности PITR. Управлять этим процессом нельзя.

### Настройка расписания резервного копирования

Расписание резервного копирования можно включить:

*   в процессе создания инстанса или кластера;
*   в настройках уже созданных инстанса или кластера.

#### Включение расписания резервного копирования при создании инстанса

Для того чтобы включить расписание резервного копирования при создании инстанса необходимо:

1.  В разделе «Резервное копирование», выберите опцию «По расписанию».
2.  В появившихся полях, введите время первого бэкапа и выберите интервал между последующими инкрементами.
3.  Нажмите «Следующий шаг» чтобы принять изменения.

#### Включение расписания резервного копирования для существующих инстансов

Для того чтобы включить расписание резервного копирования у существующих инстансов необходимо:

1.  На вкладке Резервное копирование или Бэкапы, нажмите «Добавить».
2.  На шаге «Создание инстанса», в разделе «Резервное копирование», выберите опцию «По расписанию».
3.  В появившихся полях, введите время первого бэкапа и выберите интервал между последующими инкрементами и выберите инстанс базы данных.
4.  Нажмите «Добавить план» чтобы принять изменения.

### Восстановление

Восстановить инстанс из резервной копии на определенный момент времени можно:

*   из списка бэкапов;
*   при создании инстанса.

#### Восстановление из списка бэкапов

Чтобы восстановить инстанс, выполните следующие шаги:

1.  Откройте раздел «Бэкапы» сервиса «Базы данных».
2.  Во вкладке «Бэкапы по расписанию» найдите бэкап план нужного инстанса и выберите бэкап на необходимый момент времени.
3.  В контекстном меню выбранного бэкапа нажмите «Восстановить из бэкапа».

#### Восстановление при создании инстанса

Чтобы создать новый инстанс из резервной копии на определенный момент времени, выполните следующие шаги:

1.  При создании инстанса, в разделе «Конфигурация», выберите опцию «Восстановление».
2.  В открывшемся окне, найдите список бэкапов нужного инстанса и выберите бэкап на необходимый момент времени.
3.  Нажмите «Следующий шаг», чтобы принять изменения и продолжить создание инстанса.