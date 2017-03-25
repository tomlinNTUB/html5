# 第11課 jQuery 外掛


## (3) bookblock


##### 執行結果:
![GitHub Logo](/imgs/results11-3.jpg)


##### 下載網址
```
https://github.com/codrops/BookBlock
```



##### 引用官網外掛檔案
```
   |___<dist>
         |___ <css>
         |      |__ bookblock.css
         |      |__ demo1.css 
         |      
         |___ <js>
         |      |__ jquery.bookblock.js
         |      |__ jquerypp.custom.js      
         |      |__ modernizer.custom.js          
         |
         |___ <fonts> (資料夾及其中檔案)
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:
   
   |
   |___<fonts>  (由官網複製)
   | 
   |___<images>
   |     |___ p01-book.jpg   (尺寸:600px*400px)
   |     |___ p02-book.jpg   (尺寸:600px*400px)
   |     |___ p03-book.jpg   (尺寸:600px*400px)
   |     |___ p04-book.jpg   (尺寸:600px*400px)   
   |     
   |___<css>
   |     |___ bookblock.css     (由官網複製)
   |     |___ demo1.css         (由官網複製)   
   |     |___ my.bookblock.css  (自行增加) 
   |
   |___<js>
   |     |___ jquery.bookblock.js    (由官網複製)
   |     |___ jquerypp.custom.js     (由官網複製)
   |     |___ modernizer.custom.js   (由官網複製)    
   |     |___ my.bookblock.js        (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.bookblock.css
```css
@charset "utf-8";

.bb-bookblock {	
    width: 600px;
    height: 400px;
    z-index: 15;
}

.bb-custom-wrapper {
    width: 600px;
}

.bb-custom-wrapper nav a {
    background:#1F2FC2;
    color: #ff0;
}
```



##### 檔案名稱: js/my.bookblock.js
```js
var Page = (function() {
    var config = {
        $bookBlock : $( '#bb-bookblock' ),
        $navNext : $( '#bb-nav-next' ),
        $navPrev : $( '#bb-nav-prev' ),
        $navFirst : $( '#bb-nav-first' ),
        $navLast : $( '#bb-nav-last' )
    },
    
    init = function() {
        config.$bookBlock.bookblock( {
            speed : 800,
            shadowSides : 0.8,
            shadowFlip : 0.7
        });
        initEvents();
    },
		
    initEvents = function() {			
        var $slides = config.$bookBlock.children();

        // add navigation events
        config.$navNext.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'next' );
            return false;
        });

        config.$navPrev.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'prev' );
            return false;
        });

        config.$navFirst.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'first' );
            return false;
        });

        config.$navLast.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'last' );
            return false;
        });
			
        // add swipe events
        $slides.on( {
            'swipeleft' : function( event ) {
                config.$bookBlock.bookblock( 'next' );
                return false;
            },
            'swiperight' : function( event ) {
                config.$bookBlock.bookblock( 'prev' );
                return false;
            }
        });

        // add keyboard events
        $( document ).keydown( function(e) {
            var keyCode = e.keyCode || e.which;
            var arrow = {
                left : 37,
                up : 38,
                right : 39,
                down : 40
            };

            switch (keyCode) {
                case arrow.left:
                    config.$bookBlock.bookblock( 'prev' );
                    break;
                case arrow.right:
                    config.$bookBlock.bookblock( 'next' );
                    break;
            }
        });
    };
    return { init : init };
})();


$(function(){
    Page.init();
});
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link href="css/bookblock.css" rel="stylesheet" type="text/css" />
<link href="css/demo1.css" rel="stylesheet" type="text/css" />
<link href="css/my.bookblock.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/modernizr.custom.js"></script>    
<script src="js/jquerypp.custom.js"></script>     
<script src="js/jquery.bookblock.js"></script>  
<script src="js/my.bookblock.js"></script> 
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!--~~~~~~~~~~~~~~~~~-->
<!-- bookblock 測試  -->
<!--~~~~~~~~~~~~~~~~~-->
<p>    
    <div class="main clearfix">
        <div class="bb-custom-wrapper">                        
            <div id="bb-bookblock" class="bb-bookblock">
                <div class="bb-item">
                    <a href="#"><img src="images/p01-book.jpg" alt="p01"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="images/p02-book.jpg" alt="p02"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="images/p03-book.jpg" alt="p03"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="images/p04-book.jpg" alt="p04"/></a>
                </div>
            </div>
            <nav>
                <a id="bb-nav-first" href="#" class="bb-custom-icon bb-custom-icon-first">First page</a>
                <a id="bb-nav-prev" href="#" class="bb-custom-icon bb-custom-icon-arrow-left">Previous</a>
                <a id="bb-nav-next" href="#" class="bb-custom-icon bb-custom-icon-arrow-right">Next</a>
                <a id="bb-nav-last" href="#" class="bb-custom-icon bb-custom-icon-last">Last page</a>
            </nav>
        </div>
    </div>
</p>
<!--~~~~~~~~~~~~~~~~~--> 
```
