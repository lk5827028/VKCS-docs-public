Перед созданием устройства:

1. Создайте драйвер.
1. Создайте шаблон устройства.

Инструкция по созданию перечисленных сущностей приведена далее.

## Создание драйвера

Драйвер — это описание способа коммуникации между агентом и конечным устройством.

Чтобы создать драйвер:

1. Перейдите в раздел **Драйверы** [личного кабинета](https://iot.mcs.mail.ru/) IoT Platform.
1. Нажмите кнопку **Добавить драйвер**.
1. В открывшейся форме укажите значения:

   - **Название**: название драйвера.
   - **Идентификатор**: идентификатор драйвера в рамках IoT Platform.
   - **Протокол**: [протокол](../connection/) взаимодействия.

1. Нажмите кнопку **Следующий шаг**.
1. Нажмите кнопку **Добавить параметр** для соответствующего подраздела. Например, параметры в разделе **Параметры События** будут контролировать частоту опроса сенсоров агентом у устройства, а в разделе **Параметры Состояния** — частоту опроса переключателей агентом у устройства. В открывшейся форме укажите значения и нажмите кнопку **Сохранить**:

   - **Название**: название создаваемого параметра.
   - **Тип значения**: тип данных, которые будут записываться в параметр.
   - **Обязательный параметр**: признак обязательности параметра.
   - **Значение по умолчанию**: показатель по умолчанию для параметра.

1. Нажмите кнопку **Сохранить** внизу страницы.

   Драйвер будет создан и появится в разделе **Драйверы**.

## Создание шаблона устройства

Шаблон устройства позволяет описать типовые устройства для быстрого последующего подключения новых устройств к платформе.

Чтобы создать шаблон для вашего устройства:

1. Перейдите в раздел **Шаблоны устройств** [личного кабинета](https://iot.mcs.mail.ru/) IoT Platform.
1. Нажмите кнопку **Добавить шаблон**.
1. Укажите в полях формы значения:

   - **Название шаблона**: наименование создаваемого шаблона.
   - **Идентификатор**: идентификатор шаблона.

1. Нажмите кнопку **Следующий шаг**.
1. Выберите в поле **Драйвер** вариант созданный ранее драйвер.
1. Нажмите кнопку **Следующий шаг**.
1. Добавьте параметры устройства при необходимости и нажмите кнопку **Следующий шаг**.
1. Задайте структуру шаблона: при необходимости укажите узел, датчик или агрегат.

   <warn>

   Конечным элементом структуры должен являться датчик.

   </warn>

1. Нажмите кнопку **Сохранить** под списком.

   Шаблон будет создан и появится в разделе **Шаблоны устройств**.

## Создание экземпляра устройства

1. Перейдите в раздел **Устройства** [личного кабинета](https://iot.mcs.mail.ru/) IoT Platform.
1. Нажмите кнопку **Добавить устройство**.
1. В появившейся форме заполните поля:

   - **Название**: наименование устройства.
   - **Идентификатор**: идентификатор устройства.
   - **Шаблон устройства**: используемый шаблон устройства.
   - **Агент**: агент для устройства.

1. Нажмите кнопку **Следующий шаг**.
1. В появившейся форме заполните поля:

   - **Название тега**: наименование тега для устройства.
   - **Идентификатор тега**: идентификатор тега.
   - **Родительский узел**: наименование родительского узла согласно выбранному шаблону устройства.

1. Нажмите кнопку **Следующий шаг**.
1. Повторите предыдущий шаг.
1. Нажмите кнопку **Сохранить**.

   Устройство будет создано и появится в разделе **Устройства**.

После создания виртуальной копии устройства задайте настройки подключения устройства к платформе — [создайте и настройте](../../agents/create-agent/) агент.
