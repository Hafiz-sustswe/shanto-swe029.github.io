[`return to Home Page`](https://shanto-swe029.github.io/) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

# Smart Declaration of an Array

***

At the beginning, let's see two short code before we begin our dicussion.

```c
    #include <stdio.h>
    int main()
    {
        int ara[500000];
        int n;
        scanf("%d", &n);
        for(int i = 0; i < n; i++) {
            scanf("%d", &ara[i]);
        }
        for(int i = 0; i < n; i++) {
            printf("%d ", ara[i]);
        }
    }
```

```c
    #include <stdio.h>
    int main()
    {
        int ara[n];
        int n;
        scanf("%d", &n);
        for(int i = 0; i < n; i++) {
            scanf("%d", &ara[i]);
        }
        for(int i = 0; i < n; i++) {
            printf("%d ", ara[i]);
        }
    }
```

Now, What is the difference between these two codes? Can you guess? If you cannot guess, then see those codes again to understand the difference. 
If you have read these two codes carefully, then move to the next section.

***

**In the first code**, we declared an array of size 500000. Then we scanned a value of n and took input of n integers as the elements of the array. 
Now, if n = 5, we do not need an array of size 500000! Again if n > 500000, this array will not be able to store all elements we need. Moreover, we will get a runtime error!
<br>
So, to become a smart programmer, we declare the array as of the second example and BINGO! We feel like we are smarter than ever! 
But in this declaration, we will get a compilation error! Why?
<br>
Let's have a look at the code again. At first, we declared `ara[n]` and then we declared n. As C compilers run line by line, in the first line, it will see that we have used a variable `n`, but we have not declared 'n' yet! 
So, we'll get a compilation error! Because, in that particular line, the compiler does not know who the hell this `n` is!
<br>
So to fix this problem we write the following code.

```c
    #include <stdio.h>
    int main()
    {
        int n;
        int ara[n];
        scanf("%d", &n);
        for(int i = 0; i < n; i++) {
            scanf("%d", &ara[i]);
        }
        for(int i = 0; i < n; i++) {
            printf("%d ", ara[i]);
        }
    }
```

Ah! Relief! Is it?
<br>
No, it's not. Why? What did we do wrong? Let's have a closer look at the code again. If you can understand the problrm by yourself, 
that's very good for you. But if you cannot understand, do not panic! Because, panic will seize the day! Move to the next portion.
<br>
In this code, we declared `n` - that is right. But as in the next line, we are declaring `int ara[n]`, will you please tell 
me what is exactly the value of `n`?
<br>

I guess - now you know the answer! Yes, you are right! We declared `n`, but we did not assign any value to `n` and we had declared 
an array of size `n`! How pathetic! The array did really mind! So before we declare an array of size `n`, the value of `n` must 
be assigned or scanned!
<br>
So, the **Smartest Declaration** is as in the following code-

```c
    #include <stdio.h>
    int main()
    {
        int n;
        scanf("%d", &n);
        int ara[n];
        for(int i = 0; i < n; i++) {
            scanf("%d", &ara[i]);
        }
        for(int i = 0; i < n; i++) {
            printf("%d ", ara[i]);
        }
    }
```

And that is - **we declare the array after we have the size of the array in our hand!**
<br>
I guess - form now we will be the smartest ones to declare an array!

***

## Happy Coding!

***

`This page is managed by Ariful Islam Shanto`

