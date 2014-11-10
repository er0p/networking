# Компьютерные сети

## Описание курса

Программа и материалы курса «Компьютерные сети»
образовательной программы по направлению подготовки (специальности)
10.05.01 «Компьютерная безопасность», преподаваемого в [Национальном исследовательском Томском государственном университете](http://www.tsu.ru) на [кафедре защиты информации и киптографии](http://isc.tsu.ru)

## Вопросы

1. Введение
 * Основные принципы построения сетей
   * Коммутация пакетов
    * Имена пакетов (PDU/SDU, кадр, дейтаграмма, сегмент, сообщение)
    * Общий формат пакетов 
    * Порядок байт
  * Многоуровневость (Layering)
  * Инкапсуляция и туннелирование (Incapsulation)
  * Адресация
 * Основные модели
   * Модель ISO/OSI
   * Модель TCP/IP
   * Модель клиент-сервер
   * Модель peer-to-peer  
 * Типы сетей
   * PAN, WLAN, LAN, MAN, WAN, VPN 
   * Internet, Extranet и Intranet
   * Сети, подсети и сегменты
   * Топологии сетей
 * Производительность сетей
   * Качество обслуживания (QoS)
   * Виртуализация
   * Отказоустойчивость и высокая доступость
 * Примеры сетевых приложений
  *  WEB
  *  Skype
  *  BitTorrent
 * [Несколько миллисекунд HTTPS соединения] (http://habrahabr.ru/post/191954/)
1. Технология Ethernet
 * Обзор технологий ЛВС
 * Архитектура Ethernet
 * Метод CSMA/CD
 * Адресация 
 * Формат кадров
 * Основные виды Ethernet
 * Коммутация в Ethernet (IEEE 802.1D)
1. Технология Wi-Fi  
 * Архитектруа IEEE 802.11
 * Проблема скрытого узла
 * Метод CSMA/CA
 * Механизм RTS/CTS 
 * Формат кадров
1. Протокол STP
 * Возникновение петель на канальном уровне
 * Формат кадров
 * Механизмы оптимизации и надежности STP
  * PortFast
  * RootGuard
  * BPDUGuard
  * BPDUFilter
  * LoopGuard
   * UplinkFast
  * Основные этапы STP
  * Механизм UDLD
   * Управление протоколом STP
   * Особенности протокола Rapid STP
1. Технология VLAN
 * Определение VLAN
 * Виды VLAN
 * Коммутация в VLAN (IEEE 802.1Q)
 * Основные протоколы VLAN (VTP, DTP и VMPS)
 * Формат кадров IEEE 802.1Q
 * Маршрутизация VLAN
1. Протокол IP
 * Протокол IPv4
  * Функции IP
  * Адресация
  * Формат дейтаграмм
  * Фрагментация
 * IP-опции
 * Протокол IPv6
  * Адресация
  * Формат дейтаграмм
  * Протокол обнаружения соседей
1. Протокол ICMP
 * Функции ICMP
 * Формат сообщений
 * Примеры работы сетевых механизмов на основе ICMP
  * Ping
  * Redirect
  * IP Expiry
1. Протоколы ARP/RARP
 * Функции ARP
 * Формат сообщений
 * Схема протокола ARP
 * Proxy-ARP
 * GARP
 * Схема пртокола RARP
1. Маршрутизация в IP-сетях
 * Основные термины
  * Коммутация
  * Маршрутизация
  * Автономная система
  * Внешняя и внутренняя маршрутизация
  * Конвергенция
  * Метрики
  * Дистанционно-векторные протоколы
  * Протоколы состояния связей
  * Гибридные протоколы
  * Схема ретрансляции дейтаграмм
  * Методы ретрансляции
   * Process Switching
   * Fast Switching
   * CEF
  * Механизм ECMP
1. Протоколы FHRP
 * Протоколы VRRP/HSRP
 * Протокол GLBP
1. Протокол RIP   
 * Адгоритм Беллмана-Форда
 * Схема протокола
 * Проблемы RIP
  * Счет до бесконечности
  * Зацикливание
 * Механизмы защиты
1. Протокол OSPF
 * Алгоритм Дейкстры
 * Схема протокола
 * Типы OSPF-сетей
 * Формат сообщений
 * Протокол Hello
 * Назначение Router-ID
 * OSPF-flooding
 * Типы областей в OSPF
 * Типы LSA
1. Протокол UDP
 * Функции протокола
 * Формат дейтаграмм
 * Случаи использования UDP
1. Протокол TCP
 * Функции протокола
 * Основные механизмы
 * Формат сегментов
 * Флаги TCP
 * Опции TCP
 * Установка и завершение соединения
 * Состояния TCP
 * Механизм скользящего окна
 * Алгоритм Найгла
 * Отложеные подтверждения
 * Повторная передача
 * Быстрая повторная передача
 * Выборочные подтверждения
 * Управление перегрузками
  * Tahoe
  * Reno
1. Система DNS
 * Функции DNS
 * Итеративные запросы
 * Рекурсивные запросы
 * Схема разрешения имен
 * Формат сообщений DNS
1. Принципы построения и оптимизации сетей
 * Иерархическая модель сетей
  * Уровень доступа 
  * Уровень распределения
  * Уровень ядра
 * Основные модули  
 * Построение ЛВС
  * Классическая ЛВС
  * Полностью маршрутизируемая ЛВС
  * Оптимизация STP
  * Агрегирование каналов
 * Построение IP-сетей
  * Принципы проектирования пространства IP-адресов
  * Суммирование маршрутов
 * Механизмы высокой доступности
 * Виртуализация сетей
  
## Проекты

### Описание
Во время курса необходимо выполнить 4 проекта. Даты начала и завершения работы, а также сдачи отчетов назначаются для каждого проекта отдельно. Проект, отчет по которому сдан с опозданием не засчитывется.

### Задания

## Материалы

### Обязательные
* [У. Ричард Стивенс. Протоколы TCP/IP в подлиннике. Практическое руководство] (http://www.labirint.ru/books/23432/) 

### Рекомендуемые
* [Kevin R. Fall, W. Richard Stevens. TCP/IP Illustrated, Volume 1: The Protocols. Second edition] (http://www.amazon.com/TCP-Illustrated-Volume-Addison-Wesley-Professional/dp/0321336313/ref=pd_sim_b_8?ie=UTF8&refRID=0ZFEHB43F6Q7QWH4MQXC) 
* В. Олифер, Н. Олифер. Компьютерные сети. Принципы, технологии, протоколы. 4-е издание
* Э. Таненбаум, Д. Уезеролл. Компьютерные сети. 5-е издание
* [Stanford Online. An Introduction to Computer Networks] (http://online.stanford.edu/content/introduction-computer-networks)
* [Coursera. Computer Networks] (https://www.coursera.org/course/comnetworks)

### Справочные
* [The TCP-IP Guide](http://www.tcpipguide.com/)

