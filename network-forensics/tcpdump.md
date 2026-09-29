# tcpdump
Lightweight command-line packet analyzer and capture engine.

Syntax: tcpdump [options] [bpf_filter]

Flags: -i <interface> (capture interface), -r <file> (read pcap), -w <file> (write raw packets to file), -nn (do not resolve hostnames or port names), -X (print payload in Hex and ASCII)

Example: tcpdump -nn -r capture.pcap 'tcp port 80 or tcp port 443'
