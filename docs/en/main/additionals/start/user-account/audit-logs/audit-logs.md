Раздел «Журнал действий» предназначен для мониторинга и установки изменений. Чтобы перейти в раздел, в верхней части панели управления, нажмите на имя пользователя и выберите «Журнал действий». 

![](./assets/1626938836761-1626938723908.jpg)

На странице отобразится история действий пользователей, работающих с проектом. Сейчас история действий записывается 6 компонентами облака VK CS:

1.   Nova — контроллер вычислительных ресурсов.
2.   Cinder — компонент, отвечающий за работу с дисками.
3.   Karbor — компонент для защиты данных, обеспечивает резервное копирование.
4.   Neutron — компонент, реализующий виртуальные сети в облаке.
5.   Glance — компонент, который отвечает за хранение и работу с образами.
6.   Octavia — компонент, управляющий балансировщиками нагрузки.

По умолчанию страница отображает действия пользователей за последний месяц. Если вас интересует другой период, укажите новый диапазон времени и нажмите «Сформировать другой запрос». Затем нажмите «Показать отчет».

Сформированный отчет можно выгрузить в формате xls. Для этого нажмите «Скачать отчет» и он автоматически сохранится у вас на компьютере.

API
---

Чтобы автоматизированно получать записи журнала действий, используйте запрос к API:

```
curl -i -X GET "[https://infra.mail.ru](https://infra.mail.ru/):{port}/v1/{project\_id}/logs?source=nova" -H "X-Auth-Token: {auth\_token}"
```

Актуальный адрес эндпоинта вы можете посмотреть на странице «Настройки проекта» -> «API Endpoints».

| Параметры запроса | Значения | Описание |
| --- | --- | --- |
| From | RFC3339 | Начало временного диапазона. |
| To | RFC3339 | Конец временного диапазона. |
| Source | String | Источник события (компонент). |
| Marker | String | Токен для запроса следующей страницы, ранее возвращенный API. TTL маркеров — 1 час. |
| Limit | Integer | Количество возвращаемых записей. По умолчанию — 1000. |

Ответ:

```
{
   "logs": \[
      {
         "action":"create-floating-ip",
         "event\_id":"9840e233-6717-44d3-af7d-7a68837ee893",
         "method":"POST",
         "request\_body":"{}",
         "request\_id":"req-6bee7f11-b233-430a-9c55-f476be373b23",
         "response\_body":"{}",
         "source":"neutron",
         "success":"yes",
         "timestamp":"2021-07-16T13:13:20Z",
         "uri":"/v2.0/floatingips",
         "user\_email":"example@mcs.mail.ru",
         "user\_id":"d06lc1dd59bc22c4bc15d1de98d28119"
      },
      {
         "action":"vm-action",
         "event\_id":"7259205b-7u4e-4078-9ffc-zf15d2bd1a8f",
         "method":"POST",
         "request\_body":"{}",
         "request\_id":"req-8449b158-19bb-41b1-b0b4-e3522b9119f4",
         "response\_body":"{}",
         "source":"nova",
         "success":"yes",
         "timestamp":"2021-07-14T21:52:20Z",
         "uri":"/v2.1/servers/912gd12d9gd912/action",
         "user\_email":"example@mcs.mail.ru",
         "user\_id":"d06lc1dd59bc22c4bc15d1de98d28119"
      }
  \]
}
```