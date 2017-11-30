# 第12課-(1) Bootstrap-客製導覽列


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
https://www.w3schools.com/html/default.asp
http://getbootstrap.com/
https://v4-alpha.getbootstrap.com/getting-started/introduction/
```


##### 執行結果:
![GitHub Logo](/imgs/results12-1.jpg)


### 檔案放置方式:
```
   | 
   |___<css>
   |     |___ style.css   (原檔為空檔)
   |
   |___<js>
   |     |___ scripts.js  (原檔為空檔)
   |
   |___ index.html  (修改)
```




### 檔案名稱: css/style.css
```css
/*==========================================*/
/* 客製化導覽列                              */
/*==========================================*/

/*---------------------------*/
/* 導覽列的商標標顏色          */
/*---------------------------*/
.navbar-custom .navbar-brand{
    color:#FFC;	
}

.navbar-custom .navbar-brand:hover{
    color:#FF0;	
}


/*---------------------------*/
/* 導覽列的背景顏色            */
/*---------------------------*/
.navbar-custom{
    background:#550000;	
}

/*---------------------------*/
/* 導覽列的文字顏色            */
/*---------------------------*/
.navbar-custom ul li a{
    color:#ccc;		
}


/*-----------------------------------*/
/* 導覽列的已被點擊過的項目文字顏色     */
/*-----------------------------------*/
.navbar-custom ul.navbar-nav li a:visited{
    color:#ccc;
}

.navbar-custom ul.dropdown-menu li a:visited{
    color:#000;	
}

/*---------------------------*/
/* 目前所在項目設定           */
/*---------------------------*/
.navbar-custom ul.navbar-nav li.active a{
    background:#000;
    color:#ccc;
}

/*---------------------------*/
/* 目前所在項目滑鼠移          */
/*---------------------------*/
.navbar-custom ul.navbar-nav li.active a:hover{
    background:#000;
    color:#fff;
}

/*---------------------------*/
/* 導覽列的項目滑鼠移入時      */
/*---------------------------*/
.navbar-custom ul.navbar-nav li a:hover{
    background:#801515;
    color:#fff;	
}

/*---------------------------*/
/* 導覽列的項目滑鼠點擊時      */
/*---------------------------*/
.navbar-custom ul.navbar-nav li a:focus{
    background:#801515;
    color:#fff;
}

/*------------------------------*/
/* 導覽列的下拉式項目滑鼠移入時    */
/*------------------------------*/
.navbar-custom ul.navbar-nav li.dropdown a:hover{
    background:#801515;
    color:#fff;
}

/*------------------------------*/
/* 導覽列的下拉式項目滑鼠點擊時    */
/*------------------------------*/
.navbar-custom ul.navbar-nav li.dropdown a:focus{
    background:#801515;
    color:#fff;
}

/*---------------------------*/
/* 下拉式選單背景色            */
/*---------------------------*/
.navbar-custom ul.dropdown-menu{
    background:#FFaaaa;	
}

/*---------------------------*/
/* 下拉式選單文字色            */
/*---------------------------*/
.navbar-custom ul.dropdown-menu li a{
    color:#000;	
}

/*------------------------------*/
/* 下拉式選單滑鼠移入時文字色      */
/*------------------------------*/
.navbar-custom ul.dropdown-menu li a:hover{
    color:#ddd;	
}
```



### 檔案名稱: js/scripts.js
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




### 檔案名稱: index.html
```
(加入css)
<link rel="stylesheet" href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css"> 



(修改, 加入navbar-custom)
將原內容
<nav class="navbar navbar-default" role="navigation">

改成:
<nav class="navbar navbar-default navbar-custom" role="navigation">



(加入js)
<script src="https://code.jquery.com/jquery-1.12.4.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>  
```
