# 第13課-(1) Bootstrap-客製導覽列


##### Bookstrap:
```
http://layoutit.com   
```


##### Bookstrap 版型:
```
https://startbootstrap.com/
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
   |___ index.html  (修改)
```




### 檔案名稱: css/style.css
```css
/*==========================================*/
/* 設定選用顏色                               */
/*==========================================*/
:root{
    --nav-1:#FFAAAA;
    --nav-2:#D46A6A;
    --nav-3:#AA3939;
    --nav-4:#801515;
    --nav-5:#550000;	
}


/*==========================================*/
/* 客製化導覽列                              */
/*==========================================*/
/*---------------------------*/
/* 導覽列的背景顏色             */
/*---------------------------*/
nav.navbar{
    background:var(--nav-5);	
}


/*---------------------------*/
/* 導覽列收合的menu            */
/*---------------------------*/
.navbar .navbar-toggler{
    background:var(--nav-3);	
    border:none;
    outline:0 none;
}


/*---------------------------*/
/* 導覽列的商標                */
/*---------------------------*/
nav.navbar a.navbar-brand{
    color:var(--nav-1);
    font-weight:800;
}

nav.navbar a.navbar-brand:hover{
    color:#fff;
}


/*-------------------------*/
/* 導覽列的項目              */
/*-------------------------*/
nav.navbar ul.navbar-nav li.nav-item a.nav-link{   
    color:var(--nav-2);
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:hover{   
    color:#fff !important;
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:focus{
    color:var(--nav-2);
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:visited{
    color:var(--nav-2);
}


/*---------------------------*/
/* 目前所在項目設定           */
/*---------------------------*/
nav.navbar ul.navbar-nav li.nav-item.active a.nav-link{
    color:var(--nav-1);
}

nav.navbar ul.navbar-nav li.nav-item.active a.nav-link:hover{
    color:#fff;
}


/*------------------------------*/
/* 導覽列的下拉式項目              */
/*------------------------------*/
nav.navbar ul.navbar-nav li.dropdown a.nav-link{
    color:var(--nav-2);
}

nav.navbar ul.navbar-nav li.dropdown a.nav-link:hover{
    color:#fff;
}


/*------------------------------*/
/* 下拉式選單                     */
/*------------------------------*/
.dropdown-menu{
    background:var(--nav-2);	
}

.dropdown-menu a{
    color:var(--nav-5);	
}

.dropdown-menu a:hover{
    background:var(--nav-1);
    color:#fff;
}


/*------------------------------*/
/* 輸入項目及按鈕                  */
/*------------------------------*/
input[type="text"]:focus{   
    border-color: rgba(255, 255, 255, 0.8);
    box-shadow: none;
    outline: 0 none;
}

.navbar form button,
.navbar form button:visited,
.navbar form button:focus{
    background:var(--nav-3);
    color:#fff;
    border:none;
}

.navbar form button:hover{
    background:var(--nav-2);
    color:#000;
}
```

