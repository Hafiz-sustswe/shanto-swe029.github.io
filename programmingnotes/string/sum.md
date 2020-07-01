[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# Sum Of Two Large Numbers Using String

- If we want to add two 100 digit numbers, it is not possible using `long long` datatype too. As we discussed earlier, string can store larger numbers. So we will manipulate the strings to get our desired result. Let's get started!

<br>

### What do we do when we add two numbers in our copy? Do you remember that process?

- Here we will use the algorithm that we use to add two numbers.
- Suppose, we want to add 83 and 79. What do we do?
	
		We write them like this:-
				83
			   +79
			------
		
		Then we calculate 3+9 = 12.
		We place 2 at the units place and count 1 as a carry.
		        83
		       +79
			------
		         2
		Then we calculate 8+7+1 = 16.
		We place 6 at the tens place and count 1 as a carry.
		        83
		       +79
			------
		        62
		As there are no digits left, we place 1 at hundreds place.
				83
			   +79
			------
		       162
		
- This is algorithm we are going to use! But before that let's work with another example.
- We want to add 9876 and 55. What do we do?

		We write them like this:-
		    9876
			+ 55
		--------
		
		calculate 6 + 5 = 11.
		Place 1 = 11 % 10 at units place, count 1 = 11 / 10 as a carry.
		    9876
			+ 55
		--------
		       1
		Calculate 7 + 5 + 1 = 13
		Place 3 = 13 % 10 at tens place, count 1 = 13 / 10 as a carry
		    9876
			+ 55
		--------
		      31
		Now, we calculate 8 + 1 = 8 + 0 + 1 = 9
		Place 9 = 9 % 10 at hundreds place, count 0 = 9 / 10 as a carry
		    9876
			+ 55
		--------
		     931
		Calculate 9 + 0 + 0 = 9.
		place 9 = 9 % 10 at hundreds place, count 0 = 9 / 10 as a carry
		    9876
			+ 55
		--------
		    9931
		As there are no digits left, we place 0 at thousands place
		    9876
			+ 55
		--------
		   09931

- So, **if the two numbers are not of equal length, we have to add leading zeros to the smaller number**. This part is very important.
- At fist we will write a code that which will work for two numbers if their length are equal or we will input leading zeros to make them of equal length.
- let `char num1[] = "12", num2[] = "34"`. We do the following operation. `int s = num1[1] + num2[1];`. Now what is the value of s? is it 6? Let's run a code and see what happens[you need to do this by your own to make your idea more clear]. The value is not 6, is it? Actually, here in num1 & num2, 1,2,3,4 etc are characters. And when you add two characters, your code actually adds their ASCII values. So, to solve this problem we can subtract the ASCII value of '0'  from each character. And if we make the following operation - `int s = (num1[1] - '0') + (num2[1] - '0')`, the value of s will be as we ecpect. We will use this idea too. This is one of the most important idea.

- But remember, we have to start from the back of each string. And The length of out summation storing string must be 1 greater than the length of the other two strings. Lets's get started!

```c
	#include <stdio.h>
    #include <string.h>
    int main()
    {
        char num1[] = "98765";
        char num2[] = "87654"; // Instead you can scan them
        int len = strlen(num1); // Instead you can write len = strlen(num2)
        char sum[len+2];    // We did not take len + 1, but len + 2. Reason will bw explained later.
        int i, j, carry, s;
        
        //in the first addition, carry = 0. So
        carry = 0;
        for(i = len - 1, j = len; i >= 0; i--, j--) {
            s = (num1[i] - '0') + (num2[i] - '0') + carry;  // Converting to numbers
            carry = s / 10;
            sum[j] = (s % 10) + '0';    // Converting into a character
            //why did we use j as indexe for sum[] and why not i? I'll leave it to you.
        }
        //After this loop ends, one carry will be pending. We have to store it into the sum[] string
        sum[j] = carry + '0';   // Converting into a character
        sum[len + 1] = '\0';    /* If we do not do this, then we will get garbage values 
                                at the end of our output. And to set this NULL character,
                                we took one more place for this string*/
        printf("%s + %s = %s\n", num1, num2, sum);
        return 0;
    }
```

So, now we can calculate the sum of two equal length large numbers!

***

In this section, I'll show you how we can add two numbers of different length. Do you have any idea?
[coming soon...]

***

`This page is managed by Ariful Islam Shanto`












