#include <stdio.h>

char* StrChr(const char* pstring, char ch);

void main(void)
{
	char string[100];
	char* pos;

	strcpy(string, "this is a book");
	pos = strchr(string, 'a');
	printf("%d 위치에 a가 있음\n", pos - string);

	strcpy(string, "this is a book");
	pos = strchr(string, 'a');
	printf("%d 위치에 a가 있음\n", pos - string);
}

char* StrChr(const char* pstring, char ch)
{
	while (*pstring && *pstring != ch)
	{
		pstring++;
	}

	if (*pstring == ch)
	{
		return(char*)pstring;
	}

	return(char*)0;
}
