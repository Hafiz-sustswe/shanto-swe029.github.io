[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# Sum Of Digits Of A Number

***

## Solution

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/sumofdigitsofanumber/statement)

#### Using C Language

##### Solution-01
- Using Modular Arithmetic

***

```c
#include <stdio.h>
int main()
{
    long long x; // as x <= 10^19
    scanf("%lld", &x);

    long long q = x, r, sum = 0;

    while(q > 0) {
        r = q % 10;
        sum += r;
        q /= 10;
    }

    printf("%lld\n", sum);


    return 0;
}
```

For a better view, [`Click here`](https://pastebin.com/QLVVeCp3)

##### Solution-02
- Using Modular Arithmetic & User Defined Function

***

```c
#include <stdio.h>

long long SumOfDigits(long long n)
{
    long long r, q = n, s = 0;
    while(q > 0) {
        r = q % 10;
        s += r;
        q /= 10;
    }
    return s;
}

int main()
{
    long long x; // as x <= 10^19
    scanf("%lld", &x);

    long long sum;

    sum = SumOfDigits(x);

    printf("%lld\n", sum);


    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/hmwmNvPg)

##### Solution-03
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

    printf("%d\n", sum);


    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/AuEfwWNm)

##### Solution-04

- Using String & User Defined Function

***

```c
#include <stdio.h>
#include <string.h>

int SumOfDigits(char n[])
{
    int len = strlen(n);
    int i, s = 0;

    for(i = 0; i < len; i++) {
        s += n[i] - '0';
    }
    return s;
}

int main()
{
    char num[25];
    scanf("%s", num);

    int sum;

    sum = SumOfDigits(num);

    printf("%d\n", sum);


    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/e83iawaH)

***

`This page is maintained by Ariful Islam Shanto`
