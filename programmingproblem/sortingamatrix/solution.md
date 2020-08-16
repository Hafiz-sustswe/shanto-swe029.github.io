<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/home.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingnotes.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/mathematicsnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/mathematicsnotes.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/programmingproblems"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingproblems.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/must-do-math-cp/home"> <img src = "https://shanto-swe029.github.io/newgitphoto/mustdomathforcp.png" height = "80"> </a>

***


# Sorting A Matrix

***

## Solution

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/sortingamatrix/statement)

#### Using C Language

##### Solution - 01

- Without Using Function

***

```c
#include <stdio.h>
int main()
{
    int m, n;
    scanf("%d %d", &n, &m);

    int ara[n][m];
    int i, j, k;
    for(i = 0; i < n; i++) {
        for(j = 0; j < m; j++) {
            scanf("%d", &ara[i][j]);
        }
    }
    for(i = 0; i < n; i++) {
        for(j = 0; j < m - 1; j++) {
            for(k = j + 1; k < m; k++) {
                if(ara[i][j] > ara[i][k]) {
                    //swap
                    int temp = ara[i][j];
                    ara[i][j] = ara[i][k];
                    ara[i][k] = temp;
                }
            }
        }
    }
    for(i = 0; i < n; i++) {
        for(j = 0; j < m; j++) {
            printf("%d", ara[i][j]);
            // we won't print extra spaces
            if(j != m - 1) {
                printf(" ");
            }
        }
        printf("\n");
    }


    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/s239Ftj8)

##### Solution - 02

- Using Function

***

```c
#include <stdio.h>

void BubbleSort(int *ara_, int len)
{
    int i, j;
    for(i = 0; i < len - 1; i++) {
        for(j = i + 1; j < len; j++) {
            if(ara_[i] > ara_[j]) {
                //swap
                int temp = ara_[i];
                ara_[i] = ara_[j];
                ara_[j] = temp;
            }
        }
    }
}

int main()
{
    int m, n;
    scanf("%d %d", &n, &m);

    int ara[n][m];
    int i, j, k;
    for(i = 0; i < n; i++) {
        for(j = 0; j < m; j++) {
            scanf("%d", &ara[i][j]);
        }
    }
    int new_ara[m];
    for(i = 0; i < n; i++) {
        for(j = 0; j < m; j++) {
            new_ara[j] = ara[i][j];
        }

        BubbleSort(new_ara, m);

        for(j = 0; j < m; j++) {
            printf("%d", new_ara[j]);
            // we won't print extra spaces
            if(j != m - 1) {
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/Wj16ZcbD)

***

`This page is maintained by Ariful Islam Shanto`
