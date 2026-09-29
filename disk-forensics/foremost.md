# Foremost
File carving tool based on headers, footers, and data structures.

Syntax: foremost [options] -i <input> -o <output_dir>

Flags: -t <types> (file types: jpg, pdf, exe, all), -v (verbose mode), -q (quick mode, search 512-byte boundaries only)

Example: foremost -t jpg,pdf -i raw_disk.dd -o ./carved_output -v