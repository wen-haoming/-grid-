table            缺点  需要全局加载完后才渲染
float            缺点  浮动流而且是只能横向
position         缺点  如果遇到放大缩小的问题容易错位
flex             缺点 只能一个维度

grid 优势 
        1，固定或弹性的轨道尺寸
        2，定位项目
        3，创建额外的轨道来保存内容
        4，对齐控制
        5，控制重叠内容 
 flexbox 与 grid 很好的配合使用


1，网格容器  grid container
    元素应用：display:grid -----> 它是所有网格项的父元素

2，网格项  grid item
     在网格容器内部都是称为网格项

3， 网格线  grid line
     组成网格项的分界线

4， 网格轨道 grid track 
    两个相邻的网格线之间为网格轨道

5， 网格单元  grid cell
两个相邻的列网格线和两个相邻的行网格线组成的是网格单元

6，网格区域  grid area
    四个网格线包围的总空间

7，单位
    fr 剩余空间的分配数，用于在一些列长度值中分配剩余空间。
    gr 网格数 （还在定稿）


容器中的属性
    1,display
        grid 属性默认为块级
            column, float, clear, vertical-align属性无效
            grid inline-grid属性为行内网格 （通常使用flex-box来取代）

    2, grid-template
                使用以空格分隔的多个值来定义网格的列和行
            1，grid-template-columns
               <track-size> .. | <line-name>  <track-size> ..
            2，grid-template-rows
               <track-size> .. | <line-name>  <track-size> ..
                    其中属性值
                    轨道大小 track-size 可以使用css长度（px,em）百分比，或者用分数(fr单位)
            3， 网格线名字 （line-name） 可以选择任何名字 --:> 是为了网格区域服务的
            4，gird-template-areas:
                通过引用grid-area属性指定的网格区域的名称来定义网格模板
                属性值： grid-area-name 使用grid-area属性设置的网格区域的名称
                “.” 点号代表一个空网格单元
                none： 没有定义网格区域
                每一行都是一个双引号，每一行没逗号没分号
                网格的区域的命名会影响网格线
            5,简写
                grid-template
    
    3, gap
        grid-column-gap / grid-row-gap
        指定网格线的大小,可以想象为设置列 / 行的之间距的宽度
        **这里只控制里面的不控制包在外面的
    
    4，item   justify-items 
            沿着行轴对齐网格内的内容
            start 内容与网格区域的左端对齐
            end 内容与网格区域的右端对齐
            center 内容位于网格区域的中间位置
            stretch 内容宽度占据整个网格区域空间(这是默认值)
        align-content 
            跟以上一样
        place-items 列 行
    
    5, content 
        justify-contnet 
            设置网格容器内的网格沿着行轴对齐网格的对齐方式
            start | end | center | stretch(调整grid item的大小宽度填充整个网格容器) | space-around grid item 之间设置等宽度的空间间隙 
            space-between在grid item 之间设置均等宽度空白间隙，其外边缘无间隙
            sapce-evenly 在每个grid item 之间设置均等宽度的空白间隙，包括外边缘
        还有align-content
    
    6，grid-auto                    


-----------------------------------------------------------------------------------
网各项上的属性
    start / end  
        grid-column-start: name | number | span number | span name |auto
        grid-column-end
        grid-row-start
        grid-row-end
    grid-area
    self





