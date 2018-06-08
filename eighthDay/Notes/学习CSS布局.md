布局

1. display 

   1. block 块级元素
   2. inline 行内元素
   3. none

2. margin

3. width:

   1. max-width

4. 盒模型

5. box-sizing

6. position 

   - 四个调节距离的属性 top,right,bottom,left

   1. static 元素不会被特殊的定位 
   2. relative 相对布局  原有位置留空
   3. fixed 固定布局 
   4. absolute  绝对定位 
      1. 相对于*最近的“positioned”祖先元素* 
      2. 如果绝对定位（position属性的值为absolute）的元素没有“positioned”祖先元素，那么它是相对于文档的 body 元素，并且它会随着页面滚动而移动。 

7. float

8. 清除浮动（clearfix hack）

   - ```
     .clearfix {
       overflow: auto;
     }
     ```

9. 媒体查询 @media 

10. inline-block

    - 有事可起到类似（float）浮动的效果

11. columns 列（以下常用参数）

    1. column-count 分为多列
    2. column-gap 列中**间隙**
    3. Column-rule  规定列之间的**宽度、样式和颜色**。