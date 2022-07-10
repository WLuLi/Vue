<template>
    <body id="web">
        <div id="center">
            <!--橘色边框-->
            <div class="greet">
                <p class="big_greet_text">:P</p>
                <p class="greet_text_chinese">欢迎，</p>
                <p class="greet_text_english">Welcome,</p>
            </div>
            <div class="orange_greet_triangle"></div>
            <div class="greet_small_margin"></div>
            <!--中央的大方框-->
            <div id="info"><!--the gray rectangle-->
                <h2 class="user_name" id="u_name">WangLuli</h2>
                <div id="info_content">
                    <div class="label_text">
                        已连接
                        <p class="english">Duration</p>
                    </div>
                    <div class="clock_text">
                        <span class="clock" style="color:#ec6677">00:00:00</span>
                        <span class="unit"></span>
                    </div>
                    <div class="label_text">
                        已用流量
                        <p class="english">Usage</p>
                    </div>
                    <div class="usage_bar">
                        <ul class="usage_number">
                            <li>125</li>
                            <li>100</li>
                            <li>75</li>
                            <li>50</li>
                        </ul>
                        <div id="usage_value" style="width:18.1487px;"></div>
                        <div class="stripe"></div>
                        <div class="stripe second_stripe"></div>
                        <div class="content_text">
                            <span class="unit" id="usage_flux">8.56G</span>
                        </div>
                    </div>
                </div>
            </div>
            <!--断开连接的按钮-->
            <div class="button_bar">
                <!--下面button中绑定事件及响应函数-->
                <button class="button_disconnect">
                    <p class="chinese">断开连接</p>
                    <p class="english">Disconnect</p>
                </button>
            </div>
            <!--链接-->
            <ul id="links">
                <!--之后添加href-->
                <li>
                    <a id="link_info" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421f9f9479369247b59700f81b9991b2631506205de" target="_new" title="清华信息门户 info.tsinghua">Info</a>
                </li>
                <li>
                    <a id="link_lib" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fcfe43d23323615e79009cadd6502720703f47/" target="_new" title="清华图书馆lib.tsinghua">Lib</a>
                </li>
                <li>
                    <a id="link_learn" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fcf2408e297e7c4377068ea48d546d30ca8cc97bcc/" target="_new" title="清华网络学堂learn.tsinghua">Learn</a>
                </li>
                <li>
                    <a id="link_mail" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fdf6489069247b59700f81b9991b263165e79cae/" target="_new" title="清华邮箱mail.tsinghua">Mail</a>
                </li>
            </ul>
        </div>
    </body>
</template>

<script>
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    border: 0;
}
div {
    display: block;
}
h2 {
    font-size: 1.5em;
    margin-block-start: 0.83em;
    margin-block-end: 0.83em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
ul {
    list-style-type: disc;
    list-style: none;
}
a {
    color: #AD3B23;
    text-decoration: none;
}
.english {
    font-family: Verdana, Geneva, sans-serif;
}
#web{
    min-width: 640px;
    min-height: 480px;
    background:#E6E6E6 url(../assets/pic/popup_bg.png) no-repeat top right;
}
body {
    min-width: 768px;
    font-family: "Microsoft YaHei", "SimHei", "Apple LiGothic Medium";
}
#web #center{
    position:relative;
    width:640px;
    height: 480px;
    background: url(../assets/pic/popup_shadow.png) no-repeat 48px 344px;
    margin:auto;
}
#web .greet{
    position: absolute;
    top: 64px;
    left: 48px;
    width: 512px;
    height: 224px;
    background:#E64E2E;
}
.greet, #title{
    overflow: hidden;
}
.greet .big_greet_text{
    font-weight:lighter;
    position: absolute;
    top:30px;
    left:20px;
    font-family: Verdana, sans-serif;
    color:white;
    font-size:70px;
}
.greet .greet_text_chinese{
    position: absolute;
    top:120px;
    left:25px;
    color:white;
    font-size:30px;
}
.greet .greet_text_english{
    position: absolute;
    top:160px;
    left:25px;
    font-family: Verdana, sans-serif;
    color:white;
    font-size:20px;
}
#web .orange_greet_triangle{
    position: absolute;
    left:80px;
    top:288px;
    border-color:#E64E2E transparent;
    border-width: 48px 48px 0 0;
    border-style: solid;
}
#web .greet_small_margin{
    position: absolute;
    top: 288px;
    left: 592px;
    border-color: transparent #CCCCCC;
    border-width: 16px 0 0 16px;
    border-style: solid;
}
#web #info{
    position:absolute;
    top:96px;
    left:176px;
    padding: 32px;
    width: 352px;
    height: 208px;
    background: #F2F2F2;
}
#info .user_name{
    float: left;
    color: #E64E2E;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 34px;
    font-weight: lighter;
    margin: 0;
}

#info #info_content{
    float: left;
    margin-top: -8px;
}
#info .content_text {
    float: left;
    margin: 24px 0 0 20px;
    padding-top: 4px;
    height: 28px;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 28px;
    font-weight: lighter;
}
.label_text .english {
    color: #303030;
    font-size: 16px;
    margin:0;
}
#info .label_text .english {
    font-size: 13px;
}
#info .label_text {
    clear: left;
    float: left;
    width: 56px;
    height: 32px;
    margin-top: 22px;
    text-align: right;
    font-size: 13px;
}
#info .clock_text {
    float: left;
    margin: 24px 0 0 20px;
    padding-top: 4px;
    height: 28px;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 28px;
    font-weight: lighter;
}
#info .content_text .unit {
    margin-left: 8px;
    color: #5C5C5C;
    font-size: 24px;
}
#info .usage_bar {
    position: relative;
    float: left;
    margin: 24px 0 0 16px;
    padding: 0;
    width: 280px;
    height: 32px;
    background: url(../assets/pic/usage_bg.gif) repeat-y;
}
#info .usage_bar .content_text {
    position: absolute;
    top: 2px;
    left: 4px;
    float: none;
    margin: 0;
    padding: 0;
}
.usage_bar .stripe {
    position: absolute;
    top: 0;
    right: 4px;
    width: 4px;
    height: 100%;
    background: #F2F2F2;
}
.usage_bar #usage_value {
    float: left;
    height: 32px;
    max-width: 280px;
    background: #FBB03B;
}
.usage_bar .second_stripe {
    right: 12px;
}
.usage_bar .usage_number {
    position: absolute;
    top: -16px;
    right: 14px;
    font-family: Verdana, Geneva, sans-serif;
    font-size: 13px;
    color: #969696;
}
.usage_number li {
    float: right;
    width: 53px;
    text-align: right;
}
#web .button_bar {
    position: absolute;
    top: 304px;
    right: 32px;
    width: 208px;
    height: 80px;
    background: #FFFFFF;
    -webkit-box-shadow: 0 0 8px rgb(0 0 0 / 10%);
    -moz-box-shadow: 0 0 4px rgba(0,0,0,0.1);
    box-shadow: 0 0 8px rgb(0 0 0 / 10%);
}
.button_bar .button_disconnect {
    margin: 16px;
    width: 174px;
    height: 46px;
    border: #B2AABE solid 1px;
    background: #C0BDCC url(https://webvpn.tsinghua.edu.cn/http/7772647…/image/disconnect.png) no-repeat center 0;
    overflow: hidden;
}
.button_bar .button_disconnect .chinese{
    color: #000000;
    font-size: 21px;
    font-weight: normal;
    margin: -3px;
    text-shadow: 0 0 2px #5C5C5C;
}
.button_bar .button_disconnect .english{
    color: #5C5C5C;
    font-size: 16px;
    margin: -3px;
    text-shadow: 0 0 1px #5C5C5C;
}
#web #links {
    position: absolute;
    bottom: 32px;
    right: 32px;
    width: 250px;
}
#links li {
    float: left;
    margin-right: 12px;
    font-size: 11px;
    font-family: Verdana, Geneva, sans-serif;
}
#links li a {
    display: block;
    padding: 16px 0 0 26px;
    height: 16px;
}
#links #link_info {
    background: url(../assets/pic/popup_info.gif) no-repeat 2px 2px;
}
#links #link_lib {
    background: url(../assets/pic/popup_lib.gif) no-repeat 2px 2px;
}
#links #link_learn {
    background: url(../assets/pic/popup_learn.gif) no-repeat 4px 1px;
}
#links #link_mail {
    background: url(../assets/pic/popup_mail.gif) no-repeat 0 1px;
}

#links li:last-child{
    float:right; margin:0;
}
</style>
