<a href = "https://shanto-swe029.github.io/"> <img src = "https://shanto-swe029.github.io/newgitphoto/home.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingnotes.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/mathematicsnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/mathematicsnotes.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/programmingproblems"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingproblems.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/must-do-math-cp/home"> <img src = "https://shanto-swe029.github.io/newgitphoto/mustdomathforcp.png" height = "80"> </a>

***


# Matrix Multiplication

***

## Solution

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/matrixmultiplication/statement)

#### Using C Language

```c
#include <stdio.h>

int main()
{
    int n1, m1, n2, m2;
    int i, j;

    scanf("%d %d", &n1, &m1);

    int mat1[n1][m1];

    for(i = 0; i < n1; i++) {
        for(j = 0; j < m1; j++) {
            scanf("%d", &mat1[i][j]);
        }
    }

    scanf("%d %d", &n2, &m2);

    int mat2[n2][m2];

    for(i = 0; i < n2; i++) {
        for(j = 0; j < m2; j++) {
            scanf("%d", &mat2[i][j]);
        }
    }

    if(m1 != n2) {
        printf("Not Possible\n");
        return 0;
    }

    int n = n1, m = m2;
    printf("%d %d\n", n, m);

    int result[n][m];
    int x, k;

    for(i = 0; i < n1; i++) {
        for(j = 0; j < m2; j++) {
            x = 0;
            for(k = 0; k < m1; k++) {
                x += mat1[i][k] * mat2[k][j];
            }
            printf("%d ", x);
        }
        printf("\n");
    }


    return 0;
}
```

For a better view, [`Click Here`](https://pastebin.com/CnrbHkyX)

***

`This page is maintained by Ariful Islam Shanto`
