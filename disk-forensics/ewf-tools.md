# EWF Tools
Utilities for handling Expert Witness Format (`.E01`) files.

---

## Tools & Commands

### 1. `ewfverify` – Verify Hashes
Verifies the integrity of an E01 image by calculating and comparing hashes.

* **Syntax:**
  ```bash
  ewfverify [options] image.E01
Example:

Bash
ewfverify evidence.E01
### 2. ewfmount – Mount E01 as Raw Disk Image
Mounts an E01 file to access it as a raw disk image stream.

Syntax:

Bash
ewfmount [options] image.E01 <mount_point>
Example:

Bash
ewfmount evidence.E01 /mnt/ewf/
Note: Access the raw stream via /mnt/ewf/ewf1.

### 3. ewfinfo – Read Metadata Headers
Extracts and displays metadata headers stored inside the E01 file.

Syntax:

Bash
ewfinfo image.E01