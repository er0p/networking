# Компьютерные сети

## Описание курса

Программа и материалы курса «Компьютерные сети»
образовательной программы по направлению подготовки (специальности)
10.05.01 «Компьютерная безопасность», преподаваемого в [Национальном исследовательском Томском государственном университете](http://www.tsu.ru) на [кафедре защиты информации и киптографии](http://isc.tsu.ru)

## Программа курса

1. [Введение] (intro.md)
1. [Технологии ЛВС](lan.md)
1. [Протокол STP] (stp.md)
1. [Протокол IP] (ip.md)
1. [Маршрутизация] (routing.md)
1. [Протокол ICMP](icmp.md)
1. [Протоколы TCP и UDP](tcp_udp.md)
1. Сетевая трансляция адресов (NAT)
  * Функции NAT
  * Виды NAT
    * Статическая трансляция адресов
    * Динамическая трансляция адресов
    * Трансляция источника (SNAT)
    * Трансляция назначения (DNAT)
  * Принципы работы 
1. [Протоколы прикладного уровня] (applications.md)
1. Базовый MPLS
  * Основные термины
  * Методы распространения меток
  * Протоколы распространения меток
  * Процесс коммутации пакетов
1. Качество обслуживания
  * Модели обслуживания
    * Best Effort Service
    * Integrated Service (IntServ)
    * Differentiated Service (DiffServ)
  * Основные функции QoS
    *  Классификация и маркирование
    *  Методы управления перегрузками
      * FIFO
      * Round robin и WRR
      * PQ
      * CQ
      * WFQ
      * CBWFQ
      * LLQ
    * Методы предотвращения перегрузок 
      * RED и WRED
      * ECN
      * Shaping
      * Policing
    * Сигнализация
      * RSVP  
1. Балансировка нагрузки (Load Balancing)
  * Назначение и функции балансировщиков нагрузки
  * Методы балансировки
    * Round robin
    * Weighted round robin
    * Least connections
    * Least response time
  * Технологии балансировки
    * Балансировка на основе DNS
    * Балансировка L3/L4
    * Балансировка L7
  * Механизмы поддержки сессий
1. [Основы дизайна компьютерных сетей] (design.md)

## Задания
1. Написать сценарий, эмулирующий [командную строку Cisco IOS] (http://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.html) в рамках конфигурирования основных сетевых параметров операционной системы. Реализовать следующие команды:
  * show ip route -  вывод таблицы маршрутизации
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
2. Написать [BPF-фильтр] (http://en.wikipedia.org/wiki/Berkeley_Packet_Filter) для [tcpdump] (http://www.tcpdump.org/), обнаруживающий использование веб-клиентом или веб-сервером шифра RC4.
3. Построить схему пространства IP-адресов компании "ABC". Провайдером выделена сеть 10.13.0.0/20. Компания "ABC" состоит из 5 филиалов, центрального офиса (ЦО) и центра обработки данных (ЦОД). Выполняются следующие условия:
  * рабочее место сотдуника включает компьютер, IP-телефон и принтер 
  * в филиале 1 работают 35 сотрудников
  * в филиале 2 работают 64 сотрудника
  * в филиале 3 работают 125 сотрудников
  * в филиале 4 работают 45 сотрудников
  * в филиале 5 работают 66 сотрудников
  * филиал 4 может увеличиться до 100 сотрудников
  * филиал 2 может сократиться до 30 сотрудников
  * в ЦОД развернуто 100 серверов 
  * схема подключения филиалов и ЦОД к ЦО - звезда
  * руководство компании задумывается о строительстве нового резервного ЦОДа
Учесть, что для организации каналов связи, подключения средств защиты, управления сетевым оборудованием, настройки маршрутизации и т.п. также необходимо выделять IP-адреса.
4. Проанализировать [трассировки wireshark] (/files) и объяснить, что проиходит в сети
5. Используя [Scapy] (http://www.secdev.org/projects/scapy/), написать скрипт, выполняющий [идентификацию] (http://nmap.org/book/man-host-discovery.html) узла по его DNS-имени или IP-адресу.
6. Настроить тройной [GRE] (http://en.wikipedia.org/wiki/Generic_Routing_Encapsulation) туннель (GRE-over-GRE-over-GRE) между двумя узлами, работающими под управлением GNU/Linux. Экспериментально определить максимально возможную длину передаваемых данных без фрагментации
7. Для трех выбранных операционных систем различных семейств (например, Windows, Solaris, Linux) провести анализ вероятностных характеристик начальных номеров последовательностей в TCP.
8. Разработать и реализовать протокол *My Ping-Pong Protocol* (MPPP), позволяющий определить доступность узла сети заданного по IP-адресу или DNS-имени. Основные требования к протоколу:
  * протокол должен обеспечивать гарантии доставки запросов и ответов
  * протокол должен работать на основе UDP
  * протокол должен позволять определять главного (master, primary) и второстепенного участника (slave, secondary)
  * все запросы инициируются только главным участником
9. Собрать следующую информацию о сети TSU.NET:
  *  имена и количество серверов имен;
  *  пространство IP-адресов;
  *  DNS-имена и IP-адреса почтовых серверов;
  *  возможность переноса зоны с первичного DNS-сервера;
  *  определить номер автономной системы сети;
  *  определить BGP-соседей;
  *  возможные маршруты до сети.


## Материалы

### Обязательная к прочтению литература
* [У. Ричард Стивенс. Протоколы TCP/IP в подлиннике. Практическое руководство] (http://www.labirint.ru/books/23432/) 

### Литература
* [Kevin R. Fall, W. Richard Stevens. TCP/IP Illustrated, Volume 1: The Protocols. Second edition] (http://www.amazon.com/TCP-Illustrated-Volume-Addison-Wesley-Professional/dp/0321336313/ref=pd_sim_b_8?ie=UTF8&refRID=0ZFEHB43F6Q7QWH4MQXC)
* [Э. Таненбаум, Д. Уезеролл. Компьютерные сети. 5-е издание] (http://www.ozon.ru/context/detail/id/20216983/)
* [Каверзные сетевые вопросы на Хабрахабр] (http://habrahabr.ru/post/189268/)
* [В. Олифер, Н. Олифер. Компьютерные сети. Принципы, технологии, протоколы. 4-е издание](http://www.ozon.ru/context/detail/id/20217199/)
* [Сети для самых маленьких на Хабрахабр] (http://linkmeup.ru/blog/11.html)
* [What happens when you type google.com into your browser's address box and press enter?](https://github.com/alex/what-happens-when)

### Справочная литература
* [The TCP-IP Guide](http://www.tcpipguide.com/)
* [Wireshark Sample Captures](http://wiki.wireshark.org/SampleCaptures)

### Видео
* [Coursera. Computer Networks] (https://www.coursera.org/course/comnetworks)
* [Stanford Online. An Introduction to Computer Networking] (https://class.stanford.edu/courses/Engineering/Networking/Winter2014/)
* [Cisco CCNA Course] (http://www.youtube.com/user/NetworKingInc)
* [David Wetherall. Video lectures for Computer Networks 5/E] (http://media.pearsoncmg.com/ph/streaming/esm/tanenbaum5e_videonotes/tanenbaum_videoNotes.html)
