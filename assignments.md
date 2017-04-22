# Компьютерные сети

## Задания к зачету

### Cisco IOS CLI 

Написать сценарий, эмулирующий [командную строку Cisco IOS](http://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.html) в рамках конфигурирования основных сетевых параметров операционной системы. Реализовать следующие команды:
  * show ip route - вывод таблицы маршрутизации
  * show interfaces - вывод информации обо всех сетевых интерфейсах
  * show interface {ethernet | loopback} *number* -  вывод информации о заданном интерфейсе 
  * ip route *prefix* *mask* *ip-address* - добавление статического маршрута к сети *prefix* с маской *mask* через шлюз *ip-address*
  * no ip route *prefix* *mask* *ip-address* - удаление статического маршрута
  * interface {ethernet | loopback} *number* - выбор интерфейса для конфигурирования
    * ip address *ip-address* *mask* - задание IP-адреса и сетевой маски для выбранного интерфейса
    * no ip address *ip-address* *mask* - удаление IP-адреса и сетевой маски для выбранного интерфейса 
    * shutdown - отключение интерфейса
    * no shutdown - включение интерфейса
  * ip name-server *server-address1* [*server-address2*] - задание DNS-сервера
  * no ip name-server *server-address1* [*server-address2*] - удаление DNS-сервера
 * ip routing - включение режима маршрутизации 
 * no ip routing - отключение режима маршрутизации

### BPF-фильтры

Реализовать [BPF-фильтры](https://blog.cloudflare.com/bpf-the-forgotten-bytecode/) для [tcpdump](http://www.tcpdump.org/), решающие следующие задачи:
 * обнаружение использования протокола SSLv3
 * обнаружение сканирования портов методом "рождественской елки"
 * обнаружение аномальных входящих сетевых IP-дейтаграмм из Интеренет в сеть 200.0.0.0/24

### Анализ трассировок Wireshark

Проанализировать [трассировки wireshark](/files) и объяснить, что проиходит в сети.

### Сканер

Используя [Scapy](http://www.secdev.org/projects/scapy/), написать скрипт, выполняющий [идентификацию](http://nmap.org/book/man-host-discovery.html) узлов сети по его DNS-имени или IP-адресу следующими методами:
  * ICMP Ping
  * TCP Ping
  * UDP Discovery
  * ARP Discovery
  
Вход: 
 * IP-адрес сети, IP-адрес или DNS-имя идентифицируемого узла
 * метод идентификации
 * перечень портов для TCP- и UDP-методов

Выход: перечень доступных узлов

Пример:

```
# discovery --icmp 10.10.34.0/24
Host 10.10.34.10 is alive
Host 10.10.34.15 is alive
Host 10.10.34.50 is alive

# discovery --tcp --ports 22,25,80,443 10.10.34.34
Host 10.10.34.34 is alive
```

### Path MTU Discovery
Реализовать алгоритм [Path MTU Discovery](https://en.wikipedia.org/wiki/Path_MTU_Discovery).

Вход: 
 * IP-адрес или DNS-имя узла

Выход: значение MTU

Пример:

```
# mtudiscovery 10.34.34.34
MTU is 1400
```

### GRE-туннель

Настроить тройной [GRE](http://en.wikipedia.org/wiki/Generic_Routing_Encapsulation)-туннель (GRE-over-GRE-over-GRE) между двумя узлами, работающими под управлением GNU/Linux. Экспериментально определить максимально возможную длину передаваемых данных без фрагментации.

### TCP Traceroute

Реализовать скрипт, который выводит маршрут до заданного узла.
Данный скрипт должен использовать протокол `TCP`, а не `ICMP` и `UDP`, как в утилитах `traceroute` или `tracert`.

Вход: IP-адрес или DNS-имя узла сети, максимальное количество промежуточных узлов.
Выход: результат трассировки

Пример:

```
# tcptraceroute 1.1.1.1 -n 40

a.b.c.d route:
1. 10.10.10.1 - 10 msec
2. *
3. *
4. 10.0.0.1 - 12 msec
5. 1.1.1.1  - 15 msec
```

### Протокол SUDP+

Разработать и реализовать протокол *Simple User Datagram Protocol Plus* (SUDP+)
Основные требования к протоколу:
  * протокол должен работать поверх UDP
  * протокол должен обеспечивать доставку дейтаграмм
  * протокол должен обеспечивать доставку дейтаграмм в оригинальном порядке

### HTTP-прокси*

Реализовать обратный HTTP-прокси (reverse proxy) с использованием фрэймворка [Twisted](https://github.com/twisted/twisted). HTTP-прокси должен иметь возможность балансировки нагрузки, добавления HTTP-заголовков, изменения HTML-документов.
