# 13-1 使用Chart.js-長條圖

### 練習重點
```
使用Chart.js, 由輸入資料產生圖表.
```

### 執行結果:
![GitHub Logo](/imgs/results13-1.jpg)


### 外掛網址
```
在<下載>中, Chart.bundle.js
```

### 檔案放置方式:
```
**以11-3網頁為基礎, 增加以下:

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
    type: 'bar',
    data: {
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
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
