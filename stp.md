# Компьютерные сети

## [Протокол STP] (http://en.wikipedia.org/wiki/Spanning_Tree_Protocol)

1. Причины и последствия возникновения петель на канальном уровне
2. Принципы работы протокола STP (IEEE 802.1d)
  * Формат кадров BPDU
  * Роли и состояния портов
  * Алгоритм STA
  * Алгоритм выбора BPDU
  * Изменение топологии
3. Обзор протоколов семейства STP
  * Cisco PVST+
  * MSTP
  * Cisco Per VLAN rapid STP
4. Принципы работы протокола Rapid STP (IEEE 802.1w)
  * Роли и состояния портов
  * Механизм Proposal - Agreement
  * Изменение топологии
  * Формат BPDU
5. Атаки на протокол STP
  * Подмена корневого моста
  * BPDU-flooding
  * Перехват пакетов
6. Механизмы защиты STP
  * Port Fast
  * BPDU Guard 
  * BPDU Filter
  * Root Guard
  * Loop Guard
7. Агрегирование каналов
  * Назначение
  * Алгоритмы балансировки 
  * Методы и протоколы конфигурирования
  * Механизм STP EtherChannel Guard
  
# Материалы
* [Сети для самых маленьких. STP](http://habrahabr.ru/post/143768/)
* [Understanding MSTP] (http://blog.ine.com/2010/02/22/understanding-mstp/)
* [Understanding Rapid Spanning Tree Protocol (802.1w)] (http://www.cisco.com/c/en/us/support/docs/lan-switching/spanning-tree-protocol/24062-146.html)
* [Принципы работы механизмов STP loop guard, root guard, BPDU filter](http://www.youtube.com/watch?v=R8gU6wJYiO4)
* [Yersinia. Framework for layer 2 attacks] (http://www.blackhat.com/presentations/bh-europe-05/BH_EU_05-Berrueta_Andres/BH_EU_05_Berrueta_Andres.pdf)
