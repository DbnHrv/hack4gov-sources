# strings & file
Basic static file inspection utilities.

file – Determine file type

Syntax: file [options] <file>

Flags: -i (output MIME type strings), -z (look inside compressed files)

Example: file -i sample.bin

strings – Extract printable characters from binaries

Syntax: strings [options] <file>

Flags: -a (scan entire file), -n <length> (minimum string length, default 4), -e <encoding> (e.g., l for 16-bit Little-Endian / Unicode)

Example: strings -a -n 8 -e l executable.exe > unicode_strings.txt
