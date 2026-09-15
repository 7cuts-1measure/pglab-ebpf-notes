
https://github.com/cilium/pwru 

Умеет отслеживать, где  находится пакет

![[Pasted image 20260915113114.png]]

# Usage
(это выдаёт `pwru --help`. попросил нейронку сделать табличку)

| Опция                            | Что делает                                                                                                   |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `--all-kmods`                    | attach to all available kernel modules                                                                       |
| `--backend string`               | Tracing backend('kprobe', 'kprobe-multi'). Will auto-detect if not specified.                                |
| `--filter-func string`           | filter kernel functions to be probed by name (exact match, supports RE2 regular expression)                  |
| `--filter-ifname string`         | filter skb ifname in --filter-netns (if not specified, use current netns)                                    |
| `--filter-kprobe-batch uint`     | batch size for kprobe attaching/detaching (default 10)                                                       |
| `--filter-mark mark[/mask]`      | filter skb mark (format: mark[/mask], e.g., 0xa00/0xf00) (default 0x0)                                       |
| `--filter-netns string`          | filter netns ("/proc/<pid>/ns/net", "inode:<inode>")                                                         |
| `--filter-non-skb-funcs strings` | filter non-skb kernel functions to be probed (--filter-track-skb-by-stackid will be enabled)                 |
| `--filter-trace-tc`              | trace TC bpf progs                                                                                           |
| `--filter-trace-xdp`             | trace XDP bpf progs                                                                                          |
| `--filter-track-bpf-helpers`     | trace BPF helper functions                                                                                   |
| `--filter-track-skb`             | trace a packet even if it does not match given filters (e.g., after NAT or tunnel decapsulation)             |
| `--filter-track-skb-by-stackid`  | trace a packet even after it is kfreed (e.g., traffic going through bridge)                                  |
| `--filter-tunnel-pcap-l2 string` | pcap expression for vxlan/geneve tunnel (l2)                                                                 |
| `--filter-tunnel-pcap-l3 string` | pcap expression for vxlan/geneve tunnel (l3)                                                                 |
| `-h, --help`                     | display this message and exit                                                                                |
| `--kernel-btf string`            | specify kernel BTF file                                                                                      |
| `--kmods strings`                | list of kernel modules names to attach to                                                                    |
| `--output-caller`                | print caller function name                                                                                   |
| `--output-file string`           | write traces to file (rotates at 100MB by default)                                                           |
| `--output-file-max-size int`     | max size in MB per file before rotation (default 100)                                                        |
| `--output-file-max-age int`      | max age in days to keep rotated files (default 0, no limit)                                                  |
| `--output-file-max-backups int`  | max number of rotated files to keep (default 0, no limit)                                                    |
| `--output-file-compress`         | compress rotated files with gzip (default false)                                                             |
| `--output-json`                  | output traces in JSON format                                                                                 |
| `--output-limit-lines uint`      | exit the program after the number of events has been received/printed                                        |
| `--output-meta`                  | print skb metadata (default true)                                                                            |
| `--output-skb`                   | print skb                                                                                                    |
| `--output-skb-cb`                | print skb->cb                                                                                                |
| `--output-skb-metadata strings`  | print skb metadata (e.g., "skb->mark", "skb->hash"), 4 at most                                               |
| `--output-skb-shared-info`       | print skb shared info                                                                                        |
| `--output-stack`                 | print stack                                                                                                  |
| `--output-tcp-flags`             | print TCP flags                                                                                              |
| `--output-tunnel`                | print encapsulated tunnel header data                                                                        |
| `--output-tuple`                 | print L4 tuple (default true)                                                                                |
| `--output-xdp-metadata strings`  | print xdp metadata (e.g., "xdp->rxq->queue_index"), 4 at most                                                |
| `--set-percpu-buf uint32`        | set the size of buffers to print skb data (used by --output-skb and --output-skb-shared-info) (default 4096) |
| `--timestamp string`             | print timestamp per skb ("current", "relative", "absolute", "none") (default "none")                         |
| `--version`                      | show pwru version and exit                                                                                   |