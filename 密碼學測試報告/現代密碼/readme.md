# 現代密碼
- 現代密碼
  - [對稱式密碼](SCrypto.md)
  - [非對稱式密碼](ASCrypto.md)
  - HASH  
- 現代密碼實戰: Openssl
- 現代密碼實戰: python

### HASH實戰 ==> [Google Colab](https://www.bing.com/ck/a?!&&p=df35b712f5207f6766574b2326de495a456593721e468c9694e5e581bcd4c1eeJmltdHM9MTczMzk2MTYwMA&ptn=3&ver=2&hsh=4&fclid=344f7df4-2fec-6017-0edf-69fe2e40610b&psq=google+colab&u=a1aHR0cHM6Ly9jb2xhYi5yZXNlYXJjaC5nb29nbGUuY29tLw&ntb=1) 實戰20241211
- MD5
- SHA
```
# 安裝好用的終端機
!pip install colab-xterm
%load_ext colabxterm

# 執行終端機
%xterm
```
- 1.實戰1:md5sum
```
echo abcd > text1.txt
echo Abcd > text2.txt
md5sum text1.txt
md5sum text2.txt
```
- 結果 == > md5值 128-bit
```
f5ac8127b3b6b85cdc13f237c6005d80  text1.txt
0d437fe5c2231b53b8fc3dc2bae7ac93  text2.txt
```
- 2.實戰2:sha1sum
```
sha1sum --help
Usage: sha1sum [OPTION]... [FILE]...
Print or check SHA1 (160-bit) checksums.

With no FILE, or when FILE is -, read standard input.

  -b, --binary         read in binary mode
  -c, --check          read SHA1 sums from the FILEs and check them
      --tag            create a BSD-style checksum
  -t, --text           read in text mode (default)
  -z, --zero           end each output line with NUL, not newline,
                       and disable file name escaping

The following five options are useful only when verifying checksums:
      --ignore-missing  don't fail or report status for missing files
      --quiet          don't print OK for each successfully verified file
      --status         don't output anything, status code shows success
      --strict         exit non-zero for improperly formatted checksum lines
  -w, --warn           warn about improperly formatted checksum lines

      --help     display this help and exit
      --version  output version information and exit

The sums are computed as described in FIPS-180-1.  When checking, the input
should be a former output of this program.  The default mode is to print a
line with checksum, a space, a character indicating input mode ('*' for binary,
' ' for text or where binary is insignificant), and name for each FILE.

Note: There is no difference between binary mode and text mode on GNU systems.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/sha1sum>
or available locally via: info '(coreutils) sha1sum invocation'
```
```
sha1sum text1.txt
sha1sum text2.txt
```
```
3330b4373640f9e4604991e73c7e86bfd8da2dc3  text1.txt
0bc2657454886e834c9ad875194f728239122b5f  text2.txt
```

## [openssl](openssl.md)
```
openssl --help
```
