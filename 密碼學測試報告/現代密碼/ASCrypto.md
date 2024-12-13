# 非對稱式密碼

# RSA非對稱式密碼
- RSA加密演算法是一種非對稱加密演算法，在公開金鑰加密和電子商業中被廣泛使用
- 1977 年由 Ron Rivest, Adi Shamir 和 Leonard Adleman一起提出的，故取名為 RSA 。

## key Generation [Math Formula](https://www.luogu.com.cn/article/1gxob6zc)
- 隨意選取兩個大質數 p,q
- 計算出 N=p∗q
- 計算歐拉函數 :
  
   $ \phi =(p−1)∗(q−1)$

- 選擇一個 e ，必須與 phi 互質，並求出模反元素(Modular multiplicative inverse) 為 d ⇒ ed ≡1 mod phi

⇒  $d ≡e^{−1} mod \phi$

- 刪除  p 和 q
- 產生的kry pair
  - 公鑰 (Public Key) : ( N,e )
  - 私鑰 (Private Key) : ( N,d )

## 加解密

加密：

$ c≡ \m^{e} mod N $

解密：

$ m≡ \c^{d} mod N $


RSA 加密
c≡me mod N
m
 為明文，是一串個很大的數字，加密後的 c
 即為密文

加密流程：

隨意選取兩個大質數 p,q
 算出 N=p∗q

根據歐拉函數 :

phi=(p−1)∗(q−1)

選擇一個 e ，必須與 phi 互質，並求出模反元素(Modular multiplicative inverse) 為 d
⇒ ed ≡1 mod phi

⇒  d ≡e−1 mod phi

消滅 p 和 q

公鑰 (Public Key) 為 ( N,e )

私鑰 (Private Key) 為 ( N,d )


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


$\shortintertext{To prove RSA we must prove:} D(c) = D(E(m)) = (m^e)^d = m^{ed} \equiv m \pmod{n}\\$
$\shortintertext{Recall: $ed \equiv 1 \pmod{\phi{n}}$}  \\$
$\exists k \ni \to de-1 = (p-1)*(q-1)*k \\$
$\to ec = 1+k(p-1)(q-1)\\$
$\shortintertext{Case 1: $m$ divides $p$ and $p$ divides $m$, then $m = 0 \pmod{p} \land m^{ed} \equiv 0 \pmod{p}$} \\$
$\to m = m^{ed} \pmod{p} \text{ Then we are done}\\$
$\shortintertext{Case 2: $m \land p$ are relatively prime}$

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
