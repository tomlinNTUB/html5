# 第11課 jQuery 外掛


## (3) timelineMe


##### 執行結果:
![GitHub Logo](/imgs/results11-4.jpg)


##### 下載網址
```
https://github.com/mickaelr/jquery-timelineMe
```



##### 引用官網外掛檔案
```
   |___<src>
         |___ jquery.timelineMe.css
         |___ jquery.timelineMe.js
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:
   
   |
   |___<images>
   |     |___ p01-small.jpg   (尺寸:250px*150px)
   |     
   |___<css>
   |     |___ jquery.timelineMe.css     (由官網複製)
   |     |___ my.jquery.timelineMe.css  (自行增加) 
   |
   |___<js>
   |     |___ jquery.timelineMe.js      (由官網複製)
   |     |___ my.jquery.timelineMe.js   (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.jquery.timelineMe.css
```css
@charset "utf-8";

/* 文字顏色 */
.timeline-me-container {
    color: #550000;
}


/* 大標題設定 */
.timeline-me-smallitem .timeline-me-label {
    font-size:25px;
    font-weight:600;
}


/* 線條顏色 */
.timeline-me-track:before {
    background: #801515;
}


/* 圓形外框及內部顏色 */
.timeline-me-milestone .timeline-me-label .timeline-me-picto {
    background-color: #d46a6a;  
    border: 3px solid #550000;
    z-index:15;
}

.timeline-me-smallitem .timeline-me-label .timeline-me-picto {
    background-color: #d46a6a;  
    border: 3px solid #550000;
    z-index:15;
}

.timeline-me-bigitem .timeline-me-label .timeline-me-picto {
    background-color: #d46a6a;  
    border: 3px solid #550000;
    z-index:15;	
}


/* 內容背景顏色 */
.timeline-me-shortcontent,
.timeline-me-fullcontent {
    background-color: #ffaaaa;
}


/* 內容的詳細功能 */
.timeline-me-showmore {
    margin-top:20px;
    font-size:15px;
    color:#fff;
    cursor:pointer;
}


/* 內容的摘要功能 */
.timeline-me-showless {
    margin-top:20px;
    font-size:15px;
    color:#fff;
    cursor:pointer;	
}
```



##### 檔案名稱: js/my.jquery.timelineMe.js
```js
$('#timeline-container-force-position').timelineMe({
    items: [
    {
        type: 'smallItem',
        label: '真正的美，作假不得',
        shortContent: '幾年來，幾乎所有的竹科企業我都去過了，和企業的人有所接觸後...',
        fullContent: '幾年來，幾乎所有的竹科企業我都去過了，和企業的人有所接觸後，我才知道我過去有「知識偏執」的狀況，但我並沒有真正認識30歲上下的職場工作人員。竹科有一家上市公司的員工平均年齡是31.8歲，他們都是最優秀大學畢業的菁英。',
        showMore: '詳細',
        showLess: '摘要'
    },
    {
        type: 'smallItem',
        label: '找回人與人之間的感覺',
        shortContent: '<img src="images/p01-small.jpg" style="width:100%">我現在不問工程師有沒有去聽音樂、看展覽，反而是問他們...',
        fullContent: '我現在不問工程師有沒有去聽音樂、看展覽，反而是問他們：「你們在這裡工作5年了，有沒有人可以告訴我公司門口那一排是什麼樹？」但很少人能夠回答的出來。',
        showMore: '詳細',
        showLess: '摘要'
    },
    {
        type: 'smallItem',
        label: '週休二日，回來做自己',
        shortContent: '現在台灣過週休二日，好像非要全家去吃一個餐廳、到哪裡...',
        fullContent: '現在台灣過週休二日，好像非要全家去吃一個餐廳、到哪裡去看薰衣草、喝咖啡，全部整套，然後全部的人塞車塞到一肚子氣。我們對休閒的定義是滿僵化的，好像一定要別人服務我們才算是休閒。',
        showMore: '詳細',
        showLess: '摘要',
        forcePosition: 'right'
    },
    {
        type: 'smallItem',
        label: '過得像個人，才能看到美',
        shortContent: '蔣勳曾說自己是用佈道的心情傳播對美的感動，現在他已經可說是美的宗教家...',
        fullContent: '蔣勳曾說自己是用佈道的心情傳播對美的感動，現在他已經可說是美的宗教家。近幾年來，蔣勳走遍竹科與各地演講，到場的聽眾們彷彿都期待受到「開釋」，除了在席間對於充滿抑揚頓挫的感性分析頻頻點頭，發問的許多也都是已超乎美學的人生之問。',
        showMore: '詳細',
        showLess: '摘要',
        forcePosition: 'left'
    }]
});
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link href="css/jquery.timelineMe.css" rel="stylesheet" type="text/css" />
<link href="css/my.jquery.timelineMe.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/jquery.timelineMe.js"></script>
<script src="js/my.jquery.timelineMe.js"></script>  
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- timelineMe 測試  -->
<!--~~~~~~~~~~~~~~~~~~-->
<p>
    <div id="timeline-container-force-position" type="text"></div>
</p>
<!--~~~~~~~~~~~~~~~~~~--> 
```
