# StepNumberChangeSNC

## action 运行

使用本仓库需要 Zepp Life app（_原小米运动 app_），请务必把 Zepp Life 注册好，设置好，与微信的同步/第三方接入什么的都弄好再往下看

<p align="right">（<a href="#修改微信运动步数">回到顶部</a>）</p>
  
## 使用指南
### 通过GithubAction
   1. Fork 本仓库
   2. 在你自己 Fork 的仓库进行设置`Settings - Actions - General - Allow all actions and reusable workflows`，别忘了`save`
   3. 然后`Settings - Secrets - Actions - New repository secret`，按下面例子新建几个`secrets`：

   <table>
    <tr>
     <td>Name</td>
     <td>Value</td>
    </tr>
    <tr>
     <td>USER_PHONE</td>
     <td>18899996666</td>
    </tr>
    <tr>
     <td>USER_PWD</td>
     <td>abc123</td>
    </tr>
    <tr>
     <td>STEP</td>
     <td>10000</td>
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
   </table>
   
   （`USER_PHONE`是注册Zepp Life app的手机号，`USER_PWD`是账号密码，**`STEP_MIN`必须小于`STEP_MAX`**，最后修改的步数为二者之间随机数）
   
   确认一切无误就可以去`Actions`里`Run workflow`

<p align="right">（<a href="#修改微信运动步数">回到顶部</a>）</p>
  
#### GitHubAction设置每日定时执行
直接修改[这个yml文件](/.github/workflows/action.yml)，把以下两句解除注释：

```
  schedule:
    - cron: '00 10 * * *'
```

修改里面的时间可以自己确定运行时间，要注意的是里面的数字指的是 UTC 时间，换算成北京时间要加 8h。

关于 GitHub Action 定时执行，请看[与此相关的 GitHub 官方文档](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)。
