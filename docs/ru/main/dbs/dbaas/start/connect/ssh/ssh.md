Для успешного подключения к БД по SSH необходимо на этапе создания Базы данных установить указанные ниже настройки.

1. При создании Базы данных необходимо в настройках Firewall добавить правило "ssh+www", которое открывает 22 порт для успешного подключения.

1. Далее, в меню "Ключ для доступа по SSH" в выпадающем списке выбрать создание нового ключа.

1. После нажатия кнопки "Создать базу данных" начнется скачивание ключа в формате .pem на локальный ПК.

1. Подключение к Базе данных по SSH происходит на локальном ПК в командной строке. Для подключения в строке необходимо ввести

```
ssh -i <путь к ключу> admin@<внешний ip-адрес>
```

При успешном подключении ответ будет выглядеть следующим образом:

```
[admin@redis-4275 ~]$
```
