# Practice
位1的个数
## 问题分析：
#### 
编写一个函数，输入是一个无符号整数，返回的是它所有 位1 的个数（也被称为汉明重量）。
例如，32位整数 '11' 的二进制表示为 00000000000000000000000000001011，所以函数返回3。
## 编程实现：
```C++
class Solution {
public:
    int hammingWeight(uint32_t n) {
        int sum=0;
        while(n)
        {
             sum += n & 0x00000001;
        n >>= 1;
        }
        return sum;
    }
};
```
## 总结体会：
提取原始数最低位，进行求和，通过移位，将32位整数都提取后求和，若最低位为1，sum加1。