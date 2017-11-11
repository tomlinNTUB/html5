# 第10課 jQuery UI


## (01u) 待修飾頁面

##### 執行結果:
![GitHub Logo](/imgs/results10-01u.jpg)


##### 檔案放置方式:
```
   | 
   |___<images>
   |     |___ logo.jpg  (尺寸:80px*80px)
   |     |___ 1.jpg     (尺寸:230px*230px)
   |     |___ 2.jpg     (尺寸:230px*230px)
   |     |___ 3.jpg     (尺寸:230px*230px) 
   |   
   |___<css>
   |     |___ main.css
   |
   |___<js>
   |     |___ scripts.js   
   |	 
   |___index.html 
   
```


##### 檔案名稱: index.html 
```html
<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>測試網頁</title>
<!-- 加入 main.css -->
<link rel="stylesheet" href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<link href="css/main.css" rel="stylesheet" type="text/css" />
</head>
<body>
    <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
    <div class="header">
        <!--~~~~~~logo圖片~~~~~-->      
        <img src="images/logo.jpg" class="logo">
        <!--~~~~~~~~~~~~~~~~~~-->         

        <!--~~~導覽列~~~-->  
        <div class="navbar">        
            <ul class="left">
                <a href="#"><li class="item">生活</li></a>
                <a href="#"><li class="item">旅遊</li></a>
            </ul>

            <ul class="right">
                <a href="#"><li class="item">食物</li></a>
                <a href="#"><li class="item">文化</li></a>
            </ul>            
        </div>   
        <!--~~~~~~~~~~~~-->         
    </div>
    <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->  
    
    
    
    <!--==========================================-->
    <div class="container">
        
        <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
        <div class="content">
            <h2 class="title">蔣勳：過得像個人，才能看到美</h2>
    
            <p>蔣勳曾說自己是用佈道的心情傳播對美的感動，現在他已經可說是美的宗教家。近幾年來，蔣勳走遍竹科與各地演講，到場的聽眾們彷彿都期待受到「開釋」，除了在席間對於充滿抑揚頓挫的感性分析頻頻點頭，發問的許多也都是已超乎美學的人生之問。事實上，這幾年來，蔣勳談的美，也有很大的變化。他過去比較偏向幫助大家賞析藝術之美，但他在與聽眾愈來愈多的互動中發現，許多上班族的餘暇時間已極度有限了，刻意附庸風雅地去欣賞音樂會、畫展已經沒有必要，重拾與周遭人的感情，重新找回「像個人樣」的生活方式，才能對美真正有所體會。本期美學學院專訪蔣勳，分享上班族也可以找回的生活之美。</p>
        
            <!--...............-->
            <div class="newsBar">
                <a href="#">
                    <div class="news">
                        <img src="images/1.jpg">
                        <h4>真正的美，作假不得 </h4>                        
                    </div>
                </a>
                
                <a href="#">                
                    <div class="news">
                        <img src="images/2.jpg">
                        <h4>找回人與人之間的感覺 </h4>                    
                    </div>
                </a>    
    
                <a href="#">     			
                    <div class="news">
                        <img src="images/3.jpg">
                        <h4>週休二日，回來做自己 </h4>
                    </div>
                </a>                  
            
            	<div class="clear"></div>
            </div>
            <!--...............-->            
            
        </div>
        <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->      
        
        
        <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
        <div class="footer">
            NTUB imd, 2017.    
        </div>        
        <!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~--> 
	
    </div>
    <!--==========================================-->  
    <!--*********-->
    <!-- 載入js  -->
    <!--*********-->
    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
    <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>      
    <script src="js/scripts.js"></script>          
</body>
</html>
```


##### 檔案名稱: css/main.css
```css
@charset "utf-8";

/*---------------------------*/
/* 引用思源中文                */
/*---------------------------*/
@import url(http://fonts.googleapis.com/earlyaccess/notosanstc.css);


/*---------------------------*/
/* 定義網頁                   */
/*---------------------------*/
html, body{
    font-size:17px;
    /*設定思源中文*/
    font-family: 'Noto Sans TC', sans-serif;
    font-weight: 400;	
    background-color:#444;
    margin:0;	
}


/*---------------------------*/
/* 定義標題                   */
/*---------------------------*/
div.header{
    width:100%;	
    min-width:800px;
    height:80px;
    background:rgba(153,153,153,0.7);    
    position:fixed;
    z-index:20;
    box-shadow:0px 1px 3px 1px #000;
}


/*---------------------------*/
/* 定義logo圖示               */
/*---------------------------*/
div.header img.logo{
    width:80px;
    height:80px;
    border-radius:40px;
    position:absolute;
    z-index:100;
    left:50%;
    top:20px;
    margin-left:-40px;
    box-shadow:0px 1px 3px 1px #000; 
}


/*---------------------------*/
/* 定義導覽列                 */
/*---------------------------*/
div.navbar{	   
    width:800px;
    margin-left:auto;
    margin-right:auto;	
    position:absolute;
    top:40px;
    left:50%;
    margin-left:-400px;	
}

div.navbar ul{	 
    list-style-type:none;
    margin:0;
    padding:0;	
}


div.navbar ul li{
    width:100px;	
    height:40px;
    margin-left:15px;
    margin-right:15px;	
    line-height:40px;	
    text-align:center;
    float:left;	
    color:#fff;	
}

div.navbar ul.left{
    float:left;
    margin-left:50px;
}

div.navbar ul.right{
    float:right;
    margin-right:50px;
}

/*--~~~~~~~~~~~~~~~~~~~~~~~--*/
/* 定義容器                   */
/*--~~~~~~~~~~~~~~~~~~~~~~~--*/
div.container{
    width:800px;	
    position:relative;
    margin-left:auto;
    margin-right:auto;	
    top:80px;
}


/*---------------------------*/
/* 定義內容                   */
/*---------------------------*/
div.content{	   
    padding:0px 25px 20px 25px;
    box-sizing:border-box;
    background:#fff;
    text-align:justify;
    letter-spacing:1px;
    padding-bottom:40px;
}

div.content h2{
    margin-top:0;
    padding-top:25px;	
}

div.content h2:first-child{
    padding-top:55px;
}



/*---------------------------*/
/* 定義最新消息                */
/*---------------------------*/
div.newsBar{
    width:100%;	
    margin-top:40px;
}


div.news{
    width:230px;
    height:300px;
    box-sizing:border-box;
    float:left;
    border:1px solid #000;
    overflow:hidden;	
    position:relative;
    color:#000;
    box-shadow:0px 0px 2px 1px #000; 
}

div.newsBar a:nth-child(1) div.news,
div.newsBar a:nth-child(2) div.news{
    margin-right:30px;
}

div.news img{
    padding-left:0;
    padding-right:0;
}

div.news h4{
    padding-left:10px;
    padding-right:10px;
}

div.clear{	
    clear:both;
}


/*---------------------------*/
/* 定義表尾                   */
/*---------------------------*/
div.footer{
    height:100px;
    line-height:100px;
    background:#CCC;
    font-size:13px;
    text-align:center;
    letter-spacing:3px;
}
```



##### 檔案名稱: js/scripts.js
```js
// 存標題列的狀態
var isOpened=true;

$(function(){
    //------------------------------------
    // 標題列動畫
    //------------------------------------	
    $('.logo').mousedown(function(){
        if(isOpened){
            //標題列動畫
            $(this).parent().stop().animate({top:-80}, {duration:500, easing:'easeOutElastic'});
			
            //logo移動
            $(this).stop().animate({top:50}, {duration:500, easing:'easeOutElastic'});			
			
            isOpened=false;
        }else{
            //標題列動畫			
            $(this).parent().stop().animate({top:0}, {duration:100});
			
            //logo移動			
            $(this).stop().animate({top:20}, {duration:500, easing:'easeOutElastic'});			
	
            isOpened=true;			
        }
    })		
    //------------------------------------
    
    
    
    //------------------------------------	
    // 最新消息動畫
    //------------------------------------	
    $('.news').mouseenter(function(){
        $(this).stop().animate({top:-10}, {duration:500, easing:'easeOutElastic'});
    })	
	
    $('.news').mouseleave(function(){
        $(this).stop().animate({top:0}, {duration:100});
    })
    //------------------------------------
});
```
