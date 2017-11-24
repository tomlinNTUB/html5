# 第12課 使用Bootstrap框架


##### Bookstrap:
```
http://layoutit.com   
```


##### Bookstrap 版型:
```
https://bootswatch.com  
```


##### Bookstrap 文件:
```
http://getbootstrap.com/
```


##### 執行結果:
![GitHub Logo](/imgs/results12-1.jpg)


##### 檔案放置方式:
```
   | 
   |___<css>
   |     |___ style.css   (原檔為空檔)
   |
   |___<js>
         |___ scripts.js  (原檔為空檔)
```




##### 檔案名稱: css/style.css
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
    /*設定思源中文*/
    font-family: 'Noto Sans TC', sans-serif;
}



/*---------------------------*/
/* 大標題                     */
/*---------------------------*/
div.jumbotron{
    background:#8f3111;
    color:#ffc;	
}


div.jumbotron h2{
    font-family: 'Noto Sans TC', sans-serif;
    font-size:26px;	
    font-weight:400;	
}

div.jumbotron p{
    font-family: 'Noto Sans TC', sans-serif;
    font-size:16px;	
    font-weight:350;
}


/*---------------------------*/
/* 按鈕                      */
/*---------------------------*/
.btn-primary{
    background:#111;
    border:1px solid #fff;
}

.btn-primary:hover{
    background:#222;
    border:1px solid #fff;	
}


/*---------------------------*/
/* 導覽列                     */
/*---------------------------*/
.nav li.active a{	
    color:#FFC;	
}

.nav li.active a:hover{	
    color:#ff0;		
}

.nav li.active a:visited{	
    color:#ffa;		
}


/*---------------------------*/
/* 下拉式選單                 */
/*---------------------------*/
ul.dropdown-menu li:hover a{
    background:#8f3111;	
    color:#ffc;
}

```



##### 檔案名稱: js/scripts.js
```js
// Easing函數使用: easings.net/zh-tw

$(function(){
    // 滑鼠移入	
    $('.thumbnail').mouseenter(function(){
        $(this).stop().animate(
            {
                marginTop:-10,
                backgroundColor:'#333'
            }, 
            {
                duration:300,
                easing:'easeOutBounce'
            });
        }
    );	

    // 滑鼠移出	
    $('.thumbnail').mouseleave(function(){			
        $(this).stop().animate(
            {
                marginTop:0,
                backgroundColor:'#222'
            }, 
            {
                duration:50
            });
        }
    );		
});
```
