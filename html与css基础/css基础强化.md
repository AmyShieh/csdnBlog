####css权重问题
    行内样式优先级最高
    #id +100
    .class +10
    e +1
    其他 +0;
    浏览器渲染DOM为从右往左的顺序（解析css,快速确定元素）
    
    权重值计算的时候，不进位
    
####选择器分类
    元素，伪元素（元素实际存在），类选择器，属性选择器，伪类选择器（元素的状态），id选择器，组合选择器，否定选择器，通用选择器（*）
    
####css盒模型
    基本概念：padding,margin,border
    盒模型分为标准模型和IE模型
    标准模型：宽度为实际宽度（content）
    IE模型：包括padding和border
    
####css如何设置这两种模型
    box-sizing: content-box
    box-sizing: border-box
    
####js如何设置获取盒模型的对应宽高
    dom.style.width/height
    dom.currentStyle.width/height(Only IE)
    window.getComputedStyle(dom).width/height
    dom.getBoundingClientRect().width/height(get 4 value: left,top,width,height,start form 左顶点，relative position)
    
####BFC(block format context)
#####BFC的原理（BFC的渲染规则）
    bfc的垂直方向的边距发生重叠
    bfc的区域不会与浮动元素的box重叠
    bfc在页面上是一个独立的容器，外面的元素与里面的元素互不干扰。
    计算BFC的高度时，浮动元素参与计算
    
#####如何创建BFC
    1.float的值不为none;
    2.position的值不为relative或者static
    3.display的值为：table或table-cell
    4.父级的overflow不为visible
    
#####BFC的使用场景
    如何使边距不重叠：给元素添加一个父元素，并创建BFC
    当子元素浮动时，父级的高度为0，想要父级的高度也参与计算，则创建BFC;
    清除浮动：跟之前说的一个概念相关，就是在计算bfc的高度时，浮动元素也参与计算，所以BFC是可以清除浮动的，已经，clear也可以清除浮动。
   
    
  
    