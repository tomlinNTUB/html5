# 13-3 使用Chart.js-折線圖

### 練習重點
```
使用Chart.js, 由輸入資料產生圖表.
```

### 執行結果:
![GitHub Logo](/imgs/results13-3.jpg)


### 檔案放置方式(以11-3範例為基礎, 增修以下):
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
    type: 'line',
    data: {
        labels: ["102年", "103年", "104年", "105年", "106年"],
        datasets: [{
            label: '新生人口(千人)',
            data: [183.7, 199.2, 201.5, 196.8, 183.4],
            fill: false,
            backgroundColor: 'rgba(212, 106, 106, 1)',
            borderColor: 'rgba(212, 106, 106, 1)'
        }, 
        {
            label: '20歲人口(千人)',
            data: [325.1, 321.4, 323.4, 321.4, 322.4],
            fill: false,
            backgroundColor: 'rgba(128, 21, 21, 1)',			
            borderColor: 'rgba(128, 21, 21, 1)'
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero:true
                }
            }]
        }
    }
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
