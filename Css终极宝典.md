#### CSS 简介

- *CSS* 指的是层叠样式表* (*C*ascading *S*tyle *S*heets)
- CSS 从 HTML 页面中删除了样式格式！
- 通过使用外部样式表文件，您只需更改一个文件即可更改整个网站的外观！

#### CSS 语法

```scss
p {  //选择器 selector 指向HTML元素
  color: red;  //属性 key
  text-align: center;  //属性值 value
}
```

#### CSS 选择器

- CSS id 选择器

  ```scss
  //这条 CSS 规则将应用于 id="para1" 的 HTML 元素：
  #para1 {
    text-align: center;
    color: red;
  }
  ```

-  CSS 类选择器

  ```scss
  #所有带有 class="center" 的 HTML 元素将为红色且居中对齐：
  .center {
    text-align: center;
    color: red;
  }
  #只有具有 class="center" 的 <p> 元素会居中对齐：
  p.center {
    text-align: center;
    color: red;
  }
  #<p> 元素将根据 class="center" 和 class="large" 进行样式设置：
  <p class="center large">这个段落引用两个类。</p>
  ```

- CSS 通用选择器

  ```scss
  #通用选择器（*）选择页面上的所有的 HTML 元素。
  下面的 CSS 规则会影响页面上的每个 HTML 元素：
  * {
    text-align: center;
    color: blue;
  }
  ```

- CSS 分组选择器

  ```scss
  #分组选择器选取所有具有相同样式定义的 HTML 元素。等同于h1，h2，p 相同
  h1, h2, p {
    text-align: center;
    color: red;
  }
  ```

#### CSS 使用

- 外部 CSS    外部样式在 HTML 页面 <head> 部分内的 <link> 元素中进行定义：

  ```html
  <link rel="stylesheet" type="text/css" href="mystyle.css">
  ```

- 内部 CSS   内部样式是在 head 部分的 <style> 元素中进行定义。

  ```scss
  # style.css
  <style>
  body {
    background-color: linen;
  }
  h1 {
    color: maroon;
    margin-left: 40px;
  } 
  </style>
  ```

- 行内 CSS   行内样式在相关元素的 "style" 属性中定义：

  ```scss
  <p style="color:red;">This is a paragraph.</p>
  ```

  (其中第一优先级最高)

  1. 行内样式（在 HTML 元素中）
  2. 外部和内部样式表（在 head 部分）
  3. 浏览器默认样式

#### CSS 注释

```scss
/* 这是一条单行注释 */
<!--...--> 
```

#### CSS 颜色

![css 颜色](/Users/ling/Code/Css Style/Snapshot/css 颜色.png)

#### CSS RGB 颜色

- rgb 每个参数 (*red*、*green* 以及 *blue*) 定义了 0 到 255 之间的颜色强度。
- rgba  颜色值是具有 alpha 通道的 RGB 颜色值的扩展 - 它指定了颜色的不透明度。
- *alpha* 参数是介于 0.0（完全透明）和 1.0（完全不透明）之间的数字。

#### CSS HEX 颜色

- 其中 rr（红色）、gg（绿色）和 bb（蓝色）是介于 00 和 ff 之间的十六进制值（与十进制 0-255 相同）。

#### CSS HSL 颜色

- 在 CSS 中，可以使用色相、饱和度和明度（HSL）来指定颜色。

- **hsla(*hue*, *saturation*, *lightness*)**

- 色相（*hue*）是色轮上从 0 到 360 的度数。0 是红色，120 是绿色，240 是蓝色。

  饱和度（*saturation*）是一个百分比值，0％ 表示灰色阴影，而 100％ 是全色。

  亮度（*lightness*）也是百分比，0％ 是黑色，50％ 是既不明也不暗，100％是白色。

  ![截屏2022-03-23 00.30.32](/Users/ling/Code/Css Style/Snapshot/HSL 颜色.png)

#### CSS 背景

- **background-color**  属性指定用作元素背景的颜色。

  ```scss
  div {
    background-color: green;
    opacity: 0.3;  //不透明度 /透明度
  }
  div {
    background: rgba(0, 128, 0, 0.3) /* 30% 不透明度的绿色背景 */
  }
  ```

  

#### CSS 背景图像

- **background-image**  属性指定用作元素背景的图像。

  ```scss
  body {
    background-image: url("paper.gif");
  }
  还可以为特定元素设置背景图像，例如 <p> 元素：
  p {
    background-image: url("paper.gif");
  }
  ```

#### CSS 背景重复

- **background-image** 属性在水平和垂直方向上都重复图像。

  ```scss
  body {
    background-image: url("gradient_bg.png");
    background-repeat: repeat-x;
  }
  提示：如需垂直重复图像，请设置 background-repeat: repeat-y;
  ```

  

#### CSS 背景附着

- **background-attachment** 属性指定背景图像是应该滚动还是固定的（不会随页面的其余部分一起滚动）

```scss
# 指定应该固定背景图像：
body {
  background-image: url("tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: fixed;
}
# 指定背景图像应随页面的其余部分一起滚动：
body {
  background-image: url("tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: scroll;
}
```



#### CSS 简写背景属性

- CSS background - 简写属性

  ```scss
  body {
    background-color: #ffffff;
    background-image: url("tree.png");
    background-repeat: no-repeat;
    background-position: right top;
  }
  # 简写
  body {
    background: #ffffff url("tree.png") no-repeat right top;
  }
  ```

  

#### CSS 边框

- CSS border 属性允许您指定元素边框的样式、宽度和颜色。

- CSS 边框样式

  border-style 属性指定要显示的边框类型。

  允许以下值：

  - dotted - 定义点线边框
  - dashed - 定义虚线边框
  - solid - 定义实线边框
  - double - 定义双边框
  - groove - 定义 3D 坡口边框。效果取决于 border-color 值
  - ridge - 定义 3D 脊线边框。效果取决于 border-color 值
  - inset - 定义 3D inset 边框。效果取决于 border-color 值
  - outset - 定义 3D outset 边框。效果取决于 border-color 值
  - none - 定义无边框
  - hidden - 定义隐藏边框

  border-style 属性可以设置一到四个值（用于上边框、右边框、下边框和左边框）。

  ```scss
     * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
          border: 0px  solid
        }
        #my_button {
          width: 200px;
          height: 100px;
          border-left: 6px solid #2196f3;
          background-color: #ddffff;
        }
  ```

![CSS 边框](/Users/ling/Code/Css Style/Snapshot/CSS 边框.png)



#### CSS 边框宽度

- **border-width** 属性指定四个边框的宽度

  ```scss
  p.three {
    border-style: solid;
    border-width: 25px 10px 4px 35px; /* 上边框 25px，右边框 10px，下边框 4px，左边框 35px */
  }
  ```

  

#### CSS 边框颜色

- 特定边框的颜色

  ```scss
  p.one {
    border-style: solid;
    border-color: red green blue yellow; /* 上红、右绿、下蓝、左黄 */
  }
  ```

#### CSS 边框各边

- 不同的边框样式

  ```scss
  /* 四个值 */
  p {
    border-style: dotted solid double dashed; 
  }
  ```

  

#### CSS 简写边框属性

```scss
border-width
border-style（必需）
border-color
```

- 左边框

  ```scss
  p {
    border-left: 6px solid red;
    background-color: lightgrey;
  }
  ```

  

#### CSS 圆角边框

- border-radius 属性用于向元素添加圆角边框：

  ```scss
  p {
    border: 2px solid red;
    border-radius: 5px;
  }
  ```

  

#### CSS 外边距

- margin 属性用于在任何定义的边框之外，为元素周围创建空间。

  ```scss
  # key
  margin-top
  margin-right
  margin-bottom
  margin-left
  # value
  auto - 浏览器来计算外边距
  length - 以 px、pt、cm 等单位指定外边距
  % - 指定以包含元素宽度的百分比计的外边距
  inherit - 指定应从父元素继承外边距
  ```

- Margin - 简写属性

  ```scss
  p {
    margin: 25px 50px 75px 100px;
  }
  ```

- auto 值   可以将 margin 属性设置为 auto，以使元素在其容器中水平居中。

- inherit 值   使 <p class="ex1"> 元素的左外边距继承自父元素（<div>）：

  ```scss
  div {
    border: 1px solid red;
    margin-left: 100px;
  }
  
  p.ex1 {
    margin-left: inherit;
  }
  ```

  

#### CSS 外边距合并

- 外边距不作为实际边距的计算值

#### CSS 内边距

- CSS padding 属性用于在任何定义的边界内的元素内容周围生成空间。

- 外边距不可以负值。

- 内边距和元素宽度，width 属性指定元素内容区域的宽度。内容区域是元素（盒模型）的内边距、边框和外边距内的部分。

  因此，如果元素拥有指定的宽度，则添加到该元素的内边距会添加到元素的总宽度中。这通常是不希望的结果

#### CSS 高度/宽度

## CSS 高度和宽度值

height 和 width 属性可设置如下值：

- auto - 默认。浏览器计算高度和宽度。
- *length* - 以 px、cm 等定义高度/宽度。
- % - 以包含块的百分比定义高度/宽度。
- initial - 将高度/宽度设置为默认值。
- inherit - 从其父值继承高度/宽度。

#### CSS 框模型

- 在 CSS 中，在谈论设计和布局时，会使用术语“盒模型”或“框模型”。
- CSS 框模型实质上是一个包围每个 HTML 元素的框。它包括：外边距、边框、内边距以及实际的内容。

#### CSS 轮廓

- 轮廓是在元素周围绘制的一条线，在边框之外，以凸显元素。
- CSS 拥有如下轮廓属性：
  - outline-style
  - outline-color
  - outline-width
  - outline-offset
  - outline

#### CSS 轮廓宽度

- outline-width 属性指定轮廓的宽度，并可设置如下值之一：
  - thin（通常为 1px）
  - medium（通常为 3px）
  - thick （通常为 5px）
  - 特定尺寸（以 px、pt、cm、em 计）

#### CSS 轮廓颜色

- outline-color 属性用于设置轮廓的颜色。

#### CSS 简写轮廓属性

- outline 属性是用于设置以下各个轮廓属性的简写属性：
  - outline-width
  - outline-style（必需）
  - outline-color

#### CSS 轮廓偏移

- outline-offset 属性在元素的轮廓与边框之间添加空间。元素及其轮廓之间的空间是透明的。

#### CSS 文本

- color 属性用于设置文本的颜色。

#### CSS 文本对齐

- text-align 属性用于设置文本的水平对齐方式。

- 文本方向  direction 和 unicode-bidi 属性可用于更改元素的文本方向

- 垂直对齐  vertical-align 属性设置元素的垂直对齐方式。

  ```scss
  img.top {
    vertical-align: top;
  }
  
  img.middle {
    vertical-align: middle;
  }
  
  img.bottom {
    vertical-align: bottom;
  }
  ```

  

#### CSS 文本装饰

- text-decoration 属性用于设置或删除文本装饰。
- text-decoration: none; 通常用于从链接上删除下划线：

#### CSS 文本转换

- text-transform 属性用于指定文本中的大写和小写字母。

  ```scss
  #全部大写
  p.uppercase {
    text-transform: uppercase;
  }
  #全部小写
  p.lowercase {
    text-transform: lowercase;
  }
  #首字母大写
  p.capitalize {
    text-transform: capitalize;
  }
  ```

  

#### CSS 文字间距

- 缩进  text-indent 属性用于指定文本第一行的缩进

- 间距  letter-spacing 属性用于指定文本中字符之间的间距

- 行高  line-height 属性用于指定行之间的间距

- 字间距  word-spacing 属性用于指定文本中单词之间的间距。

- 空白换行 white-space 属性指定元素内部空白的处理方式。

  ```scss
  p {
    white-space: nowrap; //不换行
  }
  ```

#### CSS 文本阴影

- text-shadow 属性为文本添加阴影。

- 最简单的用法是只指定水平阴影（2px）和垂直阴影（2px）

  ```scss
  h1 {
    text-shadow: 2px 2px;
  }
  #向阴影添加颜色（红色）
  h1 {
    text-shadow: 2px 2px red;
  }
  #向阴影添加模糊效果（5px）
  h1 {
    text-shadow: 2px 2px 5px red;
  }
  ```



#### CSS 字体

- 衬线字体（Serif）- 在每个字母的边缘都有一个小的笔触。它们营造出一种形式感和优雅感。
- 无衬线字体（Sans-serif）- 字体线条简洁（没有小笔画）。它们营造出现代而简约的外观。
- 等宽字体（Monospace）- 这里所有字母都有相同的固定宽度。它们创造出机械式的外观。
- 草书字体（Cursive）- 模仿了人类的笔迹。
- 幻想字体（Fantasy）- 是装饰性/俏皮的字体。

#### CSS 字体样式

- font-style 属性主要用于指定斜体文本。
  - normal - 文字正常显示
  - italic - 文本以斜体显示

- font-weight 属性指定字体的粗细

#### CSS 字体大小

- font-size 属性设置文本的大小。

- 用 em 设置字体大小

  - 为了允许用户调整文本大小（在浏览器菜单中），许多开发人员使用 em 而不是像素。

  - W3C 建议使用 em 尺寸单位。

  - 1em 等于当前字体大小。浏览器中的默认文本大小为 16px。因此，默认大小 1em 为 16px。

  - 可以使用这个公式从像素到 em 来计算大小：pixels/16=em。

    ```scss
    h1 {
      font-size: 2.5em; /* 40px/16=2.5em */
    }
    
    h2 {
      font-size: 1.875em; /* 30px/16=1.875em */
    }
    ```

- 响应式字体大小

  - 可以使用 vw 单位设置文本大小，它的意思是“视口宽度”（"viewport width"）。
  - 视口（Viewport）是浏览器窗口的大小。 1vw = 视口宽度的 1％。如果视口为 50 厘米宽，则 1vw 为 0.5 厘米。

  

#### CSS 谷歌字体

- 如果您不想使用 HTML 中的任何标准字体，则可以使用 Google Fonts API 向页面添加数百种其他字体。

#### CSS 简写字体属性

font 属性是以下属性的简写属性：

- font-style
- font-variant
- font-weight
- font-size/line-height
- font-family

#### CSS 图标

- 如需使用 Bootstrap glyphicons，请在 HTML 页面的 <head> 部分内添加这行：

  ```html
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <!-- use -->
  <i class="glyphicon glyphicon-cloud"></i>
  ```



#### CSS 链接

- 设置链接样式 

  链接可以使用任何 CSS 属性（例如 color、font-family、background 等）来设置样式。

- 可以根据链接处于什么状态来设置链接的不同样式。

  四种链接状态分别是：

  - a:link - 正常的，未访问的链接

  - a:visited - 用户访问过的链接

  - a:hover - 用户将鼠标悬停在链接上时

  - a:active - 链接被点击时

    ```scss
    /* 未被访问的链接 */
    a:link {
      color: red;
    }
    
    /* 已被访问的链接 */
    a:visited {
      color: green;
    }
    
    /* 将鼠标悬停在链接上 */
    a:hover {
      color: hotpink;
    }
    
    /* 被选择的链接 */
    a:active {
      color: blue;
    }
    ```

    如果为多个链接状态设置样式，请遵循如下顺序规则：

    - a:hover 必须 a:link 和 a:visited 之后
    - a:active 必须在 a:hover 之后

#### CSS 列表

- list-style-type 属性指定列表项标记的类型。

```scss
ul.a {
  list-style-type: circle; //圆形
}

ul.b {
  list-style-type: square;//方块
}

ol.c {
  list-style-type: upper-roman;//罗马数字
}

ol.d {
  list-style-type: lower-alpha;//英文abc
}
```

- list-style-image 属性将图像指定为列表项标记：

  ```scss
  ul {
    list-style-image: url('sqpurple.gif');
  }
  ```

- 定位列表项标记

  - list-style-position 属性指定列表项标记（项目符号）的位置。

    "list-style-position: outside;" 表示项目符号点将在列表项之外。

    "list-style-position: inside;" 表示项目符号将在列表项内。

## CSS 表格

**使用 CSS 可以极大地改善 HTML 表格的外观：**

| Company   | Contact              | Address                                            | City          |
| :-------- | :------------------- | :------------------------------------------------- | :------------ |
| Alibaba   | Ma Yun               | No. 699, Wangshang Road, Binjiang District         | Hangzhou      |
| APPLE     | Tim Cook             | 1 Infinite Loop Cupertino, CA 95014                | Cupertino     |
| BAIDU     | Li YanHong           | Lixiang guoji dasha,No 58, beisihuanxilu           | Beijing       |
| Canon     | Tsuneji Uchida       | One Canon Plaza Lake Success, NY 11042             | New York      |
| Google    | Larry Page           | 1600 Amphitheatre Parkway Mountain View, CA 94043  | Mountain View |
| HUAWEI    | Ren Zhengfei         | Putian Huawei Base, Longgang District              | Shenzhen      |
| Microsoft | Bill Gates           | 15700 NE 39th St Redmond, WA 98052                 | Redmond       |
| Nokia     | Olli-Pekka Kallasvuo | P.O. Box 226, FIN-00045 Nokia Group                | Helsinki      |
| SONY      | Kazuo Hirai          | Park Ridge, NJ 07656                               | Park Ridge    |
| Tencent   | Ma Huateng           | Tencent Building, High-tech Park, Nanshan District | Shenzhen      |

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_fancy)

## 表格边框

如需在 CSS 中设置表格边框，请使用 border 属性。

下例为 <table>、<th> 和 <td> 元素规定了黑色边框：

| Firstname | Lastname |
| --------- | -------- |
| Bill      | Gates    |
| Steve     | Jobs     |

### 实例

```
table, th, td {
  border: 1px solid black;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=js_ajax_xmlhttp)

**注意：**上例中的表格拥有双边框。这是因为 table 和 <th> 和 <td> 元素都有单独的边框。

## 全宽表格

在某些情况下，上表似乎很小。如果您需要一个可以覆盖整个屏幕（全宽）的表格，请为 <table> 元素添加 width: 100%：

### 实例

```
table {
  width: 100%;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_fullwidth)

### 双边框

请注意上面的表格有双边框。这是因为表格和 th、td 元素都有单独的边框。

如需删除双边框，请看下面的例子。

## 合并表格边框

border-collapse 属性设置是否将表格边框折叠为单一边框：

| Firstname | Lastname |
| --------- | -------- |
| Bill      | Gates    |
| Steve     | Jobs     |

### 实例

```
table {
  border-collapse: collapse;
}

table, th, td {
  border: 1px solid black;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_border-collapse)

如果只希望表格周围有边框，则仅需为 <table> 指定 border 属性：

| Firstname | Lastname |
| --------- | -------- |
| Bill      | Gates    |
| Steve     | Jobs     |

### 实例

```
table {
  border: 1px solid black;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_border_2)

## 表格宽度和高度

表格的宽度和高度由 width 和 height 属性定义。

下例将表的宽度设置为 100％，将 <th> 元素的高度设置为 50px：

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
table {
  width: 100%;
}

th {
  height: 50px;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_width_1)

要创建仅占页面一半的表，请使用 width: 50%：

### 实例

```
table {
  width: 50%;
}

th {
  height: 70px;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_width_2)

## 水平对齐

text-align 属性设置 <th> 或 <td> 中内容的水平对齐方式（左、右或居中）。

默认情况下，<th> 元素的内容居中对齐，而 <td> 元素的内容左对齐。

要使 <td> 元素的内容也居中对齐，请使用 text-align: center：

| Firstname | Lastname | Savings |
| :-------: | :------: | :-----: |
|   Bill    |  Gates   |  $100   |
|   Steve   |   Jobs   |  $150   |
|   Elon    |   Musk   |  $300   |

### 实例

```
th {
  text-align: center;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_align_center)

下例使 <th> 元素中的文本左对齐：

| Firstname | Lastname | Savings |
| :-------- | :------- | :------ |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
th {
  text-align: left;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_align)

## 垂直对齐

vertical-align 属性设置 <th> 或 <td> 中内容的垂直对齐方式（上、下或居中）。

默认情况下，表中内容的垂直对齐是居中（<th> 和 <td> 元素都是）。

下例将 <td> 元素的垂直文本对齐方式设置为下对齐：

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
td {
  height: 50px;
  vertical-align: bottom;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_vertical-align)

## 表格内边距

如需控制边框和表格内容之间的间距，请在 <td> 和 <th> 元素上使用 padding 属性：

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
th, td {
  padding: 15px;
  text-align: left;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_padding)

## 水平分隔线

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

向 <th> 和 <td> 添加 border-bottom 属性，以实现水平分隔线：

### 实例

```
th, td {
  border-bottom: 1px solid #ddd;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_border_divider)

## 可悬停表格

在 <tr> 元素上使用 :hover 选择器，以突出显示鼠标悬停时的表格行：

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
tr:hover {background-color: #f5f5f5;}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_hover)

## 条状表格

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

为了实现斑马纹表格效果，请使用 nth-child() 选择器，并为所有偶数（或奇数）表行添加 background-color：

### 实例

```
tr:nth-child(even) {background-color: #f2f2f2;}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_striped)

## 表格颜色

下例指定了 <th> 元素的背景颜色和文本颜色：

| Firstname | Lastname | Savings |
| --------- | -------- | ------- |
| Bill      | Gates    | $100    |
| Steve     | Jobs     | $150    |
| Elon      | Musk     | $300    |

### 实例

```
th {
  background-color: #4CAF50;
  color: white;
}
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_color)

## 响应式表格

如果屏幕太小而无法显示全部内容，则响应式表格会显示水平滚动条：

| First Name | Last Name | Points | Points | Points | Points | Points | Points | Points | Points | Points | Points |
| ---------- | --------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Bill       | Gates     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     | 50     |
| Steve      | Jobs      | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     | 94     |
| Elon       | Musk      | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     | 67     |

在 <table> 元素周围添加带有 overflow-x:auto 的容器元素（例如 <div>），以实现响应式效果：

### 实例

```
<div style="overflow-x:auto;">

<table>
... table content ...
</table>

</div>
```

[亲自试一试](https://www.w3school.com.cn/tiy/t.asp?f=css_table_responsive)

**注释：**在 OS X Lion（在 Mac 上）中，滚动条默认情况下是隐藏的，并且仅在使用时显示（即使设置了 "overflow:scroll"）。

## 更多实例

- [做一张花式表格](https://www.w3school.com.cn/tiy/t.asp?f=css_table_fancy)

  本例演示如何创建花式表格。

- [设置表格标题的位置](https://www.w3school.com.cn/tiy/t.asp?f=css_table_caption-side)

  本例演示了如何放置表格标题。

## CSS 表格属性

| 属性                                                         | 描述                                           |
| :----------------------------------------------------------- | :--------------------------------------------- |
| [border](https://www.w3school.com.cn/cssref/pr_border.asp)   | 简写属性。在一条声明中设置所有边框属性。       |
| [border-collapse](https://www.w3school.com.cn/cssref/pr_border-collapse.asp) | 规定是否应折叠表格边框。                       |
| [border-spacing](https://www.w3school.com.cn/cssref/pr_border-spacing.asp) | 规定相邻单元格之间的边框的距离。               |
| [caption-side](https://www.w3school.com.cn/cssref/pr_tab_caption-side.asp) | 规定表格标题的位置。                           |
| [empty-cells](https://www.w3school.com.cn/cssref/pr_tab_empty-cells.asp) | 规定是否在表格中的空白单元格上显示边框和背景。 |
| [table-layout](https://www.w3school.com.cn/cssref/pr_tab_table-layout.asp) | 设置用于表格的布局算法。                       |