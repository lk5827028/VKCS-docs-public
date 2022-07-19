VK Cloud Solutions предоставляет инсталляцию Hystax Acura для бесшовной live миграции вашей инфраструктуры в целевой проект облака VK CS.

Процесс подключения сервиса Hystax состоит из следующих шагов:

- Настройка облака для работы с контроллером Hystax Acura.
- Создание личного кабинета пользователя Hystax Acura и добавление целевого проекта VK CS.

## Настройка облака

В целевом проекте необходимо создать сеть (Network) *hystax_network* с включенной опцией «Доступ в интернет» и группу безопасности *sg_cloud_agent* (в группе должны быть разрешающие правила на входящий трафик к портам tcp/80, tcp/3260 и tcp/15000, а также разрешен весь исходящий трафик).

<info>

**Примечание**

Облако настраивается один раз, при этом целевых проектов может быть много.

</info>

## Создание ЛК пользователя Hystax Acura и добавление целевого проекта VK CS

Для создания личного кабинета пользователя Hystax Acura, перейдите на [страницу сервиса](https://mcs.mail.ru/disaster-recovery/) и нажмите на кнопку «Отправить заявку».

Введите ваши контактные данные: ФИО, ваш действующий email, номер телефона.

В ответе на ваше обращение менеджер запросит следующую информацию:

|Параметр| Значение|
|---|---|
|Project ID| Идентификатор проекта, (например bf3042f1725942d3ba90ea435f25bb54).|
|Project Name| Название проекта, (например mcs123456789).|
|User Domain Name| Имя пользовательского домена, (например users).|
|Project Domain ID| Идентификатор пользовательского домена, (например a59f3e0e7d32409cae61416a17de814a).|
|Username| Имя пользователя, (например j.snow@mail.ru).|
|Region Name| Название региона проекта, (например RegionOne).|
|Interface| Название типа интерфейса проекта, (например public).|
|Identity API Version| Версия API, (например 3).|
|Auth URL| URL аутентификации. |

Эти данные можно получить в личном кабинете VK CS, перейдя в «Настройки проекта» во вкладку «API ключи».

Наши специалисты на основании этих данных заведут учетную запись на контроллере Hystax Acura. Авторизуйтесь под полученным логином и паролем. Далее наш менеджер попросит предоставить данные пользователя для проведения валидации в облаке. Можно предоставить данные уже существующего в проекте пользователя, но мы рекомендуем создавать отдельного пользователя под задачу миграции инфраструктуры.