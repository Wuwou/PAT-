# PAT-
- string::to_string() 
>将括号（）内的内容转换为字符串string类型
- algorithm中的max_element，min_element
>这两个函数返回的是位置指针，*max_element可以获得最大值
```c++
int len[10] = {1,2,3,4,5,6,7,8,8,9};
int max;
max = (*max_element(len, len + 10));//这时候，max值为9
```
- reverse()，_strrev()函数
> reverse()实现对字符串的反转，对字符数组无效。_strrev()实现对字符数组的反转，对字符串无效
```c++
string s = "asdf";    
reverse(s.begin(), s.end());  //s = "fdsa"
int a[5] = { 1,2,3,4,5 };
reverse(a[0], a[5]);          //犯错。。。怎样用下标？疑问：似乎只能对string类型才可以用reverse
char s[]="hello";
_strrev(s);                    //s[] = "olleh"
```

- 数组初始化的误区及fill()和fill_n()的用法
```c++
int a[10] = {9}; //a[10] = {9,0,0,0,0,0,0,0,0,0,0};
int main()
{
    int a[20];
    std::memset(a, 0, sizeof a);
    for (int ai : a) std::cout << ai;
}
此时可以用fill(first,last,value) or fill_n(first, size, value)
eg：
vector<int>　myvector (8,10);     // myvector: 10 10 10 10 10 10 10 10
fill_n (myvector.begin(),4,20);   // myvector: 20 20 20 20 10 10 10 10
fill_n (myvector.begin()+3,3,33); // myvector: 20 20 20 33 33 33 10 10
fill(myvector, myvector+8, 10);   // myvector: 10 10 10 10 10 10 10 10
```
- strump属于头文件string.h
- 在比较字符数组的时候用strump，不能直接用等于来比较
- partiton is too hard for me T.T
- 关于字符串与数字之间的转换，可以用to_string（）和stoi（）函数，这样可以不用写出复杂的转换函数
- double类型，scanf用lf%，printf用f%



















# 一级标题
## 二级标题
### 三级标题

> 这是第一级引用。
>
> > 这是第二级引用。
>
> 现在回到第一级引用。

- Red

*  Coding.net有以下主要功能:
    > 代码托管平台
    > 在线运行环境    
    > 代码质量监控    
    > 项目管理平台
    
- [ ] 不勾选
- [x] 勾选
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
**Coding，让开发更简单**
__Coding，让开发更简单__

