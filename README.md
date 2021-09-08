# assignment2-Gouravelly
# SanhithGouravelly
### Paris

I love Paris because of its **bustling** river banks,beauty and charm ofits **architecture**,delicious food, countless **opportunities** to explore art, culture, and history—the reasons.we love Paris are as diverse as the city itself.
****
# Directions to Kansas

1. The total driving distance from Maryville, MO to Kansas City, MO is 95 miles or 153 kilometers.
2. Your trip begins in Maryville, Missouri. It ends in Kansas City, Missouri.
    1. Travel by vechile from maryville.
    2. tracel towards to southern part of the state
* my phone
* Snacks<br>
[AboutMe](https://github.com/sanhith693/assignment2-Gouravelly/blob/main/AboutMe.md)
----
# My Favorite Food and Drinks
Here I'm going to tell you about my favorite food and drinks,most of them are authentic and delecious food with some refreshing drinks.

| **Food/Drink**               |**Location**|**Cost($)**|
|:----------------------------:|:----------:|:---------:|
|Hyd Biryani                   |Hyderabad   |10         |
|Chocolate bomb                |Vizag       |5          |
|Cheese Dosa                   |hyd         |5          |
|Chinese Cosmopolitan cocktail |vizag       |7          |
*****
# Pithy Quotes
> The greatest glory in living lies not in never falling, but in rising every time we fall. - *Nelson Mandela*<br>
> Life is what happens when you're busy making other plans. - *John Lennon*

***
# Code Fencing
## Dynamic Programming
> Dynamic Programming (DP) is an algorithmic technique for solving an optimization problem by breaking it down into simpler subproblems and utilizing the fact that the optimal solution to the overall problem depends upon the optimal solution to its subproblems. <br>
<https://www.educative.io/courses/grokking-dynamic-programming-patterns-for-coding-interviews/m2G1pAq0OO0>

* DP Optimizationn
    * Divide and Conquer DP<br>

  ```
  int m, n;
vector<long long> dp_before(n), dp_cur(n);

long long C(int i, int j);

// compute dp_cur[l], ... dp_cur[r] (inclusive)
void compute(int l, int r, int optl, int optr) {
    if (l > r)
        return;

    int mid = (l + r) >> 1;
    pair<long long, int> best = {LLONG_MAX, -1};

    for (int k = optl; k <= min(mid, optr); k++) {
        best = min(best, {(k ? dp_before[k - 1] : 0) + C(k, mid), k});
    }

    dp_cur[mid] = best.first;
    int opt = best.second;

    compute(l, mid - 1, optl, opt);
    compute(mid + 1, r, opt, optr);
}

int solve() {
    for (int i = 0; i < n; i++)
        dp_before[i] = C(0, i);

    for (int i = 1; i < m; i++) {
        compute(0, n - 1, 0, n - 1);
        dp_before = dp_cur;
    }

    return dp_before[n - 1];
} 
 ```
<br>
<https://cp-algorithms.com/dynamic_programming/divide-and-conquer-dp.html>
* Tasks 
    * Dynamic Programming on Broken Profile. Problem "Parquet"<br>
    ```mask=0,…2M−1```<br>
    <https://cp-algorithms.com/dynamic_programming/profile-dynamics.html>
    * Finding the largest zero submatrix<br>
    ```Elements of the matrix will be a[i][j], where i = 0...n - 1, j = 0... m - 1. For simplicity, we will consider all non-zero elements equal to 1.```<br>
    <https://cp-algorithms.com/dynamic_programming/zero_matrix.html>
    ## Linear Algebra
    > Linear algebra is the branch of mathematics concerning linear equations such as: {\displaystyle a_{1}x_{1}+\cdots +a_{n}x_{n}=b, } linear maps such as: {\displaystyle \mapsto a_{1}x_{1}+\cdots +a_{n}x_{n}, } and their representations in vector spaces and through matrices.<br>
    <https://en.wikipedia.org/wiki/Linear_algebra#:~:text=Linear%20algebra%20is%20the%20branch,almost%20all%20areas%20of%20mathematics.>

* Matrices
    * Gauss & System of Linear Equations<br>
    ```This problem also has a simple matrix representation:Ax=b```<br>
    <https://cp-algorithms.com/linear_algebra/linear-system-gauss.html>
    * Gauss & Determinant<br>
        ```This problem also has a simple matrix representation:Ax=b```<br>
    <https://cp-algorithms.com/linear_algebra/determinant-gauss.html><br>
    * Kraut & Determinant<br>
    ```Uij=Aij−∑k=1i−1Lik⋅Ukj```<br>
    <https://cp-algorithms.com/linear_algebra/determinant-kraut.html><br>
    * Rank of a matrix<br>
    ```This problem also has a simple matrix representation:Ax=b```<br> 
    <https://cp-algorithms.com/linear_algebra/linear-system-gauss.html><br>
# Numerical Methods
> In numerical analysis, a numerical method is a mathematical tool designed to solve numerical problems. The implementation of a numerical method with an appropriate convergence check in a programming language is called a numerical algorithm.<br>
<https://en.wikipedia.org/wiki/Numerical_method>
* Search 
    * Ternary Search<br>
    ```consider any 2 points m1, and m2 in this interval: l<m1<m2<r. We evaluate the function at m1 and m2, i.e. find the values of f(m1) and f(m2). Now, we get one of three options:```<br>
    <https://cp-algorithms.com/num_methods/ternary_search.html><br>
    * Newton's method for finding roots<br>
    ```xi+1=xi−f(xi)f′(xi)```<br>
    <https://cp-algorithms.com/num_methods/roots_newton.html><br>
* Integration
    * Integration by Simpson's formula<br>
    ```∫baf(x)dx≈(f(x0)+4f(x1)+2f(x2)+4f(x3)+2f(x4)+…+4f(x2N−1)+f(x2N))h3```<br>
    <https://cp-algorithms.com/num_methods/simpson-integration.html>