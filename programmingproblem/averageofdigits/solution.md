**Go To**: [`Home Page'](https://shanto-swe029.github.io/)||[`Some Programming Problem`]

# Average Of Digits Of A Number

[`See Statement`]

***

## Solution

#### Using C language

##### SOlution-01

- Using Modular Arithmetic

***

```c
    #include <stdio.h>
    int main()
    {
        long long x; // as x <= 10^19
        scanf("%lld", &x);

        long long q = x, r, sum = 0, tot = 0;

        while(q > 0) {
            r = q % 10;
            sum += r;
            q /= 10;
            tot++;
        }

        double avg = (double) sum / (double)tot;

        printf("%lf\n", avg);


        return 0;
    }
```

For a better view, [`Click Here`](https://pastebin.com/R9S5GzRM)

##### SOlution-02
- Using Modular Arithmetic & User Defined Function

```c
    #include <stdio.h>

    double Average(long long n)
    {
        long long r, q = n, s = 0, tot = 0;
        while(q > 0) {
            r = q % 10;
            s += r;
            q /= 10;
            tot++;
        }
    return (double)s / (double)tot;
    }

    int main()
    {
        long long x; // as x <= 10^19
        scanf("%lld", &x);
        double avg = Average(x);
        printf("%lf\n", avg);
        return 0;
    }
```

For a better view, [`Click Here`](https://pastebin.com/FiYWfgTm)

##### SOlution-03
` Using String

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

##### SOlution-04
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










