# CSS-  
##OO CSS的作用：  
    1.加强代码维护以及方便复用  
    2.减小CSS体积  
    3.提升渲染效率  
    4.组件库思想，栅格布局可共用，减少选择器，方便扩展。  
    
##OO CSS的注意事项：  
    1.不要直接定义子节点，把共性声明放到父类。  
    2.结构和皮肤相分离
    3.容器与内容相分离  
      example：  
        <div class="container"><ul><li>排行</li></ul></div>  
        .container ul{....}    //ul依赖了容器  
        
        <div class="container"><ul class="rankList"><li>排行</li></ul></div>  
        .rankList {...}   //解除与容器的依赖  
    4.抽象出可重用的元素，建好组件库，在组件库内寻找可用的元素组装页面  
    5.避免使用ID选择器，权重太高，无法重用  
    6.保证选择器相同的权重  
    7.类名 简短 清晰 语义化  
      
## CSS3新加的选择器：  
        1.[att*=val]：表示包含val的所有att，注意只要包含就行。举例：  
                在HTML中：
                <div id="container">  
                    <div id="div1"></div>
                    <div id="div2"></div>
                    <div id="div3"></div>
                    <div id="div4"></div>
                    <div id="other"></div>
                </div>    
                
                在CSS中：  
                [id*=div] {...} 就表示选择了所有id包含div的标签
        2.[att^=val]:表示开头为val的所有att ，这里区别于上一种，只有开头是val才会被选中。  
        3.[att&=val]:表示以val结尾的att。比如某标签：id="my"，那么[att&=y]可选中改标签。如果要使用数字，那么数字前要加\,比如[id&=\1].
