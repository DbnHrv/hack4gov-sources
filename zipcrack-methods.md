You cannot bypass or extract a password-protected ZIP file without finding the correct password first. The files inside are encrypted using algorithms like ZipCrypto or AES-256.

In Kali Linux, unlocking a password-protected ZIP involves **recovering (cracking) the password** using built-in utilities like **John the Ripper** (`zip2john`) or **Hashcat**, and then extracting the archive.

---

### Method 1: Using John the Ripper (Recommended & Pre-installed)

John the Ripper is the standard tool in Kali Linux for recovering archive passwords.

#### 1. Extract the Hash
First, extract the password hash from the encrypted ZIP file into a text file using `zip2john`:

```bash
zip2john protected_file.zip > zip_hash.txt
2. Crack the Hash with a Wordlist
Use john with a dictionary wordlist (such as rockyou.txt, which comes with Kali):

Note: If rockyou.txt is compressed on your system, decompress it first:
sudo gzip -d /usr/share/wordlists/rockyou.txt.gz

Run John the Ripper:

Bash
john --wordlist=/usr/share/wordlists/rockyou.txt zip_hash.txt
3. View the Recovered Password
Once the process completes, show the cracked password:

Bash
john --show zip_hash.txt
4. Unzip the File
Extract the archive using the password found in step 3:

Bash
unzip protected_file.zip
Method 2: Using Hashcat (GPU-Accelerated)
If you have GPU acceleration enabled or need a faster cracking process, use Hashcat.

Extract the hash format:

Bash
zip2john protected_file.zip > zip_hash.txt
Clean the hash:
Open zip_hash.txt in a text editor and keep only the hash section starting from $zip2$ up to the end of the line (remove the filename prefix).

Identify the Hash Type:

PKZIP / ZipCrypto: Mode 13600

WinZip AES-128: Mode 13711

WinZip AES-192: Mode 13721

WinZip AES-256: Mode 13731

Run Hashcat:

Bash
hashcat -m 13600 -a 0 zip_hash.txt /usr/share/wordlists/rockyou.txt