## Syntax
$$[\text{capture}](\text{params}) \rarr \text{ return\_type } \{ \text{body} \}$$
The *capture* can either be $=$ (by value) or $&$ (by reference).
```cpp
std::vector<int> v = { 1, 2, 3};
int sum = 0;
std::for_each(v.begin(), v.end(), [&sum](int x) { sum += x; })
```
- ### Anonymous
  Not able to be referenced inside of itself!
  
  To do so, you need *y combinators*.