Приватный DNS в VK Cloud — функциональность DNS-сервера, работающего в проектных сетях платформы. Позволяет обращаться к инстансам по DNS-именам.

Сервис поддерживает настройку приватной зоны и имен портов виртуальных машин. DNS-сервер отвечает по тем же адресам, что и порты DHCP в сети. Для работы приватного DNS в сети должен быть включен DHCP-сервер.

<info>

В данный момент серверы пересылки запросов приватного DNS — `8.8.8.8`, `8.8.4.4`. Изменение этих адресов не поддерживается.

</info>

## Редактирование имени зоны для сети

1. Перейдите в [личный кабинет](https://mcs.mail.ru/app/) VK Cloud.
1. Выберите проект и регион.
1. Перейдите в раздел **Виртуальные сети** → **Сети**.
1. Откройте карточку сети, нажав на ее имя в общем списке.
1. Перейдите на вкладку **Настройка сети**.
1. Введите имя зоны в поле **Зона**.
1. Нажмите кнопку **Сохранить изменения**.

<warn>

Максимальная длина имени зоны — 253 символа. Состоит из блоков вида `[a-z0-9-]+\\.`. Максимальная длина блока — 63 символа. Блок не может начинаться и заканчиваться на `-`.

</warn>

## Настройка DNS-имени

<tabs>
<tablist>
<tab>Личный кабинет</tab>
<tab>OpenStack CLI</tab>
</tablist>
<tabpanel>

Возможно несколько способов настройки DNS-имени:

Через ВМ:

1. Перейдите в [личный кабинет](https://mcs.mail.ru/app/) VK Cloud.
1. Выберите проект и регион.
1. Начните [создавать новую виртуальную машину](/ru/base/iaas/vm-start/vm-quick-create). На шаге «Настройки сети» укажите имя в поле **DNS-имя**.

Через настройки порта:

1. Перейдите в [личный кабинет](https://mcs.mail.ru/app/) VK Cloud.
1. Выберите проект и регион.
1. Перейдите в раздел **Виртуальные сети** → **Сети**.
1. Откройте карточку сети, нажав на ее имя в общем списке.
1. Откройте карточку подсети, нажав на ее имя в общем списке.
1. Перейдите на вкладку **Порты**.
1. Раскройте меню нужного порта и выберите пункт **Редактировать порт**.
1. Укажите имя в поле **DNS-имя**.
1. Нажмите кнопку **Сохранить изменения**.

</tabpanel>
<tabpanel>

1. Убедитесь, что OpenStack CLI [установлен](../../../../base/account/project/cli/setup) и вы можете [авторизоваться](../../../../base/account/project/cli/authorization) в нем.

1. Получите список портов инстанса, выполнив команду:

   ```bash
   openstack port list --server <ID сервера>
   ```

1. Выполните команду:

   ```bash
   openstack port set --dns-name <DNS-имя> <ID порта>
   ```

</tabpanel>
</tabs>

<warn>

Максимальная длина имени — 63 символа. Допустимы только цифры, маленькие латинские буквы и тире `-`.

</warn>