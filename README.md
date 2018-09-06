##  导航
- [demo1](#demo1)---百度统计
- [demo2](#demo2)---自动更换公司名称及资质
- [demo3](#demo3)---单页微信修改
- [demo4](#demo4)---手机验证码模块
- [demo5](#demo5)---复制微信
- [demo6](#demo6)---轮播
- [demo7](#demo7)---nav滚动
- [demo8](#demo8)---视频播放模块
- [demo9](#demo9)---m端fastClick
- [demo10](#demo10)---小能代码
- [demo11](#demo11)---动画至锚点
- [demo12](#demo12)---倒计时模块
- [demo13](#demo13)---表格标题显示切换
- [demo14](#demo14)---导航滚屏
- [demo15](#demo15)---元素入屏幕动画

###  demo1
####  百度统计
```
<script>
    var _hmt = _hmt || [];
    (function() {
        var hm = document.createElement("script");
        hm.src = "https://hm.baidu.com/hm.js?2c681ae4f5f65e293c799beac90eedb7";
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(hm, s);
    })();
</script>
```
###  demo2
####  自动更换公司名称及资质 registeredSh/registeredBd/registered
#####  审核页面
**引用方法库**
```
<script src="https://js.ykclass.com/frame/jquery/v2.1.4/jquery.min.js"></script>
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
    $_y.registeredSh();
```
#####  百度单页
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
    $_y.registeredBd();
```
#####  其他页面
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
公司名称替换成如下：
```
<span id="registeredName"></span>
```
备案号替换成如下：
```
<span id="registeredNum"></span>
```
证书部分替换成：
```
<div class="p-warp" id="certificate">
    <p>网络文化经营许可证 鄂网文许字【2014】1409-032号</p>
    <p>互联网出版许可证 鄂字第23号 </p>
</div>
```
例：M端替换后如下：
```
<div class="p-warp">
    <p>版权所有@<span id="registeredName"></span> </p>
    <p> 2018 保留一切权利 <span id="registeredNum"></span> </p>
</div>
<div class="p-warp" id="certificate">
    <p>网络文化经营许可证 鄂网文许字【2014】1409-032号</p>
    <p>互联网出版许可证 鄂字第23号 </p>
</div>
```
**调用方法**
```
   $_y.registered();
```
### demo3
####  单页微信修改 changeWeChat
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
    $_y.changeWeChat(['gpa6597']);
```
### demo4
####  手机验证码模块 saveActivitySmsInfo
##### 【html】
```
<!--弹出层 开始-->
<div class="layer-warp">
    <div class="layer">
        <div class="title">恭喜您，提交成功！</div>
        <div class="text">
            您好，您的信息已提交成功，<span class="c-b">查询结果将于15分钟内以短信或电话的方式通知您，</span>请注意查收！
        </div>
        <div class="layer-close"></div>
    </div>
</div>
<!--弹出层 结束-->
```
##### 【css  M】
```
.layer-warp {
	position: fixed;
	left: 0px;
	top: 0px;
	right: 0px;
	bottom: 0px;
	display: none;
	text-align: center;
	background: rgba(0, 0, 0, 0.4);
	z-index: 9999999;
	.layer {
		position: absolute;
		top: 50%;
		left: 35%;
		transform: translate(-35%, -50%);
		.w(700);
		.h(700);
		background: url(//m.ykclass.com/zt/zyImages/ykclass/layer.png) no-repeat;
		background-size: cover;
		z-index: 99999999;
	}
	.title {
		position: absolute;
		top: 110/75rem;
		left: 164/75rem;
		.fs(50);
		color: #fff;
	}
	.text {
		position: absolute;
		top: 260/75rem;
		left: 130/75rem;
		color: #666666;
		.w(490);
		.h(250);
		.fs(36);
		line-height: 1.5;
		text-align: left;
		.c-b {
			font-weight: bold;
			color: #333333;
		}
	}
	.layer-close {
        position: absolute;
        top: 502/@r;
        left: 134/@r;
        .w(463);
        .h(92);
    }
}
```
##### 【css  PC】
```
.layer-warp {
    position: fixed;
    left: 0px;
    top: 0px;
    right: 0px;
    bottom: 0px;
    display: block;
    text-align: center;
    background: rgba(0, 0, 0, 0.4);
    z-index: 99999;
    .layer {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: 400px;
        width: 400px;
        background: url(//m.ykclass.com/zt/zyImages/ykclass/layer.png) no-repeat;
        background-size: cover;
        z-index: 99999999;
    }
    .title {
        position: absolute;
        top: 60px;
        left: 100px;
        font-size: 26px;
        color: #fff;
    }
    .text {
        position: absolute;
        top: 145px;
        left: 60px;
        color: #666666;
        width: 300px;
        height: 300px;
        font-size: 20px;
        line-height: 1.5;
        text-align: left;
        .c-b {
            font-weight: bold;
            color: #333333;
        }
    }
    .layer-close {
        position: absolute;
        top: 286px;
        left: 76px;
        height: 54px;
        width: 268px;
    }
}
```
##### 【html】
```
<div id="get-phone">
    <div class="row">
        <input class="phone-num" type="number" placeholder="请输入电话号码">
        <input class="send-code" type="button" value="获取验证码">
    </div>
    <div class="row">
        <input class="code-value" type="number" placeholder="请输入验证码">
    </div>
    <button class="vail-code">提交</button>
</div>
```
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.saveActivitySmsInfo({
    id: '#get-phone2',    // 获客模块id  必需
    cjCode: 'YK_TT_TONGJI',     // 场景代码  必需
    needMsg: true,      // 是否短信验证(true表示需要)  非必需
    countdown: 90,      // 首次倒计时时间（默认90）  非必需
    info: infoObj,      // 传入的用户填写信息（一个包含msg参数的对象）   非必需
    toutiaoCallback: function () {      // 获客完成后回执  非必需
        if(_taq) {
          _taq.push({convert_id: "1606319178273799", event_type: "form"})
        }
    }
});
```
附带信息如
```
var infoObj = {
    msg: ''
};
$('.vail-code').on('click',function () {
    var province = $('#province').val();
    var education = $('#education').val();
    infoObj.msg = province + '-' + education;
    // 信息自行更换
});
```
### demo5
####  复制微信 copyWeChat
##### 【html】
```
<!--弹出层 开始-->
<div class="weChatB w_2">
    <div class="title">加微信领取</div>
    <p class="weChatTitle">长按复制下方微信添加为好友<br>↓↓↓</p>
    <p class="weChatCenter wxnumber"></p>
    <p class="weChatBottom">微信咨询  免费获取信息</p>
</div>
<!--弹出层 结束-->

<div class="footerBar">
    <p>老师微信：<span class="c-yellow wxCode"></span>（点击复制）</p>
</div>
<div class="footH" style="height: 1.2rem"></div>
```
##### 【css】
```
// 底部浮动条
.footerBar {
	width: 10rem;
	position: fixed;
	height: 1.2rem;
	bottom: 0;
	left: 50%;
	margin-left: -5rem;
	background-color: #E9360F;
	p {
    	line-height: 1.2rem;
    	font-size: 0.4rem;
    	color: #fff;
    	text-align: center;
    }
    .c-yellow {
    	color: #FFF83A;
    }
}
// 微信弹窗
div.layui-layer {   //取消layer默认外阴影
	box-shadow: none;
}
.weChatB {
	display: none;
	width: 8.36rem;
	height: 6.066666666666666rem;
	background: url(//m.ykclass.com/zt/zyImages/ykclass/layer-wx.png) no-repeat center;
	background-size: cover;
	.title {
    	height: 1.2533333333333334rem;
    	font-size: 0.56rem;
    	line-height: 1.2533333333333334rem;
    	color: #FFFFFF;
    	text-align: center;
    }
    .weChatTitle {
    	text-align: center;
    	margin: 0.7066666666666667rem auto 0.16rem ;
    	font-size: 0.4rem;
    	line-height: 0.6666666666666666rem;
    	color: #ff452d;
    }
    .weChatCenter {
    	width: 5.04rem;
    	height: 1.24rem;
    	display: block;
    	font-weight: bold;
    	background: #ff1a1f;
    	border-radius: 0.49333333333333335rem;
    	margin: 0 auto;
    	font-size: 0.56rem;
    	color: #FFFFFF;
    	text-align: center;
    	line-height: 1.2933333333333332rem;
    }
    .weChatBottom {
    	text-align: center;
    	font-weight: bold;
    	font-size: 0.5rem;
    	line-height: 0.5333333333333333rem;
    	color: #ff1a1f;
    	margin-top: 0.3466666666666667rem;
    }
}
// 微信弹窗（新版）
div.layui-layer {   //取消layer默认外阴影
	box-shadow: none;
}
.weChatB {
    display: none;
	width: 7.6rem;
	height: 8rem;
	box-sizing: border-box;
	background: url(//m.ykclass.com/zt/zyImages/ykclass/1533535073405.png) no-repeat center;
	background-size: cover;
	padding-top: 1.5rem;
	.title {
		font-size: 0.6rem;
		line-height: 1.25rem;
		color: #FFFFFF;
		text-align: center;
	}
	.weChatTitle {
		text-align: center;
		margin-top: 0.7rem;
		font-size: 0.4rem;
		line-height: 0.8rem;
		color: #ff452d;
	}
	.weChatCenter {
		width: 5.04rem;
		line-height: 1.24rem;
		font-weight: bold;
		background: #ff1a1f;
		border-radius: 0.5rem;
		margin: 0.2rem auto;
		font-size: 0.7rem;
		color: #FFFFFF;
		text-align: center;
	}
	.weChatBottom {
		text-align: center;
		font-weight: bold;
		font-size: 0.5rem;
		line-height: 0.5rem;
		color: #ff1a1f;
		margin-top: 0.4rem;
	}
}
```
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/layer/layer.js"></script>
<script src="//m.ykclass.com/zt/zyjs/clipboard.min.js"></script>
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
// 新版弹窗
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.copyWeChat(['qbk8730']);
```
### demo6
####  轮播 slider
##### 【html】
```
<div id="slide">
    <ul class="slider">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
    <ol class="control clearfix">
        <li data-i="0" class="active">1</li>
        <li data-i="1">2</li>
        <li data-i="2">3</li>
        <li data-i="3">4</li>
    </ol>
    <div class="bar">
        <div class="l"><</div>
        <div class="r">></div>
    </div>
</div>
```
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.slider({
    id: '#slide',   // 轮播模块id   必需
    mode: 1,        // 轮播方式 1、左右切换 2、淡出淡入切换    必需
    addTouch: true,     // 是否手指滑动事件 true 有滑动事件     非必需
    moveTime: 400,      // 轮播切换动画时间（默认800毫秒）    非必需
    interval: 3000,      // 轮播间隙时间（默认4000毫秒）     非必需
    mouseenterStop: true      // 鼠标进入时轮播是否停止
});
```
### demo7
####  nav滚动(已封装，见demo14)
```
<script src="js/scrollPage.js"></script>
// 滚屏
    $(".common-module").scrollPage();
```
### demo8
####  视频播放模块
##### 【js】
```
<script src="http://static.ykclass.com/frame/polyv/polyvplayer.min.js"></script>
//视频
	var uid = "336d8745b4";
	var vid = "5af4dd0127c62475750485dc988b22d2_5";
	var videoPlayer = null; //live：直播播放器  video：点播播放器
	initVidoPlayer(vid);
	function initVidoPlayer(vid) {
		videoPlayer = polyvObject('#player').videoPlayer({
			'width': '100%',
			'height': '100%',
			'vid': vid,
			flashParams: {
				'allowScriptAccess': 'always',
				'allowFullScreen': 'true',
				'quality': 'high',
				'bgcolor': '#ffffff',
				'wmode': 'transparent',
			},
			flashvars: {
				'autoplay': '1',
				'is_auto_replay': 'on',
				'ban_history_time': 'on',
				'setScreen': 'fill',
			}
		});
	};
```
### demo9
####  m端fastClick
```
<script src="http://js.ykclass.com/frame/fastClick/v1.0.0/fastClick.js"></script>
// 快速点击
FastClick.attach(document.body);
```
### demo10
####  小能代码
```
var kf = 'kf_9540_1520933792603';
var NTKF_PARAM = {
    "siteid": "kf_9540" /*网站siteid*/ ,
    "settingid": kf /*代码ID*/ ,
    "uid": "" /*会员ID*/ ,
    "uname": "" /*会员名*/ ,
    "userlevel": "0" /*会员等级*/
};
$(document).on("click", ".ntkf", function() {
    NTKF.im_openInPageChat(kf);
});
```
**引用js文件**
```
<script type="text/javascript" src="//dl.ntalker.com/js/xn6/ntkfstat.js?siteid=kf_9540" charset="utf-8"></script>
```
### demo11
####  动画至锚点 scrollTo
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.scrollTo('#id');
```
### demo12
####  倒计时模块
```
var today = new Date().getTime();
var  examDay = [2018,4,24];
var endDay = new Date(examDay[0], examDay[1]-1, examDay[2]).getTime();
if(endDay - today > 0) {
    var day = Math.ceil((endDay - today) / (24 * 60 * 60 * 1000));
    var single = day % 10;
    var decade = parseInt((day % 100) / 10);
    var hundreds = parseInt((day % 1000) / 100);
    $(".single").html(single);
    $(".decade").html(decade);
}
```
### demo13
####  表格标题显示切换 fixedTop
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.fixedTop({
    target: '#table-title',  // 目标元素
    relatedTarget: '.table',   // 关联元素
    time: 50,   // 节流时间（ms）默认50
    subtractHeight: 0   // 底部预留高度 默认0
});
```
### demo14
####  导航滚屏 scrollPage
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.scrollPage('.class');
// 导航条需为包含类名'md'的ul/ol
```
### demo15
####  元素入屏幕动画 enterScreenAnimate
##### 【css】
[Animate.css 动画库](https://daneden.github.io/animate.css/)
```
<link rel="stylesheet" type="text/css" href="//m.ykclass.com/zt/zyjs/animate.css"/>
```
[Magic.css 动画库](https://www.minimamente.com/example/magic_animations/)
```
<link rel="stylesheet" type="text/css" href="//m.ykclass.com/zt/zyjs/magic.min.css"/>
```
##### 【js】
**引用方法库**
```
<script src="//m.ykclass.com/zt/zyjs/yuanaaa1.2.js"></script>
```
**调用方法**
```
$_y.enterScreenAnimate([
    {
        el: part1,   // dom元素
        animateType: 'bounceIn',   // 动画类型，动画样式的class
        addLibrary:'animated'     // 依赖animate.css 库
    }, {
        el: '.part-2',   // 类名或者ID
        animateType: 'puffIn',      // 动画类型，动画样式的class
        addLibrary: 'magictime'     // 依赖magic.css 库
    }
]);
```