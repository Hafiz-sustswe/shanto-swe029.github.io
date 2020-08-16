<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/home.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingnotes.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/mathematicsnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/mathematicsnotes.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/programmingproblems"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingproblems.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/must-do-math-cp/home"> <img src = "https://shanto-swe029.github.io/newgitphoto/mustdomathforcp.png" height = "80"> </a>

***


# Average Of Digits Of A Number

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/averageofdigits/statement)

***

## Solution

#### Using C language

##### SOlution-01
- Using String

```c
    #include <stdio.h>
    #include <string.h>

    int main()
    {
        char num[25];
        scanf("%s", num);
        
        int q, r, sum = 0;
        int len = strlen(num);
        int i;
        for(i = 0; i < len; i++) {
            sum += num[i] - '0';
        }
        
        double avg = (double)sum / (double)(strlen(num));
        printf("%lf\n", avg);
        return 0;
    }
```

For a better view, [`Click Here`](https://pastebin.com/3A6bx5XC)

##### SOlution-02
- Using Stirng & User Defined Function

```c
    #include <stdio.h>
    #include <string.h>

    double Average(char n[])
    {
        int len = strlen(n);
        int i, s = 0;

        for(i = 0; i < len; i++) {
            s += n[i] - '0';
        }
        return (double)s / (double)(strlen(n));
    }

    int main()
    {
        char num[25];
        scanf("%s", num);
        double avg = Average(num);
        printf("%lf\n", avg);
        return 0;
    }
```

For a better view, [`Click Here`](https://pastebin.com/WGzDycxw)

***

`This page is managed by Ariful Islam Shanto`










