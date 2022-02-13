#### A Data Encryption Standard for a File System

#### **Objectives**
* Understanding the need of data security and integrity to be included during design of distributed operating system. 
* Types of cryptography modules used by different operating system store data and authorize users.
* Implement a file encryption technique using DES for the windows platform.
* Comparing the time and space aspects of decrypted file and encrypted file.

#### **Modules**
* A block cipher takes a block of plaintext bits and generates a block of ciphertext bits, generally of same size. The size of block is fixed in the given scheme. The choice of block size does not directly affect to the strength of encryption scheme. The strength of cipher depends up on the key length.

* Feistel Cipher is not a specific scheme of block cipher. It is a design model from which many different block ciphers are derived. DES is just one example of a Feistel Cipher. A cryptographic system based on Feistel cipher structure uses the same algorithm for both encryption and decryption.  

#### **How algorithm works?**

* The process begins with the 64-bit plain text block getting handed over to an initial permutation (IP) function.
* The initial permutation (IP) is then performed on the plain text.
*  Next, the initial permutation (IP) creates two halves of the permuted block, referred to as Left Plain Text (LPT) and Right Plain Text (RPT).
*  Each LPT and RPT goes through 16 rounds of the encryption process.
*  The encryption process (16 rounds) is further broken down into five stages:
    *  Key transformation
    *  Expansion permutation
    * S-Box permutation
    * P-Box permutation
    * XOR and swap
*	For decryption, we use the same algorithm, and we reverse the order of the 16 round keys.
*	Finally, the LPT and RPT are rejoined, and a Final Permutation (FP) is performed on the newly combined block.
*	The result of this process produces the desired 64-bit ciphertext.




