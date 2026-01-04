Источник информации:
 
https://www.youtube.com/watch?v=5Ppg5PHQFH4
https://m.vk.com/video-165282829_456239102?from=video&t2fs=2477d99476abdc1b4e_2

# Диагностика физического уровня
Диагностика физических параметров подключния и линии связи
- **ethtool**
- **cable diag**
- **test copper-port dir**
- **ddm status**

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

# Диагностика канального уровня:
Проверка двухсторонней связности и настроек сетевых интерфейсов
- **ifconfig** (устаревшая), **ipconfig**, **ipaddr**
- **ping**
- **arp**
- **show mac-address table** / **fdb**

Проверка IP адреса и маски, MAC-адреса, статистика по пакетам
```
ifconfig
```
- **ping** (работает по протоколу ICMP)

Проверка доступности сервера
```
ping <IP-address>
```

- **arp** 

Проверка ARP таблицы
```
arp -a
```
# Диагностика сетевого уровня
Трассировка маршрута и проверка таблиц маршрутизции
- **traceroute**/**tracert**
- **netstat -r**
- **ip route**/**route print**
- **show ip route**

Задание шлюза по умолчанию
```
ip route add default via <IP-addr>
```

Проверка маршрута. Первый адрес - всегда шлюз по умолчанию
```
traceroute <IP-addr>
```

# Диагностика транспортного уровня
Диагностика транспорта на уровне сокетов
- **netstat**/**lsof**/**ss**
- **telnet <port>**
- **nmap**

Просмотр списка соединений
```
netstat
netstat -nt | grep <IP-adr>
```
Просмотр прослушиваемых портов
```
ss -lnt
```
Проверка открыти ли порт
```
telnet <IP-addr> <port>
GET/
```
Просмотр списка активных портов
```
nmap <IP-addr>
nmap -nsP <IP-addr>
nmap -sV -p <port> <IP-addr>
```
# Диагностика верхних уровней
Диагностика работы служб и приложений
- **tcpdump**
- **wireshark**
- **dhcpdump**
- **nslookup**/**dig**/**host**
- **iperf**
- **iptables**

Просмотр траффика 
```
tcpdump -i <interace> host <IP-addr>
```
Проверка скорость передачи
Запуск на сервере
```
iperf3 -s
```
Запуск на клиенте
```
iperf3 -c <IP-addr>
```