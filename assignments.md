# Компьютерные сети

## Задания к зачету

1. Написать сценарий, эмулирующий [командную строку Cisco IOS] (http://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.html) в рамках конфигурирования основных сетевых параметров операционной системы. Реализовать следующие команды:
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
2. Написать [BPF-фильтры] (https://blog.cloudflare.com/bpf-the-forgotten-bytecode/) для [tcpdump] (http://www.tcpdump.org/), решающие следующие задачи:
 * обнаружение использования протокола SSLv3
 * обнаружение сканирования портов методом "рождественской елки"
 * обнаружение аномальных сетевых пакетов
3. Проанализировать [трассировки wireshark] (/files) и объяснить, что проиходит в сети.
4. Используя [Scapy] (http://www.secdev.org/projects/scapy/), написать скрипт, выполняющий [идентификацию] (http://nmap.org/book/man-host-discovery.html) узла по его DNS-имени или IP-адресу следующими методами:
  * ICMP Ping
  * TCP Ping
  * UDP Discovery
5. Настроить тройной [GRE](http://en.wikipedia.org/wiki/Generic_Routing_Encapsulation)-туннель (GRE-over-GRE-over-GRE) между двумя узлами, работающими под управлением GNU/Linux. Экспериментально определить максимально возможную длину передаваемых данных без фрагментации.
6. Разработать и реализовать протокол *My Ping-Pong Protocol* (MPPP), позволяющий определить доступность узла сети по его IP-адресу или DNS-имени. Основные требования к протоколу:
  * протокол должен обеспечивать гарантии доставки запросов и ответов
  * протокол должен работать на основе протокола UDP
  * протокол должен позволять определять или назначать главного (master, primary) и второстепенного участника (slave, secondary)
  * все запросы инициируются только второстепенным участником
