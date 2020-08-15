[🏠Home](https://shanto-swe029.github.io/)
[✳️Programming Notes](https://shanto-swe029.github.io/programmingnotes)
[✴️Programming Problems](https://shanto-swe029.github.io/programmingproblems)
[🔢Mathematics Notes](https://shanto-swe029.github.io/mathematicsnotes)
[💻Must Do Math For Competitive Programmers](https://shanto-swe029.github.io/must-do-math-cp/home)

***

# How Many Integers Are There?

***

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/howmanyintegers/statement)

***

## Solution

- We have to solve this problem using `string`.

```c
	#include <stdio.h>
	#include <string.h>

	int main()
	{
    	int T;
    	scanf("%d", &T);
    	getchar();	// If we do not use this getchar then out program will scan the enter 
			// we press, after typing the value of T, as a string.

    	char str[1000000];
    	int i, len, count, flag; 		//flag = 1 >> paichi, flag = 0 >> pai nai

    	while(T--){
        	gets(str);
        	len = strlen(str);
        	count = 0;
        
        	for(i = 0; i < len; i++){
            	if(str[i] != ' '){
                	flag = 1;
            	}
            	else{
                	if(flag == 1){
                    	count++;
                	}
                	flag = 0;
            	}
        	}
        	printf("%d\n", count + 1);
    	}
    	return 0;
	}
```

***

`This page is managed by Ariful Islam Shanto`
