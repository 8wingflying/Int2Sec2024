# 非對稱式密碼 [wiki](https://en.wikipedia.org/wiki/Public-key_cryptography)
- 非對稱式密碼 | asymmetric key algorithms | Public-key cryptography
  - [Diffie–Hellman key exchange protocol](https://zh.wikipedia.org/wiki/%E8%BF%AA%E8%8F%B2-%E8%B5%AB%E7%88%BE%E6%9B%BC%E5%AF%86%E9%91%B0%E4%BA%A4%E6%8F%9B)
    - D-H密鑰交換是一種安全協議。
    - 它可以讓雙方在完全沒有對方任何預先資訊的條件下通過不安全通道建立起一個金鑰。
    - 這個金鑰可以在後續的通訊中作為對稱金鑰來加密通訊內容。
    - key exchange交換的概念最早由瑞夫·墨克（Ralph C. Merkle）提出
    - 這個密鑰交換方法，由惠特菲爾德·迪菲（Bailey Whitfield Diffie）和馬丁·赫爾曼（Martin Edward Hellman）在1976年首次發表。
    - 馬丁·赫爾曼曾主張這個密鑰交換方法，應被稱為迪菲-赫爾曼-墨克密鑰交換（Diffie–Hellman–Merkle key exchange）。 
  - DSS (Digital Signature Standard), which incorporates the Digital Signature Algorithm
  - ElGamal
  - Various elliptic curve techniques
- Various password-authenticated key agreement techniques
  - Paillier cryptosystem
  - RSA encryption algorithm (PKCS#1)
  - Cramer–Shoup cryptosystem
  - YAK authenticated key agreement protocol
- 不常被使用的 asymmetric key algorithms:
  - NTRUEncrypt cryptosystem
  - McEliece cryptosystem
- 著名但以已經不安全(notable – yet insecure) asymmetric key algorithms:
  - Merkle–Hellman knapsack cryptosystem

# RSA非對稱式密碼
- RSA加密演算法是一種非對稱加密演算法，在公開金鑰加密和電子商業中被廣泛使用
- 1977 年由 Ron Rivest, Adi Shamir 和 Leonard Adleman一起提出的，故取名為 RSA 。

## key Generation [Math Formula](https://www.luogu.com.cn/article/1gxob6zc)
- 隨意選取兩個大質數 p,q
- 計算出 N=p∗q
- 計算歐拉函數 :

  $$ \phi =(p−1)∗(q−1)$$

- 選擇一個 e ，必須與 phi 互質，並求出模反元素(Modular multiplicative inverse) 為 d

⇒  $ ed ≡1 mod \phi$

⇒  $d ≡e^{−1} mod \phi$

- 刪除  p 和 q
- 產生的kry pair
  - 公鑰 (Public Key) : ( N,e )
  - 私鑰 (Private Key) : ( N,d )

$$
A^{\phi y} \equiv (A^y)^{\phi} 
\equiv a^{\phi} \equiv 1 \mod N
$$

## 加解密

RSA 加密：  m ==為明文，是一串個很大的數字  加密後的 c 為密文

$$ c≡ m^{e} mod N $$

RSA 解密：  d 可以透過模反元素(inverse module) : invmod(e,phi) 計算出來

$$ m≡ c^{d} mod N $$


加密流程：



RSA 解密
m≡cd mod N
這個 d
 可以透過模反元素(inverse module) : invmod(e,phi) 計算出來

其實 d
 在做的事情也就是將 (e∗d) mod phi
 要等於 1

就是當： mx mod N
 時

只要 x
 每遇到 N
 的尤拉函數 Euler function ϕ
 的值： ϕ(N)
 就會被歸 0
 !!!


To prove RSA we must prove: 

$$ D(c) = D(E(m)) = (m^e)^d = m^{ed} \equiv m \pmod{n}$$

$\shortintertext{Recall: $ed \equiv 1 \pmod{\phi{n}}$}  $

\exists k \ni \to de-1 = (p-1)*(q-1)*k \\
\to ec = 1+k(p-1)(q-1)\\
\shortintertext{Case 1: $m$ divides $p$ and $p$ divides $m$, then $m = 0 \pmod{p} \land m^{ed} \equiv 0 \pmod{p}$} \\
\to m = m^{ed} \pmod{p} \text{ Then we are done}\\
\shortintertext{Case 2: $m \land p$ are relatively prime}$

舉個例子：

→
 假設 ϕ(N)
 為 60
，那麼 m120
 會等於 m0=1

→
 假設 ϕ(N)
 為 60
，那麼 m61
 會等於 m1=m


也就是： C=mx mod ϕ(N)mod N

C=med mod ϕ(N)mod N

所以只要找到一個數字 d
 乘上 e
 : 使得 ed mod ϕ(N)=1

那麼 cd=med=m1=m
 就能成功解密了。
# RSA非對稱式密碼: C 語言實作
# RSA非對稱式密碼: Python實作
