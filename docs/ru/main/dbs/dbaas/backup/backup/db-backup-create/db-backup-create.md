При создании базы данных в панели VK Cloud создается план резервного копирования, которым можно управлять в разделе [«Бэкапы»](https://mcs.mail.ru/app/services/databases/backups/) панели управления.

Текущий статус плана можно увидеть при наведении мыши на цветной индикатор статуса.

### Настройка плана

1.  Перейдите в раздел «Базы данных» → «Бэкапы».
2.  Выберите нужный план и нажмите «Изменить».
3.  В появившемся окне можно настроить периодичность выполнения резервного копирования. Возможно комбинирование нескольких расписаний, например, раз в сутки по выбранным дням и каждые три часа с различным интервалом хранения копий.
4.  Для применения изменений нажмите кнопку «Сохранить».

<warn>

В случае изменения параметра «Макс. количество полных бэкапов», удаление лишних резервных копий происходит через 1 час после сохранения изменений.

</warn>

### Остановка плана

Если по каким-то причинам требуется остановить создание резервных копий - выделите нужный план и нажмите на кнопку «Остановить».  Создание бэкапов будет приостановлено до активации плана вручную.

<info>

Изменение расписания резервного копирования активирует план.

</info>

### Остановка резервного копирования

Для остановки создания резервной копии инстанса, в раздере «Резервное копирование» выделите активный бэкап и нажмите «Остановить». Создание бэкапа будет остановлено, а записанные до момента остановки файлы удалены.

### Удаление плана

В случае, если оригинальный инстанс удален, возможно удалить и план резервного копирования для инстанса. Следует выделить необходимый план галочкой и нажать на кнопку «Удалить».

<warn>

При удалении плана резервного копирования будут удалены все точки восстановления.

</warn>