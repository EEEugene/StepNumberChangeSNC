# StepNumberChangeSNC

## action 运行

使用本仓库需要 Zepp Life app（_原小米运动 app_），请务必把 Zepp Life 注册好，设置好，与微信的同步/第三方接入什么的都弄好再往下看

<p align="right">（<a href="#修改微信运动步数">回到顶部</a>）</p>
  
## 使用指南
### 通过GithubAction
   1. Fork 本仓库
   2. 在你自己 Fork 的仓库进行设置`Settings - Actions - General - Allow all actions and reusable workflows`，别忘了`save`
   3. 然后`Settings - Secrets - Actions - New repository secret`，按下面例子新建几个`secrets`：
#### secrets 变量
   <table>
    <tr>
     <td>Name</td>
     <td>Value</td>
    </tr>
    <tr>
     <td>USER_PHONE</td>
     <td></td>
    </tr>
    <tr>
     <td>USER_PWD</td>
     <td></td>
    </tr>
    <tr>
     <td>TG_BOT_TOKEN</td>
     <td></td>
    </tr>
     <td>STEP</td>
     <td>10000</td>
    </tr>
    <tr>
     <td>STEP_MAX</td>
     <td>12000</td>
    </tr>
    <tr>
     <td>TG_BOT_TOKEN</td>
     <td></td>
    </tr>
    <tr>
     <td>TG_USER_ID</td>
     <td></td>
    </tr>
    <tr>
     <td>TX_QQ</td>
     <td></td>
    </tr>
    <tr>
     <td>STEP</td>
     <td></td>
    </tr>
    <tr>
     <td>STEP_MIN</td>
     <td>10000</td>
    </tr>
    <tr>
     <td>STEP_MAX</td>
     <td>30000</td>
    </tr>
   </table>
   
-`USER_PHONE`是注册Zepp Life app的手机号，`USER_PWD`是账号密码，**`STEP_MIN`必须小于`STEP_MAX`**，最后修改的步数为二者之间随机数

- 开启 tg 消息推送,需自行填入`TG_BOT_TOKEN` 和 `TG_USER_ID`

- 开启 qq 消息推送,需自行填入`TX_QQ` 和 `SEND_KEY`。文档见[Qmsg 酱 API 文档
  ](https://qmsg.zendee.cn/docs/api/)
- 默认开启随机步数 `STEP_MIN` 和 `STEP_MAX`，随机步数范围在`STEP_MIN`到`STEP_MAX`之间，默认为 10000-30000

确认一切无误就可以去`Actions`里`Run workflow`

#### GitHubAction 设置每日定时执行

直接修改[这个 yml 文件](/.github/workflows/action.yml)，把以下两句解除注释：

```
  schedule:
    - cron: '00 10 * * *'
```

修改里面的时间可以自己确定运行时间，要注意的是里面的数字指的是 UTC 时间，换算成北京时间要加 8h。

关于 GitHub Action 定时执行，请看[与此相关的 GitHub 官方文档](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)。
