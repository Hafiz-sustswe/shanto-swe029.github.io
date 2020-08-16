<a href = "https://shanto-swe029.github.io/"> <img src = "https://shanto-swe029.github.io/newgitphoto/home.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingnotes.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/mathematicsnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/mathematicsnotes.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/programmingproblems"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingproblems.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/must-do-math-cp/home"> <img src = "https://shanto-swe029.github.io/newgitphoto/mustdomathforcp.png" height = "80"> </a>

***


# Store Large Numbers & Count Number Of Digits

***

Did you know that one of the most important limitations in `C Programming` or `C++ Programming` is **we cannot use numbers larger than 10^19**?
<br>

Whatever, you knew it or not, now you do. So **what can we do to overcome this limitation so that we can store a number than greater than that range?** Suppose, we need to scan a 100 digit number and print it. So, how do we do it? **Here comes the concept of `string`.**
<br>

Let's see a simple code!

```c
	#include <stdio.h>
	#include <string.h>
	
	int main()
	{
		char num[1000];
		scanf("%s", num);
		printf("The number is %s\n", num);
		return 0;
	}
```

	Input:
	1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111
	
	Output:
	1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111


So, here we go! Scanning the number as a string, we can store bigger numbers in this way! But **what is the largest number we can store in a string?**
- A string can store around 10^7 characters (varies from version to version of the language). So you can store a 10^7 digit number in a string! Can you imagine the number which has 10^7 digits! Like the biggest number you can store is **999......999 (10^7 nines!)**. So string is very much helpful for storing very much large numbers while using `long long` / `unsigned long long`, you can use upto 18 digit numbers.
<br>

### How many digits are there in a number?

- We can write a code for this number in 2 ways:-
	- Using Modular Arithmetics (if the number is less then 10^19)
	- Using String

Well, if you wanna count how many digits are there using modular arithemtics, you have do it like this :-

```c
	int main()
	{
		long long n;
		n = 12345;	//you can use scanf()
		long long r, q = n, count = 0;
		while(q > 0) {
			r = q % 10;
			q = q / 10;
			count++;
		}
		printf("%lld has %lld digits", n, count);
		reutrn 0;
	}
```

	Output:
	12345 has 5 digits

Using string, you can solve it easily in this way :-

```c
	#include <stdio.h>
	#include <string.h>
	
	int main()
	{
		char num[] = "12345";
		long long len = strlen(num);	// To use strlen() function, we have to use <string.h>
		printf("%s has %lld digits", num, len);
		return 0;
	}
```

	Output:
	12345 has 5 digits

***

**So, feel free to use string!"

***

## Happy Coding!

***

`This page is maintained by Ariful Islam Shanto`












