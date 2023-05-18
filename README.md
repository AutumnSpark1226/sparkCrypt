# sparkCrypt
A simple tool to encrypt files with GPG

## Encryption
1. hash file(s)
2. save original filename(s) and hash(es) to temporary metadata file
3. encrypt file(s) with GPG
4. randomly rename encrypted file(s)
4. hash encrypted file(s) and save hash(es) to temporary metadata file
5. encrypt metadata file
6. shred temporary metadata file
7. (optional) shred original file(s)

## Decryption
1. decrypt metadata file
2. validate hash of encrypted file(s)
3. decrypt file(s) with GPG
4. restore original filename(s)
5. validate hash of decrypted file(s)
6. shred decrypted metadata file
7. (optional) shred encrypted file(s)
