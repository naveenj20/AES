# NAME: NAVEEN JAISANKER
# REG. NO.: 212224110039

# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:

```
#include <stdio.h>
#inclpude <string.h>
int main() {
 char text[100], key[100], result[100];
 int i, len, klen;
 printf("Enter text: ");
 scanf("%s", text);
 printf("Enter key: ");
 scanf("%s", key);
 len = strlen(text);
 klen = strlen(key);
 // Encryption
 for(i = 0; i < len; i++) {
 result[i] = text[i] ^ key[i % klen];
 }
 result[len] = '\0';
 printf("Encrypted ASCII: ");
 for(i = 0; i < len; i++) {
 printf("%d ", (unsigned char)result[i]);
 }
 // Decryption
 for(i = 0; i < len; i++) {
 result[i] = result[i] ^ key[i % klen];
 }
 printf("\nDecrypted Text: %s\n", result);
 return 0;
}
```

# OUTPUT:
<img width="1480" height="746" alt="image" src="https://github.com/user-attachments/assets/e1e0afd8-5e30-4493-895a-dfc8dcdf3444" />


# RESULT:

Thus, the program was implemented successfully.
