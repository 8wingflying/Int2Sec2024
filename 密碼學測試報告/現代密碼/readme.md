# 現代密碼
- 現代密碼
  - 對稱式密碼
  - 非對稱式密碼
  - HASH  
- 現代密碼實戰: Openssl
- 現代密碼實戰: python

### HASH實戰 ==> Colab 實戰20241211
- MD5
- SHA

```
# 安裝好用的終端機
!pip install colab-xterm
%load_ext colabxterm

# 執行終端機
%xterm
```

```
echo abcd > text1.txt
echo Abcd > text2.txt
md5sum text1.txt
md5sum text2.txt
```
- 結果 == > md5值 128-bit
f5ac8127b3b6b85cdc13f237c6005d80  text1.txt
0d437fe5c2231b53b8fc3dc2bae7ac93  text2.txt
