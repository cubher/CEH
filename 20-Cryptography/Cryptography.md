# keys for challenges https://pwn.college/cse365-s2023/cryptography

Theory 
----
CID
Block Cipher and Stream(character) Cipher belongs to the symmetric key cipher.

symmetric
----------------------------
one time pad (stream chiper) - uncrackable technique mathematically with certain conditions. basicallly works on XOR. key should be => then plaintext.
https://www.youtube.com/watch?v=rCeWtQERizA&t=836s
-----------------------------
properties for good encryption
* confusion - small change in the key should change the chipertext
* diffusion - small change in plain text should change the chipertext
-----------------------------
AES (Block Cipher) 
-------------------------
plain txt xor with key(which has expanded to make 11 rounds) and then converted into subytes(function which will substitute every bytes(SPN)) and then shifting rows and columns and again the above process is repeated till last round where the mixing of row and col wont perform.
block size 128
key 128 196 256
*substitution permutation network
key 128 is more efficient since both 128 and 256 never been cracked so 128 is more power effective
![[Pasted image 20230813103405.png]]
DES(block)
------------------
works by Feistel cipher( it is a framework on which every crypto works)
block size 64
key 48
![[Pasted image 20230812183727.png]]

ECB (electronic codebook)
-------
just block cipher 
pattern will repeat
CBC (cipher block chaining)
---
block cipher but they are linked (xor the result with nxt block)
but the output has to wait for prev output
CTR - counter
---
instead of prev result it uses some counter
one solution for overcoming parallels computing
Key exchange
---
DH key exchange
---
(paint exchange)
modulas (%)
eg. (7^n)%25 
![[Pasted image 20230813094523.png]]
![[Pasted image 20230813094556.png]]
asymmetric 
--
RSA
--
similar to DH key exchange
https://www.youtube.com/watch?list=PL-ymxv0nOtqpBYQKnbivatYlfQ3Ygf63_&v=661MFqOp0WA

HASH
--
sha256
proof of work

trust:
hashing
rsa public and private key 

=======================================================
challenges
lvl
1- pwn.college{I4wHOxEABo-7EkmmFwaxEGK3AF7.dNzNzMDL2cjNzIzW}
2 -pwn.college{k8960W1WAPvCbtd36_763lBuHdX.dRzNzMDL2cjNzIzW}
first converted base64 to hex and then xor ed and convered hex to base64 to decode
3- pwn.college{sUJka5twA39_BoFUdlTCL9ySJqe.dVzNzMDL2cjNzIzW}
just input the given cipher
4-


=======================================================
1.

###########################################################################
CEH book

types
-substitution
-transposition
- based on key
-based on type of input data
 ---(block)DES AES IDEA
 ---(stream)RC4  SEAL

cryptanalysis
-linear 
-differential
-integral

breaking technique
-brute force
-frequency analysis
-trickery and deceit


birthday paradox or pigeon hole

meet in the middle
E1(E2(plain txt, key),key)
attacker tries to encrypt with random key which give output of E1
and also he tries to decrypt E2 backwards, if both output is same then key is found

side channel attack 
physical environmental factors affect the crypto hardware and software

hash collision

DUHK(dont use hard coded keys) vuln
random number generator

vaudenay(padding oracle attack)
exploits padding validatinon of encrypted messsage

ssl and tsl

tsl is upgraded version of ssl 
tsl uses DH key exchange , rsa , aes, sha356
ssl used older key exchange, Des , sha1


pgp (pretty good privacy (normal aesymentric key))
gnu privacy guard(normal digital signature and encryption)
web of trust (instead of public key infrastructure (like blockchain))

further research
Duhk
DROWN attack (ssl breaking)
openssl
ipsec