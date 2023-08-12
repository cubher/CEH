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
plain txt xor with key(which has expanded to make 11 rounds) and then converted into subytes(function which will substitute every bytes(SPN)) and then shifting rows and columns and again the above process is reapeated till last round where the mixing of row and col wont perform.
block size 128
key 128 196 256
*substitution permutation network
key 128 is more efficient since both 128 and 256 never been cracked so 128 is more power effective

DES(block)
------------------
works by Feistel cipher()
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
(paint exchange)

asymmetric 
--


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
