# Code With Explanation

***

```cpp
////BISMILLAGIR-RAHMANIR-RAHIM

///                 Multiply Two Number Using String

/*
    In this code, we'll see how we can multiply two string of the same size.
        This is necessary because we cannot multiply and get a product if
        the product becomes larger than 10^19 ( = 10000000000000000000 ).
        Using this method we can get a product whose value is up to 10^(4294967295).
        So this is the number you can barely imagine as it has 4294967295 digits!
    N.B. If we multiply two string of size 3,
         our product string must be of length 6.
         So, the the size is x,
         our product string must be of length 2*x.
         But we don't need more that 2*x indexes to store the product in a string.
    Hint:
            Suppose, we wanna multiply 345 with 129.
            so, char s1[] = "345"    ,     s2[] = "129";
            and, char result[6] = "000000";
            we are initializing the result string with 6 zeros. "This part is important."
            Let's see how we can multiply 345 by 129.
                *       345 x 129 = (345 x 9) + (345 x 20) + (345 x 100)
                # we will use this method to multiply two string.
                    >> firstly, we'll multiply 345 by 9, store it in a temporary string and
                       we'll add the temporary string with our result string.
                    >> then we'll multiply 345 by 2, store it in a temporary string and
                       we'll have to ad an extra 0 after the last element of the temporary
                       string and then we'll add it to our result string.
                    >> then we multiply 345 by 1, store it in a temporary string, add two
                       0s after the last elements and then we add it with our result string.
            Now you have enough instructions to write the code by yourself. First, I suggest that
            you try it by yourself. If you fail to code, then see my code.
        Please, move to the main function first  >> Line - 127.
*/

#include <bits/stdc++.h>
using namespace std;

void multiply(string s, char ch, string &temporary)
{
    temporary.clear();              // this line is necessary
    temporary.assign(2 * s.size(), '0');

    /*
        why we are reusing the assign() function here to set the values to 0
        will be discussed in the main function.
    */

    int i, j;
    int n = s.size();
    int m = temporary.size();
    int carry = 0, product;
    for(i = n - 1, j = m - 1; i >= 0; i--, j--) {
        product = (s[i] - '0') * (ch - '0') + carry;
        carry = product / 10;
        temporary[j] = product % 10 + '0';
        /*
            please read the explanation below this function
            if you do not understand previous three lines.
                Line number - 77
        */
    }
    temporary[j] = carry + '0'; /* This line is necessary because there might be a carry
                                remaining after the last step.
                            */
}

/*
    Explanation:
            Let's first see an example. If you write this code in
            the main function and run, what will be the output?
                    int x;
                    char ch = 'a';
                    x = ch;
                    cout << "x = " << x << endl;
            The output will be the ASCII value of 'a' that is 65.
            now, what happens in this code below?
                    char x = '5';
                    char y = '7';
                    int p = x * y;
                    cout << "product is " << p << endl;
            ASCII value of '5' is 53 and ASCII value of '7' is 53.
            So your code will give the product 2915 and not 35.
            So, to solve this problem we use the method below:
                    char x = '5';
                    char y = '7';
                    int p = (x - '0') * (y - '0');
                    cout << "product is " << p << endl;
            Now, if you run the code it will give you 35 as the product. WHY?
            ASCII value of '0' = 48;
            So, '5' - '0' = 53 - 48 = 5     and
                '7' - '0' = 55 - 48 = 7.
                Therefore,
                        ('5' - '0') * ('7' - '0') = 35;
            So, if we want to use character '5' as integer 5,
            we have to subtract '0' from '5' or we can also
            subtract the ASCII value of '0' instead like { '5' - 48 }
            But I guess subtracting '0' will give you more flexibility
            when you write your code.
            Now I guess you understand what happened in the function and
            why we committed the subtraction.
            But you will see that when we stored product into the temporary
            string, we again added '0' with it. This is because, we want to
            store the ASCII value of our product into the string. Let's say
            that the product is 7. If we do not add '0' with it and store it
            in the string, then the string will store the character whose ASCII
            value is 7 and obviously will not store '7'.
*/


int main()
{
    /* we are not using character data_type, but string data_type.
       Because, string data_type allows us to add extra elements
       after the last position.
       But we can also use character data_type and handle the case
       of adding 0s in another way. I'll show it in another code.
    */

    string str1;
    string str2;

    /*
        you can take the two string as input or you can manually assign them.
        Here, I'll manually assign them. In another code, I'll take them as input.
    */

    str1 = "8496";
    str2 = "6204";

    /*
            just remove the previous two lines and
            use this line below to take input.
                cin >> str1 >> str2;
    */
    int n = str1.size(); // you can also write " n = str2.size() "

    /*
        Now we will declare our result string and set all of the elements to zero.
        Besides we will also declare a temporary array of the same size as our result array.
    */

    string result;
    string temp;
    int i;

    for(i = 0; i < 2 * n; i++) {
        result.push_back('0');      // please note that 0 is stored as a character
    }

    /*
        if you do not like the idea of using loop,
        you can also use std::assign() function to
        do the same task for you.
        But I suggest that before you use std::assign(),
        you learn about it.
        we are assigning eight 0s to our temp string using std::assign().
    */

    temp.assign(2 * n, '0'); // this is the format >> var_name.assign(number of index, value)

    /*
        we will use std::assign() function again and again in our code.
        Now let's go to the main action.
    */

    /*
        we will use several function to keep our main function understandable.
        As you see we have to multiply our first string with all of the elements
        of our second string one by one and build our temp string, we'll create
        a function which will do the same work for us.
        Let's name it       >>      multiply();
    */

    int j, step = 0;

    for(i = n - 1; i >= 0; i--) {
        multiply( str1, str2[i], temp );
        /*
            now we write the function before our main function.
            move to line number 41.
        */
        /*
            now our temp string is ready but there is another work to do.
            we have to include the 0s after the temp string.
                in the 1st sept we have to add 0 0s
                in the 2nd step we have to add 1 0s
                in the 3rd step we have to add 2 0s
            But we can say those previous line like this too-
                in the 0th sept we have to add 0 0s
                in the 1st step we have to add 1 0s
                in the 2nd step we have to add 2 0s
            This will help us think easily. We use the variable "step"
            to tract our step number. We will at  assign 0 in it and
            increase its value by 1after each step.
        */
        for(j = 0; j < step; j++) {
            temp.push_back('0'); // we have to use push back here
        }
        step++;

        /*
            Now we have to add this temp to our result string.
            We can do it by function or we can do it here.
            To use function, you have to use pointer as we used
            in our multiply() function to change our temp string.
        */

        int carry = 0, x, k;
        for(j = result.size() - 1, k = temp.size() - 1; j >= 0; j--, k--) {
            x = (result[j] - '0') + (temp[k] - '0') + carry;
            carry = x / 10;
            result[j] = x % 10 + '0';
            //just same as multiplying
        }
        // we are done. Let's get out from this loop and print the result string.
    }

    cout << str1 << " x " << str2 << " = " << result << endl;

    /*
        You can also take str1 and str2 as input.
        just use cin >> str1 >> str2.
        Remember that, here the two number must have equal number of digits.
        Otherwise, you'll not get expected output.
        if you want to multiply 12345 with 123,
        you can take input as 12345 and 00123 or assign them like this.
        Otherwise,
            if you take input as or assign value as 12345 and 123,
                you have manually change 123 to 00123.
                you can use insert() function to do this.
        Now this would be much better if you try to write a code which
        takes 12345 and 123 as input and multiply them using strings.
    */

    return 0;
}

```
