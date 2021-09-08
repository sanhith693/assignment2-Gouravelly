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
<https://cp-algorithms.com/dynamic_programming/divide-and-conquer-dp.html>

