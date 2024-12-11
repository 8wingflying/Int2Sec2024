# Network_CTF_101
### NET1  20
```
封包分析最簡章
請使用工具解析側錄的封包

Linux: file strings
Windows:strings

題目來源: CSAW Quals CTF 2013: Networking 1
```
- 下載分析檔案
  - [NET1]()
- 使用windows/sysinternals的strings工具分析檔案
  - [sysinternals的strings下載點](https://learn.microsoft.com/en-us/sysinternals/downloads/strings)
### NET2  30
```
Someone intercepted a chat between illustris and codelec

BITSCTF 2017 : woodstock-1-10
```
- 下載分析檔案
  - []()
### NET3_Wireshark封包分析  80
```
The shark won't bite you. Don't worry, it's wired!
鯊魚不會咬你.別擔心 .這是有線網路的(鯊魚)

答案格式:IW{xxxxxxxxxxxxxxx}

題目來源:Internetwache-CTF-2016:Network Forensic(MUST)
```
- 下載分析檔案
  - []()
  - []() 
### NET4_Special Agent User(MUST)  70
```
We can get into the Administrator's computer with a browser exploit.
But first, we need to figure out what browser they're using.
Perhaps this information is located in a network packet capture we took: data3.pcap.
Enter the browser and version as "BrowserName BrowserVersion".

NOTE: We're just looking for up to 3 levels of subversions for the browser version
(ie. Version 1.2.3 for Version 1.2.3.4) and
ignore any 0th subversions (ie. 1.2 for 1.2.0)

PicoCTF_2017: Special Agent User(MUST) Hint:

Where can we find information on the browser in networking data?
Maybe try reading up on user-agent strings.
```
- 下載分析檔案
  - []()

## windows版的strings
```
strings64.exe /?

Strings v2.54 - Search for ANSI and Unicode strings in binary images.
Copyright (C) 1999-2021 Mark Russinovich
Sysinternals - www.sysinternals.com

usage: strings64.exe [-a] [-f offset] [-b bytes] [-n length] [-o] [-s] [-u] <file or directory>
-a     Ascii-only search (Unicode and Ascii is default)
-b     Bytes of file to scan
-f     File offset at which to start scanning.
-o     Print offset in file string was located
-n     Minimum string length (default is 3)
-s     Recurse subdirectories
-u     Unicode-only search (Unicode and Ascii is default)
-nobanner
       Do not display the startup banner and copyright message.
```
