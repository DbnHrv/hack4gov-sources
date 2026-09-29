# Binwalk
Firmware analysis and embedded file extraction tool.

Syntax: binwalk [options] <binary_file>

Flags: -e (automatically extract known file types), -M (matryoshka: recursively extract inside extracted files), -E (calculate and plot entropy graph), -c (carve unknown files)

Example: binwalk -e -M firmware.bin

