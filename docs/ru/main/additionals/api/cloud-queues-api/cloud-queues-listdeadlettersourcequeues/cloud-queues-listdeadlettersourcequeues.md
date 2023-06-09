Запрос возвращает список ваших очередей, для которых RedrivePolicy атрибут очереди настроен с помощью очереди недоставленных сообщений.

Метод поддерживает разбиение на страницы. Задайте параметр MaxResults в запросе, чтобы указать максимальное количество результатов, возвращаемых в ответе. Если не установить MaxResults, ответ будет содержать не более 1000 результатов. Если вы установили MaxResults и есть дополнительные результаты для отображения, ответ будет содержать значение для NextToken. Используйте NextToken в качестве параметра в запросе ListDeadLetterSourceQueuesчтобы получить следующую страницу результатов.

## Параметры запроса

MaxResults

Максимальное количество результатов для включения в ответ. Диапазон значений от 1 до 1000. Вы должны установить, MaxResults чтобы получить значение NextToken в ответе.

Тип: целое число

Обязательно: Нет

NextToken

Токен разбиения на страницы для запроса следующего набора результатов.

Тип: Строка

Обязательно: Нет

QueueUrl

URL-адрес очереди недоставленных сообщений.

URL-адреса и имена очередей чувствительны к регистру.

Тип: Строка

Обязательно: Да

## Элементы ответа

Следующие элементы возвращаются службой.

NextToken

Токен разбиения на страницы для включения в следующий запрос. Значение токена - это nullесли нет дополнительных результатов для запроса или если вы не указали MaxResultsв запросе.

Тип: Строка

QueueUrl.N

Список URL-адресов исходных очередей, для которых RedrivePolicyатрибут очереди настроен с помощью очереди недоставленных сообщений.

Тип: массив строк

## Ошибки

AWS.SimpleQueueService.NonExistentQueue

Указанная очередь не существует.

Код состояния HTTP: 400

## Примеры

Следующий пример запроса запроса возвращает список исходных очередей недоставленных сообщений. В этом примере только одна исходная очередь MySourceQueue настроена с очередью недоставленных сообщений. Структура AUTHPARAMSзависит от подписи запроса API.

#### Образец  запроса

```
?Action=ListDeadLetterSourceQueues
&Expires=2020-12-12T22:52:43PST
&Version=2012-11-05
&AUTHPARAMS
```

#### Образец ответа

```
<ListDeadLetterSourceQueuesResponse xmlns="https://sqs.mcs.mail.ru/doc/2012-11-05/">
    <ListDeadLetterSourceQueuesResult>
        <QueueUrl>https://sqs.mcs.mail.ru/123456789012/MySourceQueue</QueueUrl>
    </ListDeadLetterSourceQueuesResult>
    <ResponseMetadata>
        <RequestId>8ffb921f-b85e-53d9-abcf-d8d0057f38fc</RequestId>
    </ResponseMetadata>
</ListDeadLetterSourceQueuesResponse>
```
