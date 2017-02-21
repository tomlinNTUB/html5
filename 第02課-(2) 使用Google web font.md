#第02課 文字排版及字型設定


## (2) 使用Google web font


#####執行結果:
![GitHub Logo](/imgs/results02-2.jpg)


#####網路資源:
https://fonts.google.com/


#####檔案放置方式:
```
   | 
   |___<css>
   |     |___ main.css
   |	 
   |___index.html   
```


#####檔案名稱: index.html 
```html
<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>測試網頁</title>
<!-- 加入 main.css -->
<link href="css/main.css" rel="stylesheet" type="text/css" />
<!-- 加入 google web fonts -->
<link href="https://fonts.googleapis.com/css?family=Amatic+SC|Handlee" rel="stylesheet">
</head>
<body>
<!-- *** 加入一個區塊 *** -->
<div class="content">
    <h1>Introducing Taiwan</h1>
    
    <p>With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication, Taiwan is a continent on one green island.</p>
    
    <h2>The Beautiful Isle</h2>
    <p>Famed for centuries as Ilha Formosa (Beautiful Isle; 美麗島; Měilìdǎo), this is a land with more sides than the 11-headed Guanyin. Towering sea cliffs, marble-walled gorges and tropical forests are just the start of your journey, which could take you as far as Yushan, Taiwan's 3952m alpine roof.</p>
    
    <p>In Taiwan you can criss-cross mountains on colonial-era hiking trails or cycle a lone highway with the blue Pacific on one side and green volcanic arcs on the other. And if you simply want a classic landscape to enjoy, you'll find them around every corner.</p>
    
    <h2>The Tao of Today</h2>
    <p>Taiwan is heir to the entire Chinese tradition of Buddhism, Taoism, Confucianism and that amorphous collection of deities and demons worshipped as folk faith. Over the centuries the people have blended their way into a unique and tolerant religious culture that's often as ritual heavy as Catholicism and as wild as Santeria.</p>
    
    <p>Taiwanese temples (all 15,000) combine worship hall, festival venue and art house under one roof. Watch a plague boat burn at Donglong Temple, go on a pilgrimage with the Empress of Heaven, study a rooftop three-dimensional mosaic, and learn why a flag and ball have come to represent prayer.</p>
    
    <h2>Have You Eaten?</h2>
    <p>'Have you eaten?' The words are used as a greeting here, and the answer is always 'yes', as there's just too much nibbling to do. Taiwan offers the gamut of Chinese cuisines, some of the best Japanese outside Japan, and a full house of local specialities from Tainan milkfish and Taipei beef noodles to indigenous barbecued wild boar. Night markets around the island serve endless feasts of snacks including stinky tofu, steamed dumplings, oyster omelettes, shrimp rolls and shaved ice. And when you're thirsty you can look forward to juices from the freshest local fruits, local craft beer, aromatic teas and, in a surprising twist, Asia's best gourmet coffee.</p>
    
    <h2>Why I Love Taiwan</h2>
    <p>When I visited Taiwan as a child, the wondrous rocks of Yeliu made an impression. Years later, a fan of director Hou Hsiao-hsien, I went to Jiufen and Fengkuei to see the settings that gave rise to the films I enjoyed, and was bewitched. Now Penghu's windswept islands mesmerise me, as does the taste of musk melons. Taiwan is full of surprises if you know where to look, like the night I waited for a meteor shower in Kenting. I'd expected a crowd to show up, but there wasn't even a hint of a shadow. I was completely alone. Then I looked up – the whole sky was moving.</p>
    
    <h2>Asian Values On Their Terms</h2>
    <p>Defying those who said it wasn't in their DNA, the Taiwanese have created Asia's most vibrant democracy and liberal society, with a raucous free press, gender equality, and respect for human rights and, increasingly, animal rights as well. The ancestors are still worshipped, and mum and dad still get their dues, but woe betide the politician who thinks it's the people who must pander, and not him – or her. If you want to catch a glimpse of the people's passion for protest, check out Taipei Main Station on most weekends, or just follow the local news.</p>
</div>
<!-- *** 區塊的結束 -->
</body>
</html>
```


#####檔案名稱: css/main.css
```css
@charset "utf-8";

/*---------------------------*/
/* 定義網頁                   */
/*---------------------------*/
html, body{
    font-size:20px;
	/*設定google web font*/
	font-family: 'Handlee', cursive;   
}


/*---------------------------*/
/* 定義內容                   */
/*-------------------------*-*/
div.content{
    width:800px;
    border:1px solid #666;  
    margin-top:50px;
    margin-bottom:50px;
    margin-left:auto;
    margin-right:auto;
    box-sizing:border-box;
    padding:20px 25px 20px 25px;
    line-height:32px;   
    text-align:justify;
}
```
