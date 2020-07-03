[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# ASCII Value : Basic Concepts

***

In every programming languages, **ASCII Value** is an important basic thoery. Programmers have to feel comfortable using **ASCII Value**s. So, every programmer should know **what they can do using ASCII values**. So, let's begin!

### Characters & ASCII Values

In C or C++ Programming Language, when we store a chartacter into a character type variable, that variable basically stores the ASCII Value of that character. That means if we write that `char ch = 'a'`, then `ch` basically stores the ASCII value of the character `'a'` and that is 65. Let's run the following code.

```c
	int main()
	{
		char ch = 'a';
		printf("The character is : %c.", ch);
		reutrn 0;
	}
```

We all know that the output will be :-

	The character is a.

The ASCII values of the characters from `a` to `z` are from 65 to 90. So the ASCII value of `b` is 66, `c` is 67, `d` is 68 and so on...

Let's guess the output of the following code :-

```c
	int main()
	{
		char ch1 = 'a';
		char ch2 = ch1 + 1;
		printf("The second character is %c.", ch2);
		return 0;
	}
```

What is the output? Is it `b` ? Yes, it is. Because, `ch1` stored the ASCII value of `a` that is 65. `ch2` stores `ch1 + 1` and that is 66. So, the output will be :-

	The second character is b.

As we are saying that `character variables store ASCII values`, can we print that value using these character variables? Yes, we can. See the following code :-

```c
	int main()
	{
		char ch = 'a';
		printf("%d", ch);
		return 0;
	}
```

The output is `65`, isn't it? 

So if we use `%d` instead of `%c`, `printf()` function will print the ASCII value that is stored in the character variable. So, if you want to know the ASCII value of, suppose, `k`, just write `char ch = 'k'` in the previous code instead od `char ch = 'a'`. 

You can see that we can print the character variable as an integer value. Can we do the reverse thing? That means I am asking you about the output of the following code:-

```c
	int main()
	{
		int x = 65;
		printf("%c", x);
		return 0;
	}
```

Before you run this code or read more of this article, please decide a `yes` or `no` for this qoute - "The output will be `a`."

Yes, the output will be `a`. Because we are printing x as a character, so `printf()` function will print the equivalent character whose ASCII value is 65. Som if I ask you to tell me the character whose ASCII value is 85, you might write the previous code using `x = 85`! So, this is how you can find the equivalent character of an ASCII value.




***

## Happy Coding!

***

`This page is maintained by Ariful Islam Shanto`
