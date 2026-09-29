# Volatility 3
Memory analysis framework for Windows, Linux, and macOS memory dumps.

Syntax: vol [global_options] <plugin> [plugin_options]

Global Flags: -f <file> (memory dump path), -o <dir> (output directory for dumped files), -v (increase verbosity)

Common Plugins:

windows.pslist / windows.pstree – List running processes

windows.netscan – View active and closed network connections

windows.malfind – Detect injected code / unlinked DLLs

windows.dumpfiles --pid <PID> – Dump executable files from memory

Example: vol -f memory.raw -o ./dumps windows.dumpfiles --pid 1044

