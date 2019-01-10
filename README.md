# PAT-
- string::to_string() 
>将括号（）内的内容转换为字符串string类型
- algorithm中的max_element，min_element
>这两个函数返回的是位置指针，*max_element可以获得最大值
```c++
int len[10] = {1,2,3,4,5,6,7,8,8,9};
int max;
max = (*max_element(len, len + 100));//这时候，max值为9
```
- reverse()很好用

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

