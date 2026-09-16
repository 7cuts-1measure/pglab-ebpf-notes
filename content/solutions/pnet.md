repo: https://github.com/AlexanderWangY/pnet


# Что умеет
## Общая статистика по всем процессам

```
 
 PID    PROCESS     UP            DOWN            TX              RX
 5558   firefox     0 B/s         0 B/s           79,6 KB         160,5 KB
 42538  electron    0 B/s         0 B/s           0 B             39 B
 40854  Telegram    0 B/s         0 B/s           3,2 KB          1,9 KB
```


## Статистика для конкретного PID
Отображает статистику по каждому процессу и все соединения. (вместо SRC_IP и DST_IP там реальные ip-адреса)
```
pnet                                                                                                Sort: [B] [N] [P]  [Q]uit

   firefox  (PID 5558)

   ── Total Traffic ──

     Sent:        75,7 KB
     Received:    155,5 KB

   ── Connections (15) ──

     SRC_IP:PORT → DST_IP:PORT
       ↑ 16,9 KB  ↓ 7,9 KB

     SRC_IP:PORT → DST_IP:PORT
       ↑ 46 B  ↓ 46 B

     SRC_IP:PORT → DST_IP:PORT
       ↑ 39 B  ↓ 39 B
```


# Чего не хватает в статистике
- отслеживание именно сокетов
- детальный путь пакета: создание, отправка, и т.д. Это решается в [[pwru]]