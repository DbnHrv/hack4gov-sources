# TShark
CLI version of Wireshark.

Syntax: tshark [options]

Flags: -r <file> (read pcap), -Y <display_filter> (Wireshark display filter), -T <format> (output format: fields, json, pdml), -e <field> (extract specific field)

Example: tshark -r capture.pcap -Y "http.request" -T fields -e ip.src -e http.host -e http.request.uri

