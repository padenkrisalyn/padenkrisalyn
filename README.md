
#include <stdio.h>
#include <stdlib.h>
void main ()
{
  FILE * fp;
  int i,n;
  char str[100];
  char fname[20];
	printf(" Input the file location : ");
	scanf("%s",fname);
    fp = fopen(fname, "a");
    printf("Input how many lines to be appended : ");
    scanf("%d", &n);
    for(i = 0; i < n+1;i++)
    {
    fgets(str, sizeof str, stdin);
    fputs(str, fp);
    }
    fclose(fp);
    
}
