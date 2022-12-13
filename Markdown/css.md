
# 选择器

> 详细内容网址: https://www.w3school.com.cn/css/css_selector_class.asp

## 元素选择器

```css
p {
    font-size:28px;
    display: block;
}
h1{  
    font-size:28px;
}
h1{  
    display: block;
}

/*改造成下面的*/
p,h1{
    font-size:28px;
    display: block;
}
```

## 类选择器

```css
<p class='important'></p>
<div class='tem'></div>
<h1 class='important tem'></h1>

.important{
    font-size:28px;
}

/*多类选择器，类顺序无关紧要*/ 
.important.tem{
    font-size:28px;
}

```

## ID选择器

```css
<p id="intro">This is a paragraph of introduction.</p>

#intro {font-weight:bold;}

```

## 属性选择器

```css
/*
<p title="intro">This is a paragraph of introduction.</p>
<a title="W3School Home" href="http://w3school.com.cn">W3School</a>
<a href="http://w3school.com.cn">W3School</a>
*/

*[title] {color:red;}
 
a[href][title] {color:red;} /*多属性*/

a[href="http://www.w3school.com.cn/"][title="W3School"] {color: red;} /*指定属性，属性值需完全匹配*/

p[class~="important"] {color: red;} /* ~= 符号 部分属性匹配*/

*[lang|="en"] {color: red;} /*选择 lang 属性等于 en 或以 en- 开头的所有元素*/
```

|类型|描述|
|:---: | :---:|
|[abc^="def"]|选择 abc **属性值** 以 "def" 开头的所有元素|
|[abc$="def"]|选择 abc **属性值** 以 "def" 结尾的所有元素|
|[abc*="def"]|选择 abc **属性值** 中包含子串 "def" 的所有元素|

## 后代选择器(子标签)

```css
<h1>This is a <em>important</em> heading</h1>
<p>This is a <em>important</em> paragraph.</p>

h1 em {color:red;} /*只会选择第一个,作为 h1 元素后代的任何 em 元素*/
                   /*会一直寻找*/
```
> 选择器之间的空格是一种结合符（combinator）
