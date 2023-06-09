## Перечень классов

Существует несколько классов бакета, отличающиеся как назначением, так и размером оплаты размещаемых в них объектах:

- Hotbox — хранение и быстрая раздача большого количества файлов для медиасервисов, онлайн-СМИ, сайтов с многопользовательским контентом и мобильных приложений. В апи обозначается названием STANDARD.
- Icebox — облачное хранение редко используемых данных: бэкапов, логов, медиаконтента, научных, статистических данных, а также рабочих архивов. В апи обозначается названием STANDARD_IA
- Backup — размещение резервных копий инстансов, созданных как автоматически, так и вручную. Бакет этого класса не подлежит самостоятельному созданию или удалению, а управляется сервисом резервного копирования. В апи обозначается названием BACKUP.

## Смена класса бакета

После создания бакета в интерфейсе панели возможно изменить его класс: с Hotbox на Icebox и обратно. Для этого в панели VK Cloud необходим выбрать бакет, класс которого подлежит смене, затем на вкладке «Класс хранения» изменить класс и подтвердить изменения кнопкой «Сохранить изменения».

Класс хранения, заданный для бакета, обозначает дефолтный сторадж класс, который назначается объектам и мультипартам, складываемым в этот бакет. То есть, если вы будете класть объекты без указания класса хранения, то они будут складываться с классом хранения заданном на бакете.

Смена класса хранения бакета не влияет на уже залитые объекты, их класс хранения не изменится.

## Класс хранения объектов

Класс хранения объектов можно назначать отличным от класса хранения бакета. Это делается через заголовок x-amz-storage-class.

Важно понимать, что если вы положите объект с заголовком x-amz-storage-class равным STANDARD ( для нас это класс хранения Hotbox ) в бакет, для которого дефолтным определен  класс хранения STANDARD_IA  ( для нас это класс хранения Icebox ), то в итоге вы получите объект с классом хранения STANDARD ( Hotbox ).

## Класс хранения мультипартов

Мультипарты отличаются от обычных объектов способом заливки:

- сначала вы инициируйте мультипарт (операция InitiateMultipart).
- потом загружаете его части  — парты (операция UploadPart).
- потом собираете мультипарт (операция CompleteMultipart).

При определении класса хранения мультипарта важно понимать, что он задается именно на стадии инициации мультипарта (InitiateMultipart). На этой операции вы задаете класс хранения или же он берется дефолтным, равным классу хранения бакета на момент операции.

При заливке частей мультипарта и последующей их сборке класс хранения поменять нельзя. Если вы хотите его поменять, нужно собрать мультипарт (CompleteMultipart) и потом уже поменять класс хранения через операцию копирования объекта.
