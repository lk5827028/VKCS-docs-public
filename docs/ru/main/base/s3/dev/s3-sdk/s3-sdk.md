SDK — это набор средств разработки, позволяющий создавать приложения для сервиса Объектное хранилище платформы VK Cloud S3.

В зависимости от варианта использования можно выбрать один из пакетов SDK или инструментов:

- [Инструменты для PowerShell](https://docs.aws.amazon.com/powershell/latest/userguide/)
- [SDK для Java](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/)
- [SDK для .NET](https://docs.aws.amazon.com/sdk-for-net/latest/developer-guide/)
- [SDK для JavaScript](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/)
- [SDK для Ruby](https://docs.aws.amazon.com/sdk-for-ruby/v3/developer-guide/)
- [SDK для Python (Boto)](http://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [SDK для PHP](https://docs.aws.amazon.com/aws-sdk-php/guide/latest/)
- [SDK для Go](https://docs.aws.amazon.com/sdk-for-go/api/)
- [Mobile SDK для iOS](https://docs.amplify.aws/)
- [Mobile SDK для Android](https://docs.amplify.aws/)

## Предварительные требования

Вне зависимости от выбранного пакета SDK следует создать учетные данные для доступа к сервису Объектное хранилище VK Cloud. Для этого в меню «Аккаунты» необходимо добавить аккаунт.

При создании аккаунта будут предоставлены данные, которые требуется сохранить. После закрытия окна восстановить Secret Key будет невозможно, однако при его утере можно создать новый аккаунт.

<warn>  

**Внимание**

Имя аккаунта должно начинаться с буквы или цифры, может состоять только из латинских букв, цифр и символов: точка (.), тире (-), подчеркивание (\_).

</warn>

## Инструменты для PowerShell

Инструменты для PowerShell — это набор модулей PowerShell, основанных на функциональности, предоставляемой SDK для .NET. Инструменты для PowerShell позволяют создавать сценарии для операций с ресурсами Объектного хранилища VK Cloud S3 из командной строки PowerShell.

Командлеты предоставляют идиоматический интерфейс PowerShell для указания параметров и обработки результатов, даже если они реализованы с использованием различных API-интерфейсов HTTP-запросов сервисов VK Cloud. Например, командлеты для PowerShell поддерживают конвейерную обработку PowerShell, то есть можно передавать объекты PowerShell в командлеты и из них.

Можно установить инструменты для PowerShell на компьютеры под управлением операционных систем Windows, Linux или macOS.

[Полная документация](https://docs.aws.amazon.com/powershell/latest/userguide/) по работе с инструментами PowerShell.

## SDK для Java

SDK для Java предоставляет Java API для VK Cloud. Используя SDK, можно создавать приложения Java, которые работают с Объектным хранилищем VK Cloud S3. Список поддерживаемых служб и их версий API, включенных в каждый выпуск SDK, можно увидеть в [заметках к выпуску](https://github.com/aws/aws-sdk-java#release-notes) для той версии, с которой в данный момент производится работа.

[Полная документация](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/) по работе с инструментами SDK для Java.

## SDK для .NET

SDK для .NET упрощает создание приложений .NET, использующих экономичные, масштабируемые и надежные сервисы VK Cloud, такие как VK Cloud S3. SDK упрощает использование сервисов VK Cloud, предоставляя набор библиотек, которые согласованы и знакомы разработчикам .NET.

[Полная документация](https://docs.aws.amazon.com/sdk-for-net/latest/developer-guide/) по работе с инструментами SDK для .NET.

## SDK для JavaScript

SDK для JavaScript предоставляет API JavaScript для услуг VK Cloud. Можно использовать JavaScript API для создания библиотек или приложений для Node.js или браузера.

Не все сервисы сразу доступны в SDK. Узнать какие сервисы в настоящее время поддерживаются SDK для JavaScript можно на [официальном ресурсе](https://github.com/aws/aws-sdk-js/blob/master/SERVICES.md).

[Полная документация](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/) по работе с инструментами SDK для JavaScript.

## SDK для Ruby

SDK для Ruby помогает упростить написание кода, предоставляя классы Ruby для сервиса Объектное хранилище VK Cloud.

[Полная документация](https://docs.aws.amazon.com/sdk-for-ruby/v3/developer-guide/) по работе с инструментами SDK для Ruby.

## SDK для Python (Boto)

Boto — это SDK для Python. Он позволяет разработчикам Python создавать, настраивать и управлять сервисом Объектное хранилище VK Cloud S3. Boto предоставляет простой в использовании объектно-ориентированный API, а также низкоуровневый доступ к сервису VK Cloud S3.

[Полная документация](http://boto3.amazonaws.com/v1/documentation/api/latest/index.html) по работе с инструментами SDK для Python (Boto).

## SDK для PHP

SDK для PHP версии 3 позволяет разработчикам PHP использовать VK Cloud S3 в своем PHP-коде и создавать надежные приложения и программное обеспечение с использованием VK Cloud S3. Можно начать работу за считанные минуты, установив SDK через Composer, потребуется пакет aws/aws-sdk-php, или загрузив автономные aws.zip или файл aws.phar.

[Полная документация](https://docs.aws.amazon.com/aws-sdk-php/guide/latest/) по работе с инструментами SDK для PHP.

## SDK для Go

Пакет SDK для Go — это официальный SDK AWS для языка программирования Go.

SDK для Go предоставляет API и утилиты, которые разработчики могут использовать для создания приложений Go, использующих сервис VK Cloud S3.

SDK устраняет сложность программирования непосредственно в интерфейсе веб-службы. Он скрывает многие элементы нижнего уровня, такие как аутентификация, повторные попытки запроса и обработка ошибок. SDK также включает полезные утилиты поверх API, которые добавляют дополнительные возможности и функции.

Дополнительная информация доступны в [документации пакета s3manager](https://docs.aws.amazon.com/sdk-for-go/api/service/s3/s3manager/).

[Полная документация](https://docs.aws.amazon.com/sdk-for-go/api/) по работе с инструментами SDK для Go.

## Mobile SDK

Amplify Framework предоставляет набор библиотек и компонентов пользовательского интерфейса, а также интерфейс командной строки для создания мобильных бэкэндов и интеграции с приложениями iOS, Android, Web и React Native. Интерфейс командной строки Amplify позволяет настраивать все службы, необходимые для работы серверной части, через простой интерфейс командной строки. Библиотека Amplify упрощает интеграцию кода с серверной частью с помощью декларативных интерфейсов и простых компонентов пользовательского интерфейса.

[Полная документация](https://docs.amplify.aws/) по работе с инструментами Mobile SDK.
