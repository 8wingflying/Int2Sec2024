# HASH
- [An Illustrated Guide to Cryptographic Hashes](http://www.unixwiz.net/techtips/iguide-crypto-hashes.html)
- [MD5 Hash Generator](https://codebeautify.org/md5-hash-generator)
# 著名的HASH FUNCTION
- MD4
  - Rivest(1990) | 雜湊值的長度為128 位元(RFC 1186 ，修改版RFC 1320)
    - R. L. Rivest, "The MD4 message digest algorithm", Advances in Cryptology - CRYPTO 90, vol. LNCS 537, pp. 303-311, 1991.
    - R. L. Rivest, The MD4 Message Digest Algorithm, Request for Comments (RFC)1320, Internet Activities         
 Board, Internet Privacy Task Force, April 1992.
  - 不安全!已被破~ Dobbeertin 發現了MD4 雜湊值的碰撞方法，所以並不安全。
    - 論文 [Cryptanalysis of MD4 |Hans Dobbertin (1998)](https://link.springer.com/article/10.1007/s001459900047)
- MD5
  - Rivest (1991) |雜湊值的長度為128 位元(RFC l321)
  - 不安全!已被破~ MD5 的強碰撞抵抗性已經被破解
    - [Wang, Xiaoyun; Feng, Dengguo; Lai, Xuejia; Yu, Hongbo. Collisions for Hash Functions MD4, MD5, HAVAL-128 and RIPEMD](https://eprint.iacr.org/2004/199.pdf)
    - [MD5 Collision Demo](https://www.mscs.dal.ca/~selinger/md5collision/)
- SHA-1
  - NIST (National Institute of Standards and Technology)
  - 雜湊值的長度為160 位元
  - 1993 年美國發表 FIPS PUB 180 稱為SHA
  - 1995 年發表的修改版FIPS PUB 180-1 稱作SHA-1
  - 不安全!已被破~2005 年SHA-I 的強碰撞抵抗性被破解
    - 2005年，密碼分析人員發現了對SHA-1的有效攻擊方法，這表明該算法可能不夠安全，不能繼續使用
    - 2017年2月23日，CWI Amsterdam與Google宣布了一個成功的SHA-1碰撞攻擊，發布了兩份內容不同但SHA-1散列值相同的PDF文件作為概念證明。
    - https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html
    - 2020年，針對SHA-1的選擇前綴衝突攻擊已經實際可行。建議盡可能用SHA-2或SHA-3取代SHA-1。
- SHA-2
  - NIST (National Institute of Standards and Technology)
  - SHA-256 、SHA-384 、SHA-512 雜湊值的長度分別是256 位元、384 位元、512 位元。這些單向雜湊函數統稱為SHA-2
  - 訊息的長度有限制(SHA-256 是不超過264 位元， SHA-384 與SHA-512 是不超過2128 位元)
  - 這些SHA-2單向雜湊函數與SHA-1 公開為FIPS PUB 180-2(2002年)
- RIPEMD-160
  - European Union PIPE 計畫設計出的RIPEMD
  - RIPEMD-160是RIPEMD修訂版,雜湊值長度為160 位元
  - Hans Dobbertin 、Antoon Bosselaers 、Bart Preneel(1996)
  - 還有RIPEMD-128 、RIPEMD-256 、RIPEMD-320 等版本
  - RIPE MD 的強碰撞抵抗性在2004 年被破解，但是RIPEMD-160 還未被破解
  - 比特幣使用RIPEMD-160
- SHA-3	NIST (National Institute of Standards and Technology)
  - 2007|2012(KECCAK 演算法)
  - SHA-3 在2015年8月5日由 NIST 通過 FIPS 202 正式發表

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
