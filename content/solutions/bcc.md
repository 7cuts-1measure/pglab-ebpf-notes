BPF Compiler Colleciton https://github.com/iovisor/bcc
![[Pasted image 20260915115942.png]]

# Чем полезно
Здесь уйма готового кода под специфичные задачи - статистика по сокетам, по соединениям (пассивным и активным). Их можно просто объединить в одно приложение для мониторинга и получить кучу инфы.

# Список инструментов
Это набор программ на eBPF под любую цель. Список из readme в разделе networking

-  tools/[gethostlatency](https://github.com/iovisor/bcc/blob/master/tools/gethostlatency.py): Show latency for `getaddrinfo/gethostbyname` calls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/gethostlatency_example.txt)
- tools/[bindsnoop](https://github.com/iovisor/bcc/blob/master/tools/bindsnoop.py): Trace IPv4 and IPv6 bind() system calls (bind()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/bindsnoop_example.txt).
- tools/[netqtop](https://github.com/iovisor/bcc/blob/master/tools/netqtop.py) tools/[netqtop.c](https://github.com/iovisor/bcc/blob/master/tools/netqtop.c): Trace and display packets distribution on NIC queues. [Examples](https://github.com/iovisor/bcc/blob/master/tools/netqtop_example.txt).
- tools/[sofdsnoop](https://github.com/iovisor/bcc/blob/master/tools/sofdsnoop.py): Trace FDs passed through unix sockets. [Examples](https://github.com/iovisor/bcc/blob/master/tools/sofdsnoop_example.txt).
- tools/[solisten](https://github.com/iovisor/bcc/blob/master/tools/solisten.py): Trace TCP socket listen. [Examples](https://github.com/iovisor/bcc/blob/master/tools/solisten_example.txt).
- tools/[sslsniff](https://github.com/iovisor/bcc/blob/master/tools/sslsniff.py): Sniff OpenSSL written and read data. [Examples](https://github.com/iovisor/bcc/blob/master/tools/sslsniff_example.txt).
- tools/[tcpaccept](https://github.com/iovisor/bcc/blob/master/tools/tcpaccept.py): Trace TCP passive connections (accept()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpaccept_example.txt).
- tools/[tcpconnect](https://github.com/iovisor/bcc/blob/master/tools/tcpconnect.py): Trace TCP active connections (connect()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpconnect_example.txt).
- tools/[tcpconnlat](https://github.com/iovisor/bcc/blob/master/tools/tcpconnlat.py): Trace TCP active connection latency (connect()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpconnlat_example.txt).
- tools/[tcpdrop](https://github.com/iovisor/bcc/blob/master/tools/tcpdrop.py): Trace kernel-based TCP packet drops with details. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpdrop_example.txt).
- tools/[tcplife](https://github.com/iovisor/bcc/blob/master/tools/tcplife.py): Trace TCP sessions and summarize lifespan. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcplife_example.txt).
- tools/[tcpretrans](https://github.com/iovisor/bcc/blob/master/tools/tcpretrans.py): Trace TCP retransmits and TLPs. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpretrans_example.txt).
- tools/[tcprtt](https://github.com/iovisor/bcc/blob/master/tools/tcprtt.py): Trace TCP round trip time. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcprtt_example.txt).
- tools/[tcpstates](https://github.com/iovisor/bcc/blob/master/tools/tcpstates.py): Trace TCP session state changes with durations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpstates_example.txt).
- tools/[tcpsubnet](https://github.com/iovisor/bcc/blob/master/tools/tcpsubnet.py): Summarize and aggregate TCP send by subnet. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpsubnet_example.txt).
- tools/[tcpsynbl](https://github.com/iovisor/bcc/blob/master/tools/tcpsynbl.py): Show TCP SYN backlog. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpsynbl_example.txt).
- tools/[tcptop](https://github.com/iovisor/bcc/blob/master/tools/tcptop.py): Summarize TCP send/recv throughput by host. Top for TCP. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcptop_example.txt).
- tools/[tcptracer](https://github.com/iovisor/bcc/blob/master/tools/tcptracer.py): Trace TCP established connections (connect(), accept(), close()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcptracer_example.txt).
- tools/[tcpcong](https://github.com/iovisor/bcc/blob/master/tools/tcpcong.py): Trace TCP socket congestion control status duration. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpcong_example.txt).
- tools/[mptcpify](https://github.com/iovisor/bcc/blob/master/tools/mptcpify.py): Force applications to use MPTCP instead of TCP. [Examples](https://github.com/iovisor/bcc/blob/master/tools/mptcpify_example.txt)
