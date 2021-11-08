# StepNumberChangeSNC
## 特别声明：
**1、请勿将本仓库的任何内容用于商业或非法目的，否则后果自负。**

2、间接使用脚本的任何用户，包括但不限于建立VPS或在某些行为违反国家/地区法律或相关法规的情况下进行传播, 本人对于由此引起的任何隐私泄漏或其他后果概不负责。

3、如果任何单位或个人认为该项目的脚本可能涉嫌侵犯其权利，则应及时通知并提供身份证明，所有权证明，我们将在收到认证文件后删除相关脚本。

4、任何以任何方式查看此项目的人或直接或间接使用该项目的任何脚本的使用者都应仔细阅读此声明。本人保留随时更改或补充此免责声明的权利。一旦使用并复制了任何相关脚本或Script项目的规则，则视为您已接受此免责声明。  


## 使用说明： 
* 该函数有借鉴 [网友的博客](https://www.iloveu.top/index.php/2021/03/30/misport-steps-tool) 中的图片，代码为(公众号：Gwen博客)提供，最后由本人写出总结的方法，并上传至github中，如有侵权，请立即联系本人删除。

* 该函数是通过小米运动app进行修改，从而实现微信支付宝的运动步数修改，再使用腾讯云的定时器，实现全自动每日随机修改步数（20000-29999）

（以下为文字教程，图片教程我放在word里了，可以下载观看，这边就不放图片了，上传到图床有点小麻烦（懒^））

1.从应用商店或者浏览器下载小米运动App，打开软件并输入手机号登录，不要使用第三方账号登录

2.点击我的->第三方接入，绑定你想同步数据的项目 注：同步微信运动请按照要求关注公众号。

3.下载bushu.py，去腾讯云函数中进行布置函数，放在index.py中

4.在函数的148行和150行写下账号和密码，让其自己进行修改

5.如果想要自己修改步数，那就在152行输入步数，如果不想，则留空为随机步数，（20000-29999）

6.触发管理，创建触发器，选择你想要的时间进行修改

7.部署并进行测试，成功的话支付宝会显示步数，即可。

8.可以自行添加通知脚本（QQ/微信都可以），QQ使用Qmsg酱，自行注册并使用，写在第123行中的qqtalk中；微信则使用Server酱（https://sct.ftqq.com/sendkey） ，该部分需自行探索，可用可不用。

如有任何问题，请留下您的Issues，看到都会回复，尽可能的帮你解决问题

## 个人使用建议：

**我本人每天刷步数主要是为了三个目的：**

1、蚂蚁森林每天296g的能量 

2、支付宝，运动，每日捐款

3、微信运动捐步数捐款

**能够用代码来为世界做一些善事，我认为是一件非常值得的事情，希望大家也可以用代码为世界多做一些贡献。**

**最后，送各位一句话，勿以善小而不为，勿以恶小而为之。**

___Don't to small and not for good, it is a sin to steal a pin___

<img src="https://s3.bmp.ovh/imgs/2021/11/5cbc397f85aacf53.jpg" width="30%"> <img src="https://gitee.com/EEEugene/my-drawing-bed/raw/master/img/微信图片_20211108234005.jpg" width="30%">
