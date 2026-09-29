# Plaso / log2timeline
Forensic timeline generation and processing toolset.

Step 1: Extract Artifacts (log2timeline.py)

Syntax: log2timeline.py [options] --storage-file <output.plaso> <input_source>

Flags: --parsers "<parser_list>" (specify custom parser filter), --vss_stores <selection> (process Volume Shadow Copies)

Example: log2timeline.py --storage-file timeline.plaso image.E01

Step 2: Filter and Format (psort.py)

Syntax: psort.py [options] -w <output_file> <timeline.plaso> "[filter_query]"

Flags: -o <format> (output format: l2tcsv, dynamic, json_line), -q (quiet mode)

Example: psort.py -o l2tcsv -w timeline.csv timeline.plaso "date > '2026-01-01 00:00:00'"
