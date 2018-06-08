父类属性

1. `display:flex `

   - 父类设置 ，子类享受
   - 两个方向轴（main axis）和（cross axis）
2. `flex-wrap: `

   - 项目是否可拆
   - 子类中默认为nowrap
   - 常用可选值nowrap、wrap、wrap-reverse
3. `flex-direction` 

   - 指定主轴方向
   - 默认为row，可选column
4. `flex-flow: row wrap;`
   - flex 包含多种属性时 简写方式
5. `align-items`

   - 调整项目的位置布局
   - 默认的值是 `stretch`，其会使所有 flex 项沿着交叉轴的方向拉伸以填充父容器。 
6. `justify-content `

   - 默认值是 `flex-start` 
   - `center` 在 `justify-content` 里也是可用的，可以让 flex 项在主轴居中。
   - 而我们上面用到的值 `space-around` 是很有用的——它会使所有 flex 项沿着主轴均匀地分布，在任意一端都会留有一点空间。
7. `order`
   - 调整项目顺序
   - 默认为0，值越小，优先级越高

子类属性

1. `flex: `

   - 尺寸调节
   - 其后三个属性*flex-grow* *flex-shrink* *flex-basis* 
     1. *flex-grow*
        - 拉伸因子，值取整
     2. *flex-shrink*
        - 收缩因子，值取整
     3. *flex-basis*
        - 指定了 flex 元素在主轴方向上的初始大小 

   


flex-basis 下含的几个属性并不知道说什么