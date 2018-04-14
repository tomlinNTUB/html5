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
	--primary-1:#FFAAAA;
	--primary-2:#D46A6A;
	--primary-3:#AA3939;
	--primary-4:#801515;
	--primary-5:#550000;	
}


/*==========================================*/
/* 客製化導覽列                              */
/*==========================================*/

/*---------------------------*/
/* 導覽列的背景顏色            */
/*---------------------------*/
nav.navbar{
    background:var(--primary-5);	
}



/*---------------------------*/
/* 導覽列的商標                */
/*---------------------------*/
nav.navbar a.navbar-brand{
    color:var(--primary-1);
	font-weight:800;
}

nav.navbar a.navbar-brand:hover{
    color:#fff;
}


/*-------------------------*/
/* 導覽列的項目              */
/*-------------------------*/
nav.navbar ul.navbar-nav li.nav-item a.nav-link{   
    color:var(--primary-2);
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:hover{   
    color:#fff !important;
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:focus{
    color:var(--primary-2);
}

nav.navbar ul.navbar-nav li.nav-item a.nav-link:visited{
    color:var(--primary-2);
}



/*---------------------------*/
/* 目前所在項目設定           */
/*---------------------------*/
nav.navbar ul.navbar-nav li.nav-item.active a.nav-link{
    color:var(--primary-1);
}

nav.navbar ul.navbar-nav li.nav-item.active a.nav-link:hover{
    color:#fff;
}


/*------------------------------*/
/* 導覽列的下拉式項目              */
/*------------------------------*/
nav.navbar ul.navbar-nav li.dropdown a.nav-link{
    color:var(--primary-2);
}

nav.navbar ul.navbar-nav li.dropdown a.nav-link:hover{
    color:#fff;
}


/*------------------------------*/
/* 下拉式選單                     */
/*------------------------------*/
.dropdown-menu{
	background:var(--primary-2);	
}

.dropdown-menu a{
	color:var(--primary-5);	
}

.dropdown-menu a:hover{
	background:var(--primary-1);
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
	background:var(--primary-3);
	color:#fff;
	border:none;
}

.navbar form button:hover{
	background:var(--primary-2);
	color:#000;
}
```

