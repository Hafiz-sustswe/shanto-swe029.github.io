[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes) || [`Must Do Math For Competitive Programmers`](https://shanto-swe029.github.io/must-do-math-cp/home)

***

# Internship Viva

***

## Solution

[`See Statement`](https://shanto-swe029.github.io/programmingproblem/sort-the-struct/statement)



### Using C language

```c

#include <stdio.h>

typedef struct {
    char name[20];
    long long reg_no;
    int nops;
    double cgpa;
} student;

int main()
{
    int n;
    scanf("%d", &n);
    student info[n];
    int i;
    for(i = 0; i < n; i++) {
        scanf("%s", &info[i].name);
        scanf("%lld", &info[i].reg_no);
        scanf("%d", &info[i].nops);
        scanf("%lf", &info[i].cgpa);
    }

    for(i = 0; i < n - 1; i++) {
        for(int j = i + 1; j < n; j++) {
            if(info[i].nops < info[j].nops) {
                student temp = info[j];
                for(int k = j; k > i; k--) {
                    info[k] = info[k - 1];
                }
                info[i] = temp;
            }
        }
    }

    int l = 0, r; /// for indexing

    for(i = 0; i < n; i++) {
        if(i == n - 1) {
            r = i;
            for(int j = l; j < r; j++) {
                for(int k = j + 1; k < r; k++) {
                    if(info[j].cgpa < info[k].cgpa) {
                        student temp = info[k];
                        for(int m = k; m > j; m--) {
                            info[m] = info[m-1];
                        }
                        info[j] = temp;
                    }
                }
            }
            l = r;
        }

        else if(info[l].nops != info[i].nops) {
            r = i;
            for(int j = l; j < r; j++) {
                for(int k = j + 1; k < r; k++) {
                    if(info[j].cgpa < info[k].cgpa) {
                        student temp = info[k];
                        for(int m = k; m > j; m--) {
                            info[m] = info[m-1];
                        }
                        info[j] = temp;
                    }
                }
            }
            l = r;
        }
    }

    printf("\nAfter sorting the list is:\n");
    for(i = 0; i < n; i++) {
        printf("%2d. ", i+1);
        printf("%s ", info[i].name);
        printf("%lld ", info[i].reg_no);
        printf("%d ", info[i].nops);
        printf("%0.2lf\n", info[i].cgpa);
    }


    return 0;
}

```








***

`This page is managed by Ariful Islam Shanto`
