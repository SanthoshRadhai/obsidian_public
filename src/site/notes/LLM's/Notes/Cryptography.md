---
{"dg-publish":true,"permalink":"/llm-s/notes/cryptography/","noteIcon":"","dg-note-properties":{}}
---

> Cryptography is the practice of developing and using coded algorithms to protect and obscure transmitted information so that it may only be read by those with the permission and ability to decrypt it. Put differently, cryptography obscures communications so that unauthorized parties are unable to access them.

Source [IBM](https://www.ibm.com/think/topics/cryptography)

### Basic Principle of Cryptography 

![Pasted image 20261015191033.png](/img/user/LLM's/__Support/Pasted%20image%2020261015191033.png)

Source : [wallarm](https://www.wallarm.com/what/cia-triad-definition)

Cryptography can be categorized in to two major categories:
1. Encryption and Decryption 
	1. Symmetric Key Structure 
	2. Asymmetric Key structure 
2. Digital Signature 

### Symmetric and Asymmetric Encryption


![Pasted image 20261015201328.png](/img/user/LLM's/__Support/Pasted%20image%2020261015201328.png)


![Pasted image 20261015201402.png](/img/user/LLM's/__Support/Pasted%20image%2020261015201402.png)

Source : [Link](https://sectigostore.com/blog/types-of-encryption-what-to-know-about-symmetric-vs-asymmetric-encryption/)
## Digital Signature 

![Pasted image 20261015200731.png](/img/user/LLM's/__Support/Pasted%20image%2020261015200731.png)

source : [link](https://blog.bugzero.io/what-are-digital-signatures-a6a9f46f1285?gi=0279bd56caec)

![Pasted image 20261015200832.png](/img/user/LLM's/__Support/Pasted%20image%2020261015200832.png)

Source : [link](https://webnic.cc/cyber-security/understand-what-is-a-digital-signature-and-its-benefits/)

Often beginners will confuse the usage of public and private key when they are first learning cryptography. 

In Asymmetric Encryption Algorithm: 
1. Public Key : Used to encrypt the Text 
2. Private Key : Used to decrypt the Cipher 

In Asymmetric Signature Algorithms: 
1. Public Key : Used to decrypt the Hash (verification)
2. Private Key : Used to encrypt the Hash (signing)

