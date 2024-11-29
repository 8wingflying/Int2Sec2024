# 密碼學上課內容
- [古典密碼](./古典密碼.md)
# 密碼學測試報告
- 密碼學
  - 1.密碼學基本觀念
    - 加密 vs 解密 vs 破密
    - 明文(plaintext)  vs 密文(cipher text)
  - 2.密碼學類型
    - 古典密碼:
    - 現代密碼:以難解的數學問題建構的密碼學<==(安全基礎)
      - RSA 公開金鑰 ==> 質因數分解 ==> 可被量子電腦秒殺 
    - 量子密碼:以量子力學基本原理建構的密碼學<==(安全基礎)
    - 後量子密碼 ==>建構不會被量子電腦攻破的密碼學
  - 3.古典密碼學
    - 凱撒密碼
    - 維吉尼亞密碼 
  - 4. CTF搶旗大賽解題
      
- 現代密碼學
  - 對稱式密碼
  - 非對稱式密碼
  - Hash 
- 現代密碼學實測:openssl
- 現代密碼學實測:python
  - Python Cryptography Toolkit (pycrypto) https://pypi.org/project/pycrypto/
  - 舊版 PyCrypto 與新版 [PyCryptodome 模組](https://github.com/Legrandin/pycryptodome)
    - pip install pycryptodome
    - pip install pycryptodomex
    - https://pypi.org/project/pycryptodome/
- 現代密碼學破密分析
  - 非對稱式密碼的攻擊
  - Hash 的攻擊

## 延伸閱讀
- [加密‧解謎‧密碼學：從歷史發展到關鍵應用，有趣得不可思議的密碼研究 密碼了不起 |劉巍然 著](https://www.tenlong.com.tw/products/9786267195239?list_name=srh)
- [深入淺出密碼學 Real-World Cryptography| 戴維·王（David Wong）](https://www.tenlong.com.tw/products/9787115600349?list_name=srh)
- [圖解密碼技術 第3版 |[日]結城浩](https://www.tenlong.com.tw/products/9787115424914?list_name=sp)
- [嚴肅的密碼學：實用現代加密術 | Jean-Philippe Aumasson ](https://www.tenlong.com.tw/products/9787121410864?list_name=srh)
  - Serious Cryptography: A Practical Introduction to Modern Encryption
- [寫給工程師的密碼學 |Robert Schmied](https://www.tenlong.com.tw/products/9787111716631?list_name=srh)
  - Cryptology for Engineers: An Application-Oriented Mathematical Introduction
- 密碼實作
  - [Python 密碼學編程, 2/e |Al Sweigart](https://www.tenlong.com.tw/products/9787115529992?list_name=srh) 
  - [應用密碼學原理、分析與Python實現 |劉卓 趙勇焜 黃領才](https://www.tenlong.com.tw/products/9787115635716?list_name=srh)
  - [應用密碼學：協定、演算法與C源程式（原書第2版·典藏版）| Bruce Schneier](https://www.tenlong.com.tw/products/9787111748878?list_name=srh)
    - Applied Cryptography: Protocols, Algorithms and Source Code in C 20th Anniversary Edition
  - [高手才用 C語言：Windows C/C++ 加密解密實戰|朱晨冰、李建英](https://www.tenlong.com.tw/products/9789860776348)
