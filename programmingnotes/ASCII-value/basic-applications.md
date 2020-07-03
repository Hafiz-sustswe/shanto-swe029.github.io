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

[in progress...]




***

## Happy Coding!

***

`This page is maintained by Ariful Islam Shanto`
