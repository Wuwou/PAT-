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
- 最大公约数gcb（）
```c++
int gcd(int a, int b)
{
    return !b ? a : gcd(b, a  % b);
}
```
- sqrt(float x)注意类型不要弄错
```c++
In C++11 you can write:
for (auto& it : s) {
    cout << it << endl;
}
instead of

for (auto it = s.begin(); it != s.end(); it++) {
    cout << *it << endl;
}
It has the same meaning.
```
- 用printf输出‘%’的时候用两个百分号%%，这样才可以输出%这个符号
- 有什么方法可以上实现用printf输出string类型的字符串呢？——使用c_str()函数可以
> 返回指向以null结尾的字符数组的指针，该数组的数据等效于存储在字符串中的数据
- map会实现自动排序
- std::isalnum用来判断字符是否是alphanumeric character，即0~9，A~Z， a~z
>头文件 <cctype>
    
- 结构体初始化时进行比较
    
```c++
    struct fruit {
	string name;
	int price;
}f1, f2, f3;
struct cmp {
	bool operator()  (fruit f1, fruit f2) {
		return f1.price > f2.price;
	}
};
```
    
或者是
```c++
struct fruit {
	string name;
	int price;
	friend bool operator < (fruit f1, fruit f2) {
		return f1.price < f2.price;
	}
};

```
-- > 用什么来拯救我濒临死亡的c++
- 有两种申请分配内存的方法：malloc和new（两者是运算符，不是函数）
在c中使用malloc运算符(free去释放)，即typename* p = (typename*) malloc (sizeof(typename));
在c++中使用new运算符(delete去释放)会方便很多，即typename* p = new typename;
eg:
int* p = (int*)malloc(sizeof(int));
int* p = new int;
- 在吸收换行符时，一般都是用getchar()函数来吸收，但是还有一种可以吸收,即cin.ignore();
    
    
    
    
    
    
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

