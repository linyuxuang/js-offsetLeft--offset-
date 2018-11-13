# js-offsetLeft--offset-
offsetLeft  与 offset
 
       查看元素尺寸 
      dom.offsetWidth 
      dom.offsetHeight

      查看元素的位置
      对于无定位父级元素，返回相对文档的坐标，对于
      有定位父级的元素，返回相对于最近定位的父级元素坐标
      dom .offsetLeft 
      dom.offsetTop 
 
      返回最近有定位的父级，如果没有：返回body，body.offsetParent   
      dom.offsetParent
      

      


       offsetLeft : 
         在页面任一元素的offsetLeft总是找到离其最近的已经定位的父元素或祖先元素定位，如果没有，就根据根节点body定位，然后获取其left值。

      offset 
         返回或设置匹配元素相对于文档的偏移（位置）。
         无论元素的父元素或祖先元素的position属性是什么，总是计算相对于文档的位置。（浏览器窗口离文本的距离）
    
    
      
    
         #parent{
            width: 300px;
            height: 100px;
            /*margin: 0 20px;*/
            border: 1px solid #ccc;
            position: relative;}
        #child{
            width: 120px;
            height: 120px;
            background: grey;
            position: absolute;

        }
    
         <div id="parent">
            <p id="child">测试offsetLeft与offset().left的区别</p>
        </div>

    
          var offsetLeft = document.getElementById('child').offsetLeft;
          var offset = $('#child').offset();
          console.log(offsetLeft);//结果始终是0    //0 
          console.log(offset);//结果是相对于文档的偏移  top:25 left:9
    
