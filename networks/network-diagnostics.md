Источник информации: https://www.youtube.com/watch?v=5Ppg5PHQFH4

# Диагностика физического уровня:
- **ethtool**

Проверка статуса линка, скорость подключения, режим дуплекса:
```
ethtool <interface name>
```
Статистика передачи принятых и полученных пакетов, ошибки приема и передачи:
```
ethtool -S <interface name>
```
Тест порта:
```
ethtool -t <interface name> online
```
