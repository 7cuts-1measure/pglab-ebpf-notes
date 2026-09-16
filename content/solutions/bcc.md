BPF Compiler Colleciton https://github.com/iovisor/bcc
![[Pasted image 20260915115942.png]]

# Чем полезно
Здесь уйма готовых программ (с исходниками!) под специфичные задачи - статистика по сокетам, по соединениям (пассивным и активным). Их можно просто объединить в одно приложение для мониторинга и получить кучу инфы.

> [!INFO] В некоторых дистрибутивах есть пакет со всеми утилитами BCC (на арче -`bcc-libbpf-tools`)

- [tcptracer](https://github.com/iovisor/bcc/blob/master/tools/tcptracer_example.txt) - отслеживание tcp соединений (`connect()`, `accept()`) по каждому процессу
- [tcplife](https://github.com/iovisor/bcc/blob/master/tools/tcplife_example.txt) - отслеживание времени жизни сокетов (отрабатывает уже когда сокет закрылся)