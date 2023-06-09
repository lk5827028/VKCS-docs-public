В VK Cloud существует возможность создавать резервные копии виртуальных машин по расписанию.

Автоматическое резервное копирование представлено в виде «Плана резервного копирования» и включает в себя все диски инстанса, добавление или удаление дисков ВМ также изменяет план.

<info>

Резервные копии размещаются в общем хранилище данных и оплачиваются в соответствии с тарифом. Подробную информацию о стоимости хранения можно увидеть в [детализации расходов](/ru/additionals/billing/operations/detail) проекта.

</info>

После удаления виртуальной машины все резервные копии сохраняются в проекте. Удаление резервных копий, созданных планом, потребуют ручной операции удаления самого плана. Ручные бэкапы можно удалить в любой момент при необходимости.

Настройка плана резервного доступны из нескольких интерфейсов.

## Панель управления VK Cloud

Для создания плана [в личном кабинете VK Cloud](https://mcs.mail.ru/app/services/infra/servers/) следует:

1.  Перейти в раздел «Резервное копирование» сервиса «Облачные вычисления».
2.  На вкладке «Автоматическое» нажать «Добавить» для добавления плана.
3.  Настроить параметры резервного копирования:

- Тип резервного копирования — полное или инкрементальное резервное копирование. Инкрементальное позволяет сэкономить место, снизить расходы и увеличить скорость создания бэкапов.
- Название плана — название плана резервного копирования.
- Максимальное количество полных бэкапов — настраивает количество хранимых полных резервных копий.
- Расписание резервного копирования	— задает дни и время создания копий. Возможно создание нескольких расписаний.
- Применить для следующих инстансов	— выбор виртуальных машин, для которых будут создаваться копии.

4. Нажать «Сохранить план».

<warn>

В случае изменения параметра «Макс. количество полных бэкапов», удаление лишних резервных копий происходит через 1 час после сохранения изменений.

</warn>

Для редактирования плана резервного копирования в разделе «Резервное копирование» требуется в контекстном меню плана выбрать пункт «Изменить».

Для удаления плана следует в контекстном меню плана выбрать «Удалить». Это также удалит все точки восстановления (резервные копии).
