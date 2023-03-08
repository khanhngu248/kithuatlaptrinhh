#include <stdio.h>
#include <ctype.h>

void countCharacters(char* str)
{
    int vowels = 0, consonants = 0, digits = 0, spaces = 0;

    for (int i = 0; str[i] != '\0'; i++)
    {
        char ch = tolower(str[i]);
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u')
            vowels++;
        else if (ch >= 'a' && ch <= 'z')
            consonants++;
        else if (ch >= '0' && ch <= '9')
            digits++;
        else if (ch == ' ')
            spaces++;
    }
	 
    printf("So nguyen am: %d\n", vowels);
    printf("So phu am: %d\n", consonants);
    printf("So chu so: %d\n", digits);
    printf("So khoang trong: %d\n", spaces);
}
int main()
{
    char str[] = "Hello World 123";
    countCharacters(str);
    return 0;
}
