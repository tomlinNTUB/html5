# 11-3 導覽列點擊收合並旋轉logo的板型

### 練習重點
```
使用固定定位方式設計元件位置, 增加使用jQueryUI, jQueryRotate.
```

### 執行結果:
![GitHub Logo](/imgs/results11-3.jpg)


### 檔案放置方式:
```
|__ index.html  
|   
|__ <css>
|     |__ main.css 
|
|__ <js>
|     |__ main.js 
|     |__ jQueryRotate.js   (下載:https://raw.githubusercontent.com/wilq32/jqueryrotate/master/jQueryRotate.js)
|
|__ <imgs>
      |__ logo.jpg    (80像素*80像素)  
```


### (1) index.html 
```html
<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>測試網頁</title>
<!-- 連結main.css及思源中文 -->
<link href="css/main.css" rel="stylesheet" type="text/css" />
<link rel="stylesheet" href="http://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<link href="https://fonts.googleapis.com/css?family=Noto+Sans+TC" rel="stylesheet">
<!------------------------->
</head>
   
<body>
    <!--~~~~~~~~~~~~~~~~~-->
    <div class="header">
        <!--logo圖片-->
        <img src="imgs/logo.jpg" class="logo">
    
        <!--導覽列-->        
        <div class="navbar">
            <ul>
                <a href="#"><li>生活</li></a>
                <a href="#"><li>旅遊</li></a>
                <a href="#"><li>食物</li></a>
                <a href="#"><li>文化</li></a>
            </ul>
        </div>   
    </div>    
    <!--~~~~~~~~~~~~~~~~~-->        

    
    <!--**************************-->        
    <div class="container">    
        <!--~~~~~~~~~~~~~~~~~--> 
        <div class="content">
            <h2>蔣勳：過得像個人，才能看到美</h2>

            <p>蔣勳曾說自己是用佈道的心情傳播對美的感動，現在他已經可說是美的宗教家。近幾年來，蔣勳走遍竹科與各地演講，到場的聽眾們彷彿都期待受到「開釋」，除了在席間對於充滿抑揚頓挫的感性分析頻頻點頭，發問的許多也都是已超乎美學的人生之問。事實上，這幾年來，蔣勳談的美，也有很大的變化。他過去比較偏向幫助大家賞析藝術之美，但他在與聽眾愈來愈多的互動中發現，許多上班族的餘暇時間已極度有限了，刻意附庸風雅地去欣賞音樂會、畫展已經沒有必要，重拾與周遭人的感情，重新找回「像個人樣」的生活方式，才能對美真正有所體會。本期美學學院專訪蔣勳，分享上班族也可以找回的生活之美。</p>


            <h2>真正的美，作假不得 </h2>

            <p>幾年來，幾乎所有的竹科企業我都去過了，和企業的人有所接觸後，我才知道我過去有「知識偏執」的狀況，但我並沒有真正認識30歲上下的職場工作人員。竹科有一家上市公司的員工平均年齡是31.8歲，他們都是最優秀大學畢業的菁英。 在開始工作的前10年，是人生很重要的階段，但他們卻通常是11點以後才下班。要戀愛，可能沒有時間戀愛；要買房子，就用世俗的固定模式買房子，找一個大家認為有名的設計師；要結婚，但用很草率的方式結婚。我知道很多工程師經由輔導去娶烏克蘭新娘，他們可能連戀愛的時間、耐心都沒有。 我原來希望的藝術是能恢復人的品味和人的感覺，但他們接觸了這些東西卻沒有感覺，像有些企業會固定舉辦一些音樂會，但他們卻沒有辦法進入那個世界。所以我現在希望向大家說的是「人的原點」，當我們失去了人的原點，談所有的美都是假的。</p>

            <p>我有一個朋友，住在信義路上億元的豪宅，找了日本最有名的設計師來裝潢，但有一次我去他家，發現他住了2年，可是廚房裡所有進口廚具的膠膜都沒撕掉。他的房子只是一個showroom。可是家不是showroom，家是讓你可以放鬆自在、活得像人的地方，家是因為住在裡面的人有自己的渴望、自己的感覺，才會有自己的風格。如果主人對這個家沒有意見、對自己的生活沒有看法，只想告訴別人買的是義大利最貴的床，那只是作假給別人看。你可以在家裡放很多明式家具，很美；你喜歡家裡很空，也很美，但這裡面的難度是你到底要什麼，如果你不知道，你找再有名的建築師設計都是假的，你怎麼樣回來做自己，才是最難的功課。</p> 

            <p>我自己是住在淡水河邊，當時會在那裡買房子，是因為覺得淡水河口好漂亮，但是我房子的建商卻不知道善用那裡的美景，窗戶建得很小，我在房間裡就覺得好難過。所以我找了一個學建築的學生，他幫我開了12個窗，而且全部是往外推的推窗，比拉窗更有靠近河邊的感覺，還架出一個小陽台，所以我可以坐在小欄杆上看河，和淡水河只有2公尺的距離。我也不喜歡隔間，所以設計師幫我用高度界定出3個不同的區域。我家最高的地方是客廳，朋友來的時候坐在最高的地方喝茶；次高的地方是書房，我在那邊看書；再次高的地方是我的餐廳。我覺得這是我的房子、我的家，我是主人，我知道我要什麼。在穿著上，我喜歡純棉、純麻，因為我覺得它們很溫暖，材料本身有觸覺上的記憶，在排汗、吸汗的過程也非常舒服。加上我喜歡爬山、喜歡躺在草地上、喜歡在海灘捲起褲腳踩水，我喜歡這樣的生活，所以我就有我服裝的特徵，名牌就不適合我，因為我喜歡自在。 </p>


            <h2>找回人與人之間的感覺 </h2>

            <p>我現在不問工程師有沒有去聽音樂、看展覽，反而是問他們：「你們在這裡工作5年了，有沒有人可以告訴我公司門口那一排是什麼樹？」但很少人能夠回答的出來。事實上，他們公司門口那排小葉欖仁的葉子漂亮得不得了，綠色會在陽光裡發亮。後來我再去，就有一個員工和我說，「謝謝你告訴我這件事，我現在下班時會先看看小葉欖仁再回家，所以比較不會和太太吵架了。」他也問我現在5歲的女兒將來該學鋼琴、還是小提琴，但我建議11點下班的他多抱抱女兒，比較重要。 因為所有的藝術講的都是人的故事，一個孩子如果不記得父親的體溫，她將來看畫、聽音樂都沒有感動。如果沒有人的記憶，所有藝術對她而言都只是賣弄而已。</p>

            <p>我們從年輕開始，就因為工作忙碌，忽略了人與人的感覺，但工作忙碌之餘，你還是一個人，你必須每分每秒提醒自己回來做人的部份。你看到了美，才會覺得這個世界是值得活下去的。如果你看到的只是品牌、只是假的美，你不見得快樂，那反而可能會是你憂鬱症的原因。找回美的感覺其實很簡單，去觸摸一片葉子，去聞一下在很熱很熱的夏天、下完午後暴雨的氣味，那是都我們有記憶的感覺，那都會引發我們的感觸和感動。 </p>

            <p>現在美常常成為新的知識、新的壓力，博士可能毫無美感，但一個不識字的美濃農夫卻可以很美，他看得到月光的美、看得到稻浪翻飛的美。美是最大的財富，它不會因為你的學歷而不同，而是因為你人的部份完不完整而不同。 </p>


            <h2>週休二日，回來做自己 </h2>

            <p>現在台灣過週休二日，好像非要全家去吃一個餐廳、到哪裡去看薰衣草、喝咖啡，全部整套，然後全部的人塞車塞到一肚子氣。我們對休閒的定義是滿僵化的，好像一定要別人服務我們才算是休閒。我自己假日的時候喜歡自己一個人做4菜1湯，因為我覺得做菜好快樂。我也很喜歡在週休二日洗我自己最喜歡的純棉的、純麻的襯衫，絕不丟給洗衣機，因為我覺得觸感好極了。看到它們晾在陽光裡、在風裡飄，白的好漂亮，我的週休二日就很快樂，因為我回來做自己。 </p>

            <p>在7、8月，民生東路六段有全台北最漂亮的大花紫薇，即使有車可開，那時候我也絕對要走路，這些是讓我最快樂的事，這才是人。如果我們吃得不像人，穿得不像人，生活都失去了人的意義，那談藝術太遙遠。我談我的生活，並不希望別人學我。每個人是不一樣的，不要隨便相信價格、人云亦云，生活中的美學，應該是不按照別人安排的。每個人應該用自己的生命，去創造自己的生活美學出來。</p>
        </div>
        <!--~~~~~~~~~~~~~~~~~-->
        
        
        <!--~~~~~~~~~~~~~~~~~--> 
        <div class="footer">
            NTUB imd, 2019.    
        </div>        
        <!--~~~~~~~~~~~~~~~~~-->         
    </div>
    <!--**************************--> 
    <!-- 載入js                    -->
    <!--**************************--> 
    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
    <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>   
    <script src="js/jQueryRotate.js"></script>            
    <script src="js/main.js"></script>    
</body>
   
</html>
```


### (2) main.css

```css
@charset "utf-8";

/*---------------------------*/
/* 編排網頁                   */
/*---------------------------*/
html, body{
    font-family: 'Noto Sans TC', sans-serif; 
    background:#444;
    margin:0;
    padding:0;
}

/*---------------------------*/
/* 編排<標題>區塊              */
/*---------------------------*/
div.header{
    width:100%;
    min-width:800px;
    height:80px;
    background:rgba(51,51,51,0.7);
    box-shadow:0px 1px 10px 0px #333;	
    position:fixed;
    z-index:10;
}

/* 定義logo圖示 */
div.header img.logo{
    width:80px;
    height:80px;
    border-radius:40px;
    position:relative;
    z-index:30;	
    left:50%;
    top:25px;
    margin-left:-40px;     
    box-shadow:0px 1px 3px 1px #000;
}

/* 定義logo圖示(滑鼠移入) */
div.header img.logo:hover{
    cursor:pointer;
}

/* 編排<導覽列> */
div.navbar{
    width:800px;	 
    height:40px;
    line-height:40px;
    font-size:18px;      
    position:relative;
    left:50%;
    top:-50px;
    margin-left:-400px;
}

div.navbar ul{	     
    margin:0;
    padding:0;
    list-style-type:none;	
}

div.navbar ul li{
    width:150px;
    text-align:center;	
    float:left;
    color:#fff;
}

div.navbar ul a:nth-child(2) li{
    margin-right:200px;
}

/*---------------------------*/
/* 編排<容器>區塊             */
/*---------------------------*/
div.container{
    width:800px;
    border:1px solid #666;  
    margin:0 auto;
    background:#fff;
    box-shadow:0px 0px 10px 0px #000;
    position:relative;
    top:80px;
    z-index:5;
}

/*---------------------------*/
/* 編排<內文>區塊              */
/*---------------------------*/
div.content{
    padding:20px 25px;    
    font-size:20px;
    line-height:32px;   	
    text-align:justify;
}

/*---------------------------*/
/* 編排<表尾>區塊             */
/*---------------------------*/
div.footer{
    height:60px;
    line-height:60px;
    background:#CCC;
    font-size:13px;
    text-align:center;
    letter-spacing:3px;
}

/*========================*/
/* 互動設計                */
/*========================*/
div.navbar ul a:hover li{
    color:#aaa;
}
```


### (3) main.js

``` js
var isOpened=true;

$(function(){
    //-----------------
    // 如果圖示被點擊
    //-----------------
    $('.header .logo').mousedown(function(){
        if(isOpened){
            //將導覽列收回
            $(this).parent().stop().animate({marginTop:-80}, {duration:400, easing:'easeOutBounce'});
            $(this).stop().animate({top:40}, {duration:400, easing:'easeOutBounce'});	
            $(this).rotate({
                angle: 0,
                animateTo:180,
                duration:1000
            });				
            isOpened=false;
        }else{
            //將導覽列打開
            $(this).parent().stop().animate({marginTop:0}, {duration:400, easing:'easeOutBounce'});
            $(this).stop().animate({top:20}, {duration:400, easing:'easeOutBounce'});
            $(this).rotate({
                angle: -180,
                animateTo:0
            });				
            isOpened=true;	
        }
    });
    //-----------------
});
```
