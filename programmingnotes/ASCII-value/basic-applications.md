[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# ASCII Value : Basic Applications

Here we will see some basic operations we can make with the help of the concept of ASCII values. This part is so much important for programmers. So, let's begin!

### Strategy-01

- Suppose, a user will give an input of a character between 'a and 'z' or between 'A' and 'Z'. We'll have to convert it to **upper case** character.

We can solve it easily by using `conditional statement`. Let's see the code:-

```c
	int main()
	{
		char ch;
		scanf("%c", &ch);
		if( ch >= 97 ) {
			ch = ch - 32;
			printf("Converted character: %c.", ch);
		}
		else {
			printf("Converted character: %c.", ch);
		}
		return 0;
	}
```

We can also write the similar code like this :- 

```c
	int main()
	{
		char ch;
		scanf("%c", &ch);
		
		if( ch >= 97 ) {
			ch = ch - 32;
		}
		
		printf("Converted character: %c.", ch);
		return 0;
	}
```

However you write, the output is still the same.

	Input:
	r
	Output:
	Converted character: R.
	
	Input:
	R
	Output:
	Converted character: R.



### Strategy-02

- Suppose, a user will give an input of a character between 'a and 'z' or between 'A' and 'Z'. We'll have to convert it to **lower case** character.

`I am leaving this one for you to practice.`


### Strategy-03

- Converet all characters of a string to `lower case` or to `upper case` and print it.

	- Case-01 : Convert To Lower Case
	
		```c
			#include <stdio.h>
			#include <string.h>
			int main()
			{
				char str[] = "My_NaMe_Is_ShAnTo";
				printf("Before conversion : %s\n", str);
				int n = strlen(str);
				for(int i = 0; i < n; i++) {
					if(str[i] >= 'A' && str[i] <= 'Z') {
						str[i] += 32;
					}
				}
				printf("After conversion : %s\n", str);
			}
		```
		
			Output:
			Before conversion : My_NaMe_Is_ShAnTo
			After conversion : my_name_is_shanto

	- Case-02 : Convert To Upper Case
		You should write this code by your own.
		So, I am leaving it for you.


Now I have a task for you. **"You have to write a code which converts a whole string to upper or to lower lase using function. You have to scan the string inside the function and you will convert it inside that function and then the function will return the converted string to the main function. Main function will receive the string from the user defined function and print the function."** A layout is given below :

```c
	#include <stdio.h>
	#include <string.h>
	Your_funciton_here()
	{
		//scan the string here.
		//convert the string here.
		//return the string to the main function
	}
	
	int main()
	{
		//call Your_function_here & receive the converted string
		//print the converted string here
	}
```




[in progress...]




***

## Happy Coding!

***

`This page is maintained by Ariful Islam Shanto`
