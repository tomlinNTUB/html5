#第03課 div區塊安排



## 測試網頁(1)

檔案放置方式如下:
```
index.html
   | 
   |___<css>
   |     |___ main.css
   |	 
   |___<js>
         |___ main.js    
```

檔案名稱: index.html 
```
<!doctype html>
<html>
<meta charset="utf-8">
<title>測試網頁</title>
<!-- 加入一個main.css -->
<link href="css/main.css" rel="stylesheet" type="text/css" />
</head>
<body>

<div class="container">
	<div class="header">
    	測試標題
    </div>
    
    <div class="content">
    	Python是當今最熱門的程式語言之一，它不僅已被Google、YouTube、BBC及Spotify等公司所採用，並且也是Raspberry Pi單板電腦所支援的主要語言。學習Python是步入程式設計領域的絕佳途徑，而透過本書更能夠確保學習過程是簡單且富含樂趣的。<p/>

		未曾有程式設計經驗？沒有問題！本書就是你的救星——帶領你走過10項程式設計專案，透過清楚、簡單的指示，使你一方面可以瞭解程式設計的基礎概念，而另一方面也逐步熟悉Python程式語言的功能特質。隨著基礎逐漸累積後，新技巧也會持續加入，讓你能汲取到更多知識。不僅如此，每一章都有線上影片教學，讓每項專案的實際過程及成果都是眼見為憑。<p/>

		本書的資源網站：www.wiley.com/go/adventuresinpython，提供了線上影片教學，及其他有用的資訊，幫助你在Python之路上走得更加輕鬆。學會Python語言後，你便擁有紮實的基礎，可以進一步學習其他的程式語言，例如：C++、Objective-C及Java等。事不宜遲，開始學習你的第一門程式語言吧！<p/>
    </div>
    
    <div class="footer">
    	版權所有 &copy;2016, NTUB IMD.
    </div>
</div>

</body>
</html>
```

檔案名稱: css/main.css
```
@charset "utf-8";

html, body{
	font-size:16px;
	background:#000;
}

div.container{
    width:800px;
	border:1px solid #666;	
	margin:10px auto 10px auto;
	box-sizing:border-box;
}

div.header{
	height:150px;
	background:#CCC;
	font-size:40px;
	text-align:center;
	line-height:150px;
	letter-spacing:18px;
}

div.content{
	padding:20px 15px 20px 15px;
	background:#FFF;
	line-height:32px;	
	text-align:justify;	
}

div.footer{
	height:100px;
	line-height:100px;
	background:#CCC;
	font-size:13px;
	text-align:center;
	letter-spacing:5px;
}
```




## 測試網頁(2)

檔案放置方式如下:
```
index.html
   | 
   |___<css>
   |     |___ main.css
   |	 
   |___<js>
         |___ main.js    
```

檔案名稱: index.html 
```
<!doctype html>
<html>
<meta charset="utf-8">
<title>測試網頁</title>
<link href="css/main.css" rel="stylesheet" type="text/css" />
</head>
<body>

<div class="container">
	<div class="header">
    	測試標題
    </div>
    
    <div class="navbar">
        導覽列
    </div>
    
    <div class="content">
    	Python是當今最熱門的程式語言之一，它不僅已被Google、YouTube、BBC及Spotify等公司所採用，並且也是Raspberry Pi單板電腦所支援的主要語言。學習Python是步入程式設計領域的絕佳途徑，而透過本書更能夠確保學習過程是簡單且富含樂趣的。<p/>

		未曾有程式設計經驗？沒有問題！本書就是你的救星——帶領你走過10項程式設計專案，透過清楚、簡單的指示，使你一方面可以瞭解程式設計的基礎概念，而另一方面也逐步熟悉Python程式語言的功能特質。隨著基礎逐漸累積後，新技巧也會持續加入，讓你能汲取到更多知識。不僅如此，每一章都有線上影片教學，讓每項專案的實際過程及成果都是眼見為憑。<p/>

		本書的資源網站：www.wiley.com/go/adventuresinpython，提供了線上影片教學，及其他有用的資訊，幫助你在Python之路上走得更加輕鬆。學會Python語言後，你便擁有紮實的基礎，可以進一步學習其他的程式語言，例如：C++、Objective-C及Java等。事不宜遲，開始學習你的第一門程式語言吧！<p/>
    </div>
    
    <div class="footer">
    	版權所有 &copy;2016, NTUB IMD.
    </div>
</div>

</body>
</html>
```

檔案名稱: css/main.css
```
@charset "utf-8";

html, body{
	font-size:16px;
	background:#000;
}

div.container{
    width:800px;
	border:1px solid #666;	
	margin:10px auto 10px auto;
	box-sizing:border-box;
}

div.header{
	height:150px;
	background:#CCC;
	font-size:40px;
	text-align:center;
	line-height:150px;
	letter-spacing:18px;
}

div.navbar{
	height:50px;
	background:#AAA;
	font-size:16px;
	text-align:center;
	line-height:50px;
	letter-spacing:12px;
}

div.content{
	padding:20px 15px 20px 15px;
	background:#FFF;
	line-height:32px;	
	text-align:justify;	
}

div.footer{
	height:100px;
	line-height:100px;
	background:#CCC;
	font-size:13px;
	text-align:center;
	letter-spacing:5px;
}
```



## 測試網頁(3)

檔案放置方式如下:
```
   | 
   |___<css>
   |     |___ main.css
   |	 
   |___<js>
   |     |___ main.js 
   |	 
   |___<img>
   |     |___ header.jpg (800px*600px) 
   |
   |___index.html		 
```

檔案名稱: index.html 
```
<!doctype html>
<html>
<meta charset="utf-8">
<title>測試網頁</title>
<link href="css/main.css" rel="stylesheet" type="text/css" />
</head>
<body>

<div class="container">
	<div class="header">    	
    </div>
    
    <div class="content">
    	<div class="left">
        	每個軟體開發者與IT專家都知道高效除錯的重要性。除錯通常佔據開發者大部分的時間，而掌握技巧需要一輩子的投入。作者Diomidis Spinellis在這本書中提供了系統化分類、解析說明、最有效的除錯方法、策略、技巧以及工具，協助有經驗的程式設計師加速掌握技能。
        </div>
        
        <div class="right">
    		Python是當今最熱門的程式語言之一，它不僅已被Google、YouTube、BBC及Spotify等公司所採用，並且也是Raspberry Pi單板電腦所支援的主要語言。學習Python是步入程式設計領域的絕佳途徑，而透過本書更能夠確保學習過程是簡單且富含樂趣的。<p/>

			未曾有程式設計經驗？沒有問題！本書就是你的救星——帶領你走過10項程式設計專案，透過清楚、簡單的指示，使你一方面可以瞭解程式設計的基礎概念，而另一方面也逐步熟悉Python程式語言的功能特質。隨著基礎逐漸累積後，新技巧也會持續加入，讓你能汲取到更多知識。不僅如此，每一章都有線上影片教學，讓每項專案的實際過程及成果都是眼見為憑。<p/>

			本書的資源網站：www.wiley.com/go/adventuresinpython，提供了線上影片教學，及其他有用的資訊，幫助你在Python之路上走得更加輕鬆。學會Python語言後，你便擁有紮實的基礎，可以進一步學習其他的程式語言，例如：C++、Objective-C及Java等。事不宜遲，開始學習你的第一門程式語言吧！<p/>
        </div>         
    </div>
    
    <div class="footer">
    	版權所有 &copy;2016, NTUB IMD.
    </div>
</div>

</body>
</html>
```

檔案名稱: css/main.css
```
@charset "utf-8";

html, body{
	font-size:16px;	
}

div.container{
    width:800px;
	border:1px solid #666;	
	margin:10px auto 10px auto;
	box-sizing:content-box;
	background:#FFC;
}

div.header{
	height:150px;
	background:url(../img/header.jpg);
}

div.content{
	text-align:justify;	
}

div.content div.left{
	width:200px;
	box-sizing:border-box;
	padding:20px 10px;
	float:left;
	line-height:32px;
}

div.content div.right{
	width:600px;
	box-sizing:border-box;
	float:left;
	padding:20px 15px 20px 15px;
	background:#FFF;
	line-height:32px;
}

div.footer{
	clear:both;
	height:100px;
	line-height:100px;
	background:#CCC;
	font-size:13px;
	text-align:center;
	letter-spacing:5px;
}
```





## 測試網頁(4)
檔案放置方式如下:
```
   | 
   |___<css>
   |     |___ main.css
   |	 
   |___<js>
   |     |___ main.js 
   |	 
   |___<img>
   |     |___ header.jpg (800px*600px) 
   |
   |___index.html		 
```
<p>

檔案名稱: index.html 
```
<!doctype html>
<html>
<meta charset="utf-8">
<title>測試網頁</title>
<link href="css/main.css" rel="stylesheet" type="text/css" />
</head>
<body>

<div class="container">
	<div class="header">    	
    </div>
    
    <div class="content">
    	<div class="left">
        	每個軟體開發者與IT專家都知道高效除錯的重要性。除錯通常佔據開發者大部分的時間，而掌握技巧需要一輩子的投入。作者Diomidis Spinellis在這本書中提供了系統化分類、解析說明、最有效的除錯方法、策略、技巧以及工具，協助有經驗的程式設計師加速掌握技能。
        </div>
        
        <div class="right">
        	<div class="navbar">
            	導覽列
            </div>
            
            <div class="context">
	    		Python是當今最熱門的程式語言之一，它不僅已被Google、YouTube、BBC及Spotify等公司所採用，並且也是Raspberry Pi單板電腦所支援的主要語言。學習Python是步入程式設計領域的絕佳途徑，而透過本書更能夠確保學習過程是簡單且富含樂趣的。<p/>

				未曾有程式設計經驗？沒有問題！本書就是你的救星——帶領你走過10項程式設計專案，透過清楚、簡單的指示，使你一方面可以瞭解程式設計的基礎概念，而另一方面也逐步熟悉Python程式語言的功能特質。隨著基礎逐漸累積後，新技巧也會持續加入，讓你能汲取到更多知識。不僅如此，每一章都有線上影片教學，讓每項專案的實際過程及成果都是眼見為憑。<p/>

				本書的資源網站：www.wiley.com/go/adventuresinpython，提供了線上影片教學，及其他有用的資訊，幫助你在Python之路上走得更加輕鬆。學會Python語言後，你便擁有紮實的基礎，可以進一步學習其他的程式語言，例如：C++、Objective-C及Java等。事不宜遲，開始學習你的第一門程式語言吧！<p/>
        	</div>        
        </div>         
    </div>
    
    <div class="footer">
    	版權所有 &copy;2016, NTUB IMD.
    </div>
</div>

</body>
</html>
```

檔案名稱: css/main.css
```
@charset "utf-8";

html, body{
	font-size:16px;	
}

div.container{
    width:800px;
	border:1px solid #666;	
	margin:10px auto 10px auto;
	box-sizing:content-box;
	background:#FFC;
}

div.header{
	height:150px;
	background:url(../img/header.jpg);
}

div.content{
	text-align:justify;	
}

div.content div.left{
	width:200px;
	box-sizing:border-box;
	padding:20px 10px;
	float:left;
	line-height:32px;
}

div.content div.right{
	width:600px;
	box-sizing:border-box;
	float:left;	
	background:#FFF;
	line-height:32px;
}

div.content div.right div.navbar{
	height:50px;
	background:#AAA;
	font-size:16px;
	text-align:center;
	line-height:50px;
	letter-spacing:12px;
}

div.content div.right div.context{
	font-size:16px;
	padding: 20px 10px;
}

div.footer{
	clear:both;
	height:100px;
	line-height:100px;
	background:#CCC;
	font-size:13px;
	text-align:center;
	letter-spacing:5px;
}
```