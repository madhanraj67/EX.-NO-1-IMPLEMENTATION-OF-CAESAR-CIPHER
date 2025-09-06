# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main() {
    char text[100], ch;
    int key, i;
    printf("Enter a plain text: ");
    fgets(text, sizeof(text), stdin);
    
    text[strcspn(text, "\n")] = '\0';
    
    printf("Enter key (integer): ");
    scanf("%d", &key);

    printf("Encrypted text: ");
    for (i = 0; text[i] != '\0'; ++i) {
        ch = text[i];

        if (isalpha(ch)) {
            char base = isupper(ch) ? 'A' : 'a';
            ch = ((ch - base + key) % 26 + 26) % 26 + base; 
        }

        printf("%c", ch);
    }

    printf("\n");

    printf("Encryption complete.\n");

    return 0;
}

```

## OUTPUT:
<img width="1920" height="1080" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/3f6a7d25-3fd5-4900-b43e-d29aa83b9f4d" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
