> JSX

是JavaScript的语法扩展，允许在JavaScript中编写类似于HTML的代码。当使用React时，JSX可以帮助我们轻松创建UI组件。

全称：JavaScript XML

React定义的一种类似于XML的JS扩展语法：JS + XML

本质是React.createElement(component,props,...children)方法的语法糖

用来简化创建虚拟DOM

注：不是字符串也不是HTML/XML标签，它最终产生的是一个JS对象

1. JSX中的标签必须有闭合标签，或者是自闭合标签。

   ```html
   // 闭合标签
   <div> Hello World! </div>
   // 自闭合标签
   <img src="example.png" />
   ```

2. JSX中的标签名可以是一个字符串，一个变量或一个表达式

   ```html
   // 字符串
   <div> Hello World! </div>
   
   // 变量
   const tagName = 'div';
   <tagName> Hello World! </tagName>
   
   // 表达式
   const isTrue = true;
   <div className={isTrue ? 'active' : 'inactive'}> Hello World! </div>
   ```

3. JSX中的注释必须用花括号包裹起来

   ```html
   <div>
     {/* 这是一个注释 */}
     Hello World!
   </div>  
   ```

4. JSX中可以包含JavaScript表达式，用花括号包裹起来

   ```html
   const name = 'Alice';
   <div> Hello {name}! </div>
   ```

5. JSX中的属性名采用驼峰式命名法，而不是HTML中的短横线命名法。

6. 样式的类名指定不要用class，要用className

7. 内联样式，要用style={{key:value}}

8. 标签首字母：若小写字母开头，则将标签转为html中的同名元素，若html中无该标签对应的同名元素，则报错。若大写字母开头，react就会去渲染对应的组件，若组件没有定义则报错。

```html
<div className="wrapper" tabIndex={0}> Hello World! </div>
```

JSX是一种方便编写React组件的语法扩展，它提供了类似于HTML的标记语言，同时也支持JavaScript的表达式和语句。