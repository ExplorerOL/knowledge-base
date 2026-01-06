Источник информации:
https://habr.com/ru/articles/435546/

# Использование ssh как прокси
Запуск на одном адресе хоста `127.0.0.1`
```
ssh -D <port> <user>@<remoteserver>
```

Запуск на всех адресах хоста `0.0.0.0:8888`
```
ssh -D 0.0.0.0:<port> <user>@<remoteserver>
```