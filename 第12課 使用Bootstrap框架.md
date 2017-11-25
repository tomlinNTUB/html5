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
https://v4-alpha.getbootstrap.com/getting-started/introduction/
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
/* 引用思源中文               */
/*---------------------------*/
@import url(http://fonts.googleapis.com/earlyaccess/notosanstc.css);


/*---------------------------*/
/* 定義網頁                   */
/*---------------------------*/
html, body{
    font-family: 'Noto Sans TC', sans-serif;
}


/*---------------------------*/
/* 導覽列的商標標顏色           */
/*---------------------------*/
.navbar-brand{
    color:#FFC;	
}

.navbar-brand:hover{
    color:#FF0;	
}


/*---------------------------*/
/* 導覽列的背景顏色            */
/*---------------------------*/
nav.navbar{
    background:#550000;	
}

/*---------------------------*/
/* 導覽列的文字顏色            */
/*---------------------------*/
nav.navbar ul li a{
    color:#ccc;		
}

/*---------------------------*/
/* 導覽列的項目滑鼠移入時      */
/*---------------------------*/
nav.navbar ul li a:hover{
    background:#801515;
    color:#fff;	
}

/*---------------------------*/
/* 導覽列的項目滑鼠點擊時      */
/*---------------------------*/
nav.navbar ul li a:focus{
    background:#801515;
    color:#fff;
}


/*-------------------------------*/
/* 導覽列的下拉式項目滑鼠移入時     */
/*-------------------------------*/
nav.navbar ul li.dropdown a:hover{
    background:#801515;
    color:#fff;
}

/*-------------------------------*/
/* 導覽列的下拉式項目滑鼠點擊時     */
/*-------------------------------*/
nav.navbar ul li.dropdown a:focus{
    background:#801515;
    color:#fff;
}


/*---------------------------*/
/* 下拉式選單背景色           */
/*---------------------------*/
ul.dropdown-menu{
    background:#FFaaaa;	
}

/*---------------------------*/
/* 下拉式選單文字色           */
/*---------------------------*/
nav.navbar ul.dropdown-menu li a{
    color:#000;	
}

/*---------------------------*/
/* 下拉式選單滑鼠移入時文字色  */
/*---------------------------*/
nav.navbar ul.dropdown-menu li a:hover{
    color:#ddd;	
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
                marginTop:-10
            }, 
            {
                duration:500,
                easing:'easeOutBounce'
            });
        }
    );	

    // 滑鼠移出	
    $('.thumbnail').mouseleave(function(){			
        $(this).stop().animate(
            {
                marginTop:0
            }, 
            {
                duration:50
            });
        }
    );		
});
```




##### 檔案名稱: index.html
```
<link rel="stylesheet" href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css"> 

...

<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>  
```
