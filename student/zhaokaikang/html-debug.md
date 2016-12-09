## www.so.com 首页找茬 嘻嘻
### header栏中天气预报(隐藏部分),个人觉得有以下几个问题
    1. 可用ul>li列表结构实现
    2. a标签是内联元素不应该嵌套div块元素
    3. img标签未写alt属性
    4. a标签未写title属性
    5. <input type="button"> 从语义化来说应使用<button type="submit"></button>
```HTML
<div class="detail" style="display: block;">
    <a class="seven" href="http://www.weather.com.cn/weather/101010100.shtml#7d" target="_blank">未来七天天气</a>
    <div class="title">12月9日－
        <span class="at">北京</span>
        <a href="javascript:;" class="change">切换</a></div>
    <div class="select" style="display: none;">
        <select class="province">
        </select>
        <select class="city">
        <select class="town">
        <input type="button" class="ok" value="更换"></div>
    <div class="curr-day">
        <a href="/s?ie=utf-8&amp;src=search_weather&amp;q=%E5%8C%97%E4%BA%AC%E5%A4%A9%E6%B0%94%E9%A2%84%E6%8A%A5" target="_blank">
            <img src="https://p.ssl.qhimg.com/dm/60_60_/d/inn/3716a4d4/1-0.png">
            <div class="curr-day-wrap">
                <span class="weather">-5~5°C</span>
                <span class="feature">晴</span>
                <span class="wind">北风 微风</span>
            </div>
        </a>
    </div>
    <div class="list">
        <a href="/s?ie=utf-8&amp;src=search_weather&amp;q=%E5%8C%97%E4%BA%AC%E5%A4%A9%E6%B0%94%E9%A2%84%E6%8A%A5" target="_blank">
            <div>明天</div>
            <img src="https://p.ssl.qhimg.com/d/inn/9371c065/weather/bg-w/1-0.png">
            <div>晴</div>
            <div>-4~5°C</div></a>
        <a href="/s?ie=utf-8&amp;src=search_weather&amp;q=%E5%8C%97%E4%BA%AC%E5%A4%A9%E6%B0%94%E9%A2%84%E6%8A%A5" target="_blank">
            <div>后天</div>
            <img src="https://p.ssl.qhimg.com/d/inn/9371c065/weather/bg-w/1-33.png">
            <div>霾</div>
            <div>-1~5°C</div></a>
        <a href="/s?ie=utf-8&amp;src=search_weather&amp;q=%E5%8C%97%E4%BA%AC%E5%A4%A9%E6%B0%94%E9%A2%84%E6%8A%A5" target="_blank">
            <div>12月12日</div>
            <img src="https://p.ssl.qhimg.com/d/inn/9371c065/weather/bg-w/1-33.png">
            <div>霾</div>
            <div>-3~7°C</div></a>
    </div>
</div>
```

#### 顶部中已用nav标签，整个导航栏为什么不使用header标签呢,同理，底部也采用footer标签，主体也应采用main标签
#### 360搜索框附近的提示列表也是div嵌套div
```HTML
<div class="ac_wrap" style="min-width: 528px; top: 42px; left: 0px; display: none;">
    <div unselectable="on" class="ac_wrap_inner">
        <div unselectable="on" class="ac_menu_ctn">
            <div unselectable="on" id="ac_one"></div>
                <ul unselectable="on" class="ac_menu" ac_word="a" ver="3.2.2"></ul>
            </div>
            <div unselectable="on" id="provided-by" class="ac_toolbar" style="position: absolute;">由360搜索提供</div>
        </div>
</div>
```