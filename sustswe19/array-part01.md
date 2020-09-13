
<a href = "https://shanto-swe029.github.io/"> <img src = "https://shanto-swe029.github.io/newgitphoto/home.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/programmingnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingnotes.png" height = "80" align = "left"> </a>
<a href = "https://shanto-swe029.github.io/mathematicsnotes"> <img src = "https://shanto-swe029.github.io/newgitphoto/mathematicsnotes.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/programmingproblems"> <img src = "https://shanto-swe029.github.io/newgitphoto/programmingproblems.png" height = "80"> </a>
<a href = "https://shanto-swe029.github.io/must-do-math-cp/home"> <img src = "https://shanto-swe029.github.io/newgitphoto/mustdomathforcp.png" height = "80"> </a>

***


# Array

### Distinct Element Count

```c

//              ******    Array Manipulation     ******
 
 
#include <stdio.h>
 
int main()
{
    int nibo[]= {1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 1, 0, 1, 1};
    int ara[] = {1, 2, 0, 3, 4, 1, 0, 2, 3, 4, 5, 3, 7, 15};
 
    //how many distinct elements are there in the array?
    //store them in another array.
 
    /*
        BIJON -> sorting, then choose one element from equal elements
 
        HORI  -> If there are multiple elements of same value,
                 we count the last one only
 
        Ibrahim -> Left Shift when find equal elements.
 
        SHATTIK -> 1. Choose an index (element)
                   2. Check all previous indexes to determine if the
                      element of this index is taken already.
                   3. If not taken already, count++; else nothing.
 
        MEEM  -> 1. find max
                 2. Replace repeated elements with a specific value
                 3. then count the number of specific element in the array
    */
 
 
    return 0;
}

```

### Determining Frequency of Each Element

```c

//              ******    Array Manipulation     ******
 
 
#include <stdio.h>
 
int main()
{
    //int count[]={1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0};
 
    int chngIdx[14+1]
              = {0, 2, 4, 7, 9, 10, 11, 14, -1, -1, -1, -1, -1};
    int ara[14] = {1, 1, 2, 2, 3, 3, 3, 4, 4, 5, 7, 15, 15, 15};
 
    int idx[6+1] = {0, 1, 2, 3, 4, 5, 6};
    int new[6]   = {1, 2, 3, 4, 5, 6};
 
    /*  output ::
        1  -> 2
        2  -> 2
        3  -> 3
        4  -> 2
        5  -> 1
        7  -> 1
        15 -> 1
    */
 
    int ara[] = {1, 2, 0, 3, 4, 1, 0, 2, 3, 4, 5, 3, 7, 15};
 
    //Frequency of each element.
 
    /*
            BIJON -> sort and count.
 
            MOJU  -> use count array and increase corresponding index by 1.
 
            MEEM  -> Cumulative Summation
    */
 
 
    return 0;
}

```


***

**`This page is mainted by Ariful Islam Shanto`**
