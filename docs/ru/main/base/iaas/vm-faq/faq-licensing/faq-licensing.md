## Как получить лицензию Windows Server?

Лицензионная копия операционной системы Windows Server предустановлена в создаваемый инстанс виртуальной машины на базе ОС Windows. Активация лицензионной копии происходит автоматически после создания инстанса. При возникновении ошибки активации ОС следует [обратиться в техническую поддержку](/ru/contacts) и указать ID виртуальной машины.

## Какие лицензии я могу получить?

Перечень предоставляемых стандартных лицензий ограничен, но вы можете посмотреть список доступных [на странице с ценами](https://mcs.mail.ru/app/project/prices/). Для этого вы должны быть авторизованы.

При необходимости вы можете получить лицензию на программный продукт, которого нет в этом списке. Для этого необходимо [обратиться в техническую поддержу](/ru/contacts) с информацией о продукте и сроке использования.

## Какие есть типы лицензирования?

Microsoft предоставляет несколько моделей лицензирования, которые позволяют наиболее оптимально использовать свой бюджет:

- На ядро. Эта модель лицензирования предоставляет доступ неограниченному числу пользователей или устройств.
- На пользователя. Предназначена для предоставления доступа к лицензии одному пользователю на неограниченное количество серверов.

Лицензирование «на ядро» в рамках правил лицензирования Microsoft для виртуальных машин означает необходимость покрыть лицензией каждое виртуальное ядро инстанса. Вне зависимости от количества ядер инстанса, лицензии подлежат каждые 2 виртуальных CPU.

<info>

Лицензирование SQL сервера требует наличие не менее 2х лицензий по 2 vCPU согласно политике Microsoft.

</info>

## Могу ли я получить скидку?

Скидки на лицензирование не предусмотрены, но, так как денежные средства списываются поминутно с работающих сущностей, вы можете сократить свои расходы и сэкономить свои средства. Например, приостановить работу виртуальной машины или кластера.

## Есть ли поддержка ПО от Microsoft?

Обратитесь в техническую поддержку Microsoft, они ответят на все вопросы, касающиеся правил использования программного обеспечения Microsoft, а также технических вопросов по программным продуктам.

## Могу ли я использовать свою лицензию?

При наличии ранее приобретенной лицензии на программные продукты компании Microsoft, ее использование на платформе VK Cloud возможно, для этого необходимо удостовериться что лицензия может подлежать переносу, а также получить на это подтверждение от Microsoft. Более подробно написано в инструкции об [использовании собственных лицензий](https://mcs.mail.ru/help/licensing/license-mobility).

## Могу ли я купить лицензию на бессрочной основе?

VK Cloud предоставляет аренду лицензий на ежемесячной основе. Выкуп лицензии в постоянное использование, как на платформе VK Cloud так и вне ее, невозможен.

## За остановленную ВМ списываются средства?

Денежные средства списываются поминутно с работающих сущностей. Если работа сущностей остановлена, то списания продолжаются только за использование лицензий (Windows и RDS, если активированы) и арендованное дисковое пространство, а также за хранение имеющихся бэкапов.
