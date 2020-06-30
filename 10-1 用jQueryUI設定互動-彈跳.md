# 10-1 用jQueryUI設定互動-彈跳

### 練習重點
```
使用jQueryUI設計使用者互動, 設定動畫, 時間及加速度.
```

### 執行結果:
![GitHub Logo](/imgs/results10-1.jpg)


### 檔案放置方式:
```
|__ index.html  
|   
|__ <css>
|     |__ main.css 
|
|__ <js>
|     |__ main.js 
|
|__ <imgs>
      |__ paper.jpg   (230像素*420像素) 
      |__ 1.jpg       (230像素*96像素) 
      |__ 2.jpg       (230像素*96像素) 
      |__ 3.jpg       (230像素*96像素)   
```


### (1) index.html 
```html
<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>測試網頁</title>
<!-- 連結main.css, jquery-ui.css及思源中文 -->
<link rel="stylesheet" href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<link href="https://fonts.googleapis.com/css?family=Noto+Sans+TC" rel="stylesheet">
<link href="css/main.css" rel="stylesheet" type="text/css" />      
<!------------------------->
</head>
   
<body>
    <!--**************************-->
    <div class="container">    
        <!--~~~~~~~~~~~~~~~~~-->
        <div class="header">
            過得像個人，才能看到美
        </div>
        <!--~~~~~~~~~~~~~~~~~-->
               
        
        <!--~~~~~~~~~~~~~~~~~--> 
        <div class="content">   
                 
            <div class="cardRow">              
                <!-- 卡片(1) -->      
                <div class="card">
                    <img src="imgs/1.jpg">
                    <h3>真正的美，作假不得 </h3>    
                    <p>我原來希望的藝術是能恢復人的品味和人的感覺，但他們接觸了這些東西卻沒有感覺，像有些企業會固定舉辦一些音樂會，但他們卻沒有辦法進入那個世界。所以我現在希望向大家說的是「人的原點」，當我們失去了人的原點，談所有的美.....</p>
                </div>                                 
                
                <!-- 卡片(2) -->  
                <div class="card">
                    <img src="imgs/2.jpg">                
                    <h3>找回人與人之間的感覺 </h3>    
                    <p>我現在不問工程師有沒有去聽音樂、看展覽，反而是問他們：「你們在這裡工作5年了，有沒有人可以告訴我公司門口那一排是什麼樹？」但很少人能夠回答的出來。事實上，他們公司門口那排小葉欖仁的葉子漂亮得不得了，綠色會在陽光裡發亮..... </p>
                </div>                                 
                
                <!-- 卡片(3) -->  
                <div class="card">
                    <img src="imgs/3.jpg">                  
                    <h3>週休二日，回來做自己 </h3>    
                    <p>現在台灣過週休二日，好像非要全家去吃一個餐廳、到哪裡去看薰衣草、喝咖啡，全部整套，然後全部的人塞車塞到一肚子氣。我們對休閒的定義是滿僵化的，好像一定要別人服務我們才算是休閒。我自己假日的時候喜歡自己一個人做4菜1湯.....</p>
                </div>                               
            </div>  
                           
        </div>
        <!--~~~~~~~~~~~~~~~~~-->
        
        
        <!--~~~~~~~~~~~~~~~~~--> 
        <div class="footer">
            NTUB imd, 2019.    
        </div>        
        <!--~~~~~~~~~~~~~~~~~-->         
    </div>
    <!--**************************--> 
    <!-- 載入js                    -->
    <!--**************************--> 
    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
    <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>      
    <script src="js/main.js"></script>    
</body>
   
</html>
```


### (2) main.css

```css
@charset "utf-8";

/*---------------------------*/
/* 編排網頁                   */
/*---------------------------*/
html, body{
    font-family: 'Noto Sans TC', sans-serif; 
    background:#444;
}

/*---------------------------*/
/* 編排<容器>區塊             */
/*---------------------------*/
div.container{
    width:800px;
    border:1px solid #666;  
    margin:10px auto 10px auto;
    background:#fff;
    box-shadow:0px 0px 10px 0px #000;
}

/*---------------------------*/
/* 編排<標題>區塊             */
/*---------------------------*/
div.header{
    height:150px;
    background:#CCC;
    font-size:40px;
    text-align:center;
    line-height:150px;
    letter-spacing:7px;
}

/*---------------------------*/
/* 編排<內文>區塊             */
/*---------------------------*/
div.content{
    padding:20px 25px;    
    text-align:justify;
}

/* 定義卡片列 */
div.cardRow{
    margin-top:25px;
    margin-bottom:25px;	
}

/* 定義卡片 */
div.card{       
    width:230px;
    height:420px;
    background:url(../imgs/paper.jpg);
    box-sizing:border-box;
    float:left; 
    overflow:hidden;    
    border:1px solid #000;
    box-shadow:0px 0px 2px 0px #000;       
}

/* 卡片標題 */
div.card h3{ 
    padding:0 12px;
    font-size:20px;
}

/* 卡片內文 */
div.card p{   
    padding:0px 12px 15px 12px;     
    text-align:justify;
    font-size:16px;
}

/* 第1, 2張卡片 */
div.card:nth-child(1),
div.card:nth-child(2){   
    margin-right:30px;
}

/*清除卡片區塊的浮動*/
div.cardRow:after {      
    content: '';
    display: block;
    clear: both;
}

/*---------------------------*/
/* 編排<表尾>區塊             */
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


### (3) main.js

``` js
// Easing函數使用: easings.net/zh-tw

$(function(){
    // 滑鼠移入	
    $('.card').mouseenter(function(){        
        $(this).stop().animate({top:-20}, {duration:300, easing:'easeOutBounce'}); 
    });	

    // 滑鼠移出	
    $('.card').mouseleave(function(){        
        $(this).stop().animate({top:0}, {duration:50});
    });		
});
```
