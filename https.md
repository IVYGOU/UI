            

**https就是套在SSL/TLS内的http，也就是安全的http。**     

**SSL/TLS**：
Transport Layer Security (TLS) and its predecessor, Secure Sockets Layer (SSL), both frequently referred to as "SSL", are cryptographic protocols that provide communications security over a computer network.                  
(https://en.wikipedia.org/wiki/Transport_Layer_Security)      

何为安全？一个安全的网络通信环境要解决3个问题：
- 通信内容的保密
- 通信双方身份不可伪造
- 通信内容不被篡改

## 1. 通信内容的保密
非对称加密算法：需要两个密钥来进行加密和解密，这两个秘钥是公开密钥（public key，简称公钥）和私有密钥（private key，简称私钥）。

公钥加密，私钥解密。



## 2. 通信双方身份不可伪造
所有加密通信都要带上一个证书，用来证明自己的身份。证书上的公章也是非对称加密过的。公章就是证书的数字签名，具体来说就是先将证书用哈希算法提取摘要，然后对摘要进行加密的过程。        

私钥加密，公钥解密。


## 3. 通信内容不被篡改
先用哈希算法提取内容摘要，然后对摘要进行加密生成数字签名，验证数字签名就可以判断出通信内容的完整性。

Origin:https://zhuanlan.zhihu.com/p/24854237    
