---
title: 写作文章示例汇总
tags:
  - Examples
createTime: 2025/07/20 14:30:31
permalink: /article/6qzu78fp/
---

## 一、基础格式

### 1.标题格式
::: code-tabs
@tab 普通标题

```markdown
## 标题H2

### 标题H3

#### 标题H4

##### 标题H5

###### 标题H6
```

@tab Badge标题

```markdown
## 标题2 Badge <Badge type="tip" text="Badge" />

### 标题3 Badge <Badge type="warning" text="Badge" />

#### 标题4 Badge <Badge type="danger" text="Badge" />
```

:::

### 2.正文格式

::: collapse
- 链接
  ```markdown
  相对链接：See my [About](/about/) page for details.
  定义链接名称:
  I get 10 times more traffic from [Google][1] than from[Yahoo][2] or [MSN][3].
  [1]: http://google.com/ "Google"
  [2]: http://search.yahoo.com/ "Yahoo Search"
  [3]: http://search.msn.com/ "MSN Search"
  行内：I get 10 times more traffic from [Google](http://google.com/ "Google") 
  than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") 
  or [MSN](http://search.msn.com/ "MSN Search").
  ```
  示例:
  相对链接：See my [About](/about/) page for details.
  
  定义链接名称:

  I get 10 times more traffic from [Google][1] than from[Yahoo][2] or [MSN][3].

  [1]: http://google.com/ "Google"
  [2]: http://search.yahoo.com/ "Yahoo Search"
  [3]: http://search.msn.com/ "MSN Search"

  行内：I get 10 times more traffic from [Google](http://google.com/ "Google") than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or [MSN](http://search.msn.com/ "MSN Search").
- 文字
  ```markdown
  强调: **double asterisks** 
  需使用星号： \*this text is surrounded by literal asterisks\*
  斜体： _斜体文字_
  ~~删除文字~~
  ==标记==
  ::: center
  内容居中
  
  ::: right
  内容右对齐
  

  ```
  示例:

  强调: **double asterisks**  
  需使用星号： \*this text is surrounded by literal asterisks\*  
  斜体： _斜体文字_  
  ~~删除文字~~  
  ==标记==  
  ::: center  
  内容居中  
  
  ::: right  
  内容右对齐  
   
- 行内代码
  ```markdown
  Use the `printf()` function.
  ```
  示例：  
  Use the `printf()` function.  
- 图片  
  ```markdown  
  [链接](/)

  [外部链接](https://github.com/pengzhanbo)

  ![plume](/plume.svg)  
  自动链接：<http://example.com/>
  ```
  [链接](/)  

  [外部链接](https://github.com/pengzhanbo)  

  ![plume](/plume.svg)   
  <http://example.com/> 
- 转义字符
  ```markdown 
  Markdown 支持在下面这些符号前面加上反斜线来帮助插入普通的符号:  
  \\ 反斜线  
  \` 反引号  
  \* 星号  
  \_ 底线  
  \{} 大括号  
  \[] 方括号  
  \() 括号  
  \# 井字号  
  \+ 加号  
  \- 减号  
  \. 英文句点  
  \! 惊叹号 
  ```  
  Markdown 支持在下面这些符号前面加上反斜线来帮助插入普通的符号:  
  
  \\ 反斜线  
  \` 反引号  
  \* 星号  
  \_ 底线  
  \{} 大括号  
  \[] 方括号  
  \() 括号  
  \# 井字号  
  \+ 加号  
  \- 减号  
  \. 英文句点  
  \! 惊叹号 


  
### 3.列表格式 

```markdown
  - 无序列表1
  - 无序列表2
  - 无序列表3

  1. 有序列表1
  2. 有序列表2
  3. 有序列表3

  - [ ] 任务列表1
  - [ ] 任务列表2
  - [x] 任务列表3
  - [x] 任务列表4

  | Tables        | Are           | Cool  |
  | ------------- |:-------------:| -----:|
  | col 3 is      | right-aligned | $1600 |
  | col 2 is      | centered      |   $12 |
  | zebra stripes | are neat      |    $1 |
```
::: collapse
- 演示
  - 无序列表1
  - 无序列表2
  - 无序列表3

  1. 有序列表1
  2. 有序列表2
  3. 有序列表3

  - [ ] 任务列表1
  - [ ] 任务列表2
  - [x] 任务列表3
  - [x] 任务列表4

  | Tables        | Are           | Cool  |
  | ------------- |:-------------:| -----:|
  | col 3 is      | right-aligned | $1600 |
  | col 2 is      | centered      |   $12 |
  | zebra stripes | are neat      |    $1 |



