# 13-2 Chart.js-圓餅圖

### 練習重點
```
使用Chart.js, 由輸入資料產生圖表.
```

### 執行結果:
![GitHub Logo](/imgs/results13-2.jpg)


### 檔案放置方式 (以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |
   |__ <js>
         |__ Chart.bundle.js     (在<下載>資料夾中)
         |__ my.Chart.bundle.js  (自行增加) 
```


### (1) my.Chart.bundle.js

``` js
var ctx = document.getElementById("myChart").getContext('2d');
var myChart = new Chart(ctx, {
    type: 'pie',
    data: {
        labels: ["星期一", "星期二", "星期三", "星期四", "星期五", "星期六"],
        datasets: [{            
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132)',
                'rgba(54, 162, 235)',
                'rgba(255, 206, 86)',
                'rgba(75, 192, 192)',
                'rgba(153, 102, 255)',
                'rgba(255, 159, 64)'
            ],
            borderWidth: 1
        }]
    },
    options: {}
});
```


### (2) index.html (引用外掛)  
``` html
.
.
.
(加入js)
<script src="js/Chart.bundle.js"></script>  
<script src="js/my.Chart.bundle.js"></script>   
.
.
```

### (3) index.html (增加顯示區域)  
``` html
<!-- 圖表位置 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->		
<canvas id="myChart" width="100" height="50">
</canvas>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
```
