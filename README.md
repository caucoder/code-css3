# code-css3

learning css

---

## selector

1. css 引入方式： inline,embedded,external
   1.1 注意 default browsers css style
2. id 在 page 中是唯一的，class 可以多次使用
3. Inheritance 层次嵌套，conflicts 冲突,权重(override)

   ```
   id(100points)>class(10points)>element(1points)
   ```

4. [`descendants(后代)与 direct child`](./selector)

   ```css
   /* 所有后代 */
   #main p {
     color: red;
   }
   /* 直接 child */
   #main > p {
     color: red;
   }
   ```

5. 属性值 !important,覆盖

   ```css
   color: red !important;
   ```

6. descendants(嵌套 所有后代),direct child(嵌套 直接后代)

   ```css
   #main p {
   }
   #main > p {
   }
   ```

7. multiple elements have one(same) css style rule

   ```
    p,span,a,li{}
   ```

8. adjacent selector

   ```css
   #all-articles h2 + p {
   }
   ```

9. attribute selector

   ```css
    span[title]{}
    /*more specific*/
    span[title="google"]
   ```

   9.1 multiple class

   ```html
   <span class="deck halls"></span>
   <!-- css  选择class都是deck的span-->
   span[class~="deck"]
   ```

   9.2 特殊符号

   ```css
   /*以属性开头*/
   a[href^="http"] {
   }
   /*以属性结尾*/
   a[href$=".pdf"] {
   }
   ```

10. Pseudo selectors

    ```css
     selector:keyword{
     declaration
     }
    ```

    10.2 keyword: **hover**,**active**,**visited**
    10.3 first & last child selector

    ```css
    /*选择article下的第一个p标签*/
    article p:first-child {
    }
    /*选择article下的最后一个p标签*/
    article p:last-child {
    }
    ```

    10.4 first & last of type selector(类型指的是标签类型)

    ```css
    /* article h1 p 在嵌套中，h1在中间*/
    article p:first-of-type {
    }
    article p:last-of-type {
    }
    ```

    10.5 nth child selector

    ```css
    /*数字*/
    ul: nth-child(2) {

    }
    /*关键字 even odd*/
    ul: nth-child(even) {

    }
    /*公式，n从0开始，默认递增1*/
    ul:nth-child(2n + 1) {
    }
    ```

    10.6 nth of type selector

    ```css
    /*usege like nth-child*/
    article: nth-of-type(2);
    ```

11. combining selectors

    ```css
    /*标签都使用同一个class名称的情况，注意没有空格*/
    article.featured-content {
    }
    div.featured-content {
    }
    ```

12. universal selector 可以 override 浏览器的默认的样式
    ```css
    * {
    }
    ```

> finished selector part

---

## style

1. font-size.

   ```css
   /*absolute size*/
   font-size: 40px;

   /*inherit(父节点,上面样式的样式) relative size*/
   font-size: 4em; /*4倍*/
   font-size: 50%;
   ```

2) The Box Model
   ![](./imgs/box-model.png)

## videos

[youtube-CSS Tutorial For Beginners](https://www.youtube.com/watch?v=MlJrAhGVIis&list=PL4cUxeGkcC9gQeDH6xYhmO-db2mhoTSrT&index=16)
