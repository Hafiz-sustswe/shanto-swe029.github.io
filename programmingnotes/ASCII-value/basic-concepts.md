[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# ASCII Value : Basic Concepts

***

In every programming languages, **ASCII Value** is an important basic thoery. Programmers have to feel comfortable using **ASCII Value**s. So, every programmer should know **what they can do using ASCII values**. So, let's begin!

### Characters & ASCII Values

In C or C++ Programming Language, when we store a chartacter into a character type variable, that variable basically stores the ASCII Value of that character. That means if we write that `char ch = 'A'`, then `ch` basically stores the ASCII value of the character `'A'` and that is 65. Let's run the following code.

```c
	int main()
	{
		char ch = 'A';
		printf("The character is : %c.", ch);
		reutrn 0;
	}
```

We all know that the output will be :-

	The character is A.

The ASCII values of the characters from `A` to `Z` are from 65 to 90. So the ASCII value of `B` is 66, `C` is 67, `D` is 68 and so on...

Let's guess the output of the following code :-

```c
	int main()
	{
		char ch1 = 'A';
		char ch2 = ch1 + 1;
		printf("The second character is %c.", ch2);
		return 0;
	}
```

What is the output? Is it `B` ? Yes, it is. Because, `ch1` stored the ASCII value of `A` that is 65. `ch2` stores `ch1 + 1` and that is 66. So, the output will be :-

	The second character is B.

As we are saying that `character variables store ASCII values`, can we print that value using these character variables? Yes, we can. See the following code :-

```c
	int main()
	{
		char ch = 'A';
		printf("%d", ch);
		return 0;
	}
```

The output is `65`, isn't it? 

So if we use `%d` instead of `%c`, `printf()` function will print the ASCII value that is stored in the character variable. So, if you want to know the ASCII value of, suppose, `K`, just write `char ch = 'K'` in the previous code instead od `char ch = 'A'`. 

You can see that we can print the character variable as an integer value. Can we do the reverse thing? That means I am asking you about the output of the following code:-

```c
	int main()
	{
		int x = 65;
		printf("%c", x);
		return 0;
	}
```

Before you run this code or read more of this article, please decide a `yes` or `no` for this qoute - "The output will be `A`."

Yes, the output will be `A`. Because we are printing x as a character, so `printf()` function will print the equivalent character whose ASCII value is 65. Som if I ask you to tell me the character whose ASCII value is 85, you might write the previous code using `x = 85`! So, this is how you can find the equivalent character of an ASCII value.

Now, we know that we can print an integer like a character and vice-versa. But we must also know that ASCII range is from 0 to 255. Now you might be wondering what happens if we assign the value of x > 255 in the previous code! Well, you are welcome to write that code so see the changes! And you should write the code! After you write this or not, let's move to the next section!

***

## Alphabets & ASCII Values

We know that ASCII values of the characters from 'A' to 'Z' is from `65 to 90`. We must know another information that ASCII values of the characters from 'a' to 'z' is from `97 to 122`.

Now we can observe that :-

	'a' = 97	&	'A' = 65	>>	97 - 65 = 32	>>	'a' - 'A' = 32;
	'b' = 98	&	'B' = 66	>>	98 - 66 = 32	>>	'b' - 'B' = 32;
	'c' = 99	&	'C' = 67	>>	99 - 67 = 32	>>	'c' - 'C' = 32;
	...
	...
	'z' = 122	&	'Z' = 90	>> 122 - 90 = 32	>>	'z' - 'Z' = 32;

So, `32` is a very important number for us. As you see the right most column, **difference of same upper case and lower case character is 32 and it is constant for all of the 26 alphabets.** Now we can use it for some very good purposes. Let's see.

- Lower Case to Upper case
	- let's see this code:-
		```c
			int main()
			{
				char ch = 'a';
				ch = ch - 32;
				printf("%c", ch);
				return 0;
			}
		```
		
		Of course, the output is `A`. So be smart to use this!
- Upper case to lower case
	- let's see this code:-
		```c
			int main()
			{
				char ch = 'A';
				ch = ch + 32;
				printf("%c", ch);
				return 0;
			}
		```
		
		The output is `a`.

So, these are the basic concepts of ASCII vlaues in programming language. You might want to see [The Basic Applications](https://shanto-swe029.github.io/programmingnotes/ASCII-value/basic-applications) of ASCII value.

Thank you for reading! If you have any suggestions, you can send me an email at `ariful.shanto786@gmail.com` or instead leave a message for me at my [Facebook ID](https://facebook.com/shanto3585).

***

## Happy Coding!

***

`This page is maintained by Ariful Islam Shanto`
