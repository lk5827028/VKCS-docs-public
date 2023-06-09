Для создания базы данных следует перейти в [раздел личного кабинета "Аналитические БД"](https://mcs.mail.ru/app/services/analytic-databases/), выбрать версию лицензии «Arenadata DB» и нажать «Создать БД».

На следующем шаге выберите необходимый тип кластера, версию инстанса ArenadataDB и конфигурацию инстанса.

Конфигурация «Кластер» — это кластер с синхронной репликацией данных. Используется при наличии повышенных требований к надежности и отказоустойчивости системы.

На следующих шагах выберите необходимые параметры конфигурации:

| Название параметра | Описание |
|----------------------------|---------------------------------------------|
| Имя кластера | Оставьте имя по умолчанию или введите свое название латинскими символами.|
| Количество несжатых чистых данных | Максимальный объём БД. |
| Конфигурация узлов | Конфигурация мастера CPU / RAM / HDD (SSD).<br>Реплика/slave будет создана с аналогичной конфигурацией автоматически. |
| Использовать резервирование | Создание избыточных дублирующих узлов для обеспечения отказоустойчивости. |
| Подключить monitoring-узел ||
| Тип диска                  | Для лучшего быстродействия рекомендуем выбирать тип диска SSD или Hi-IOPS SSD.|
| Сеть                       | Оставьте по умолчанию или выберите свою приватную сеть.|
| Назначить внешний IP | Присвоить кластеру внешний IP для получения возможности подключения к кластеру из внешних сетей. |
| Зона доступности           | укажите зону доступности (рекомендуем DP1 или MS1).|

На следующем шаге задайте параметры инициализации базы данных:

| Название параметра | Описание |
|----------------------------|---------------------------------------------|
| Имя базы данных для создания | Можно оставить по умолчанию или ввести свое. |
| Имя пользователя | Нужно указать имя пользователя для удаленного доступа. |
| Пароль пользователя | Следует задать пароль пользователя для удаленного доступа. |

Инстанс создастся в течение нескольких минут. После этого появится информация об инстансе и способы подключения.
