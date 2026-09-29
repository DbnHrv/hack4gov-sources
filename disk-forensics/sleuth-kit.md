# DISK FORENSICS

## 1. The Sleuth Kit (TSK)
Command suite for analyzing disk images and file systems.

---

### `mmls` – Volume/Partition Layout

* **Syntax:**
  ```bash
  mmls [options] image.dd
  ```
* **Flags:**
  * `-t <type>`: Specify media type (e.g., `dos`, `gpt`)
  * `-i <format>`: Image format (e.g., `raw`, `ewf`)
* **Example:**
  ```bash
  mmls -t gpt evidence.raw
  ```

---

### `fls` – Directory Listing

* **Syntax:**
  ```bash
  fls [options] image.dd [offset]
  ```
* **Flags:**
  * `-r`: Recursive
  * `-p`: Display full path
  * `-d`: Deleted entries only
  * `-o <sector_offset>`: Partition sector offset
* **Example:**
  ```bash
  fls -r -p -o 2048 image.dd
  ```

---

### `icat` – Extract File by Inode

* **Syntax:**
  ```bash
  icat [options] image.dd <inode_number>
  ```
* **Flags:**
  * `-o <sector_offset>`: Partition sector offset
  * `-r`: Recover deleted data if possible
* **Example:**
  ```bash
  icat -o 2048 image.dd 14209 > extracted_file.exe
  ```

---

### `fsstat` – File System Details

* **Syntax:**
  ```bash
  fsstat [options] image.dd
  ```
* **Flags:**
  * `-o <sector_offset>`: Partition sector offset
* **Example:**
  ```bash
  fsstat -o 2048 image.dd
  ```