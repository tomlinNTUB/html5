# 12-2 使用jQuery外掛-t.js

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-2.jpg)


### 外掛網址
```
https://github.com/mntn-dev/t.js
```

### 引用官網外掛檔案
```
   |___ t.js  
   |   
   |___ demo.html (參考用法)  
```


### 檔案放置方式(以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |     
   |__ <css>
   |     |__ my.t.css  (自行增加) 
   |
   |__ <js>
         |__ t.js     (由官網複製)     
         |__ my.t.js  (自行增加)       
```


### (1) my.t.css
``` css
@charset "utf-8";

div#t{	
    width:100%;	
    height:180px;
    box-sizing:border-box;
    background:#000;
    padding:20px;
    text-align:left;
    color:#0f0;
    font-size:16px;
    line-height:25px;	
}
```

### (2) my.t.js
``` js
var fin=!1;

function foo(){
    $('mark').eq(0).css({background:'magenta'});
}


$(function(){
    $('#t').t({
        speed:60,
        speed_vary:true,
        mistype:15,
		
        typing:function(elem,chars_total,chars_left,_char){
            if(_char=='*')foo();
        },
 
        fin:function(){
            if(fin==!1){
                fin=!!1; //avoids triggering after 'add' cmd
                window.setTimeout(function(){$('#t').t('add','一起去看小葉欖仁? ');},2e4);
                window.setInterval(function(){$('#t').find('.t-caret').toggle();},5e2);
            }
        }
    });
});
```

### (3) index.html (引用外掛)  
``` html
.
.
(加入css)
<link href="css/my.t.css" rel="stylesheet" />
.
.
.
.
(加入js)
<script src="js/t.js"></script> 
<script src="js/my.t.js"></script> 
.
.
```

### (4) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- t.js 測試        -->
<!--~~~~~~~~~~~~~~~~~~-->
<p>
    <div id="t">                
        我現在不問工程師有沒有去聽音樂、看展覽，反而是問他們：「<del>人人火人日弓大土</del>你們在這裡工作5年了，有沒有人可以告訴我公司門口那一排是什麼<del>木土口廿戈</del>樹?」但很少人能夠回答的出來。<br/>事實上，他們公司門口那排<del style="color:red;border-bottom:1px dashed yellow;">小葉懶人<ins>1</ins></del>小葉欖仁的葉子漂亮得不得了，綠色會在陽光裡發亮。<br/><br/>                                               
        那裡有<del>小葉懶人</del>小葉欖仁? 
    </div>       
</p>
<!--~~~~~~~~~~~~~~~~~~--> 
```
