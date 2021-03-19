# Action-keepGV

GoogleVoice 全自动批量保号<br>
通过 GitHub Actions 定期向群内发送短信触发关键词，然后配置各gv号自动回复短信实现全自动保号。

# Usage

1.注册 GitHub，然后Fork本项目（顺便点个Star）
2.在[Groupme官网](https://groupme.com)注册一个账户，并激活主手机号。（建议用谷歌邮箱和对应gv号）
3.登录后新建一个群组，群名和介绍都用英文。手机打开 "Voice"或者"环聊Hangouts" App 就能看到这个群组（系统默认会发来一条消息，也可以手动发一条）（群建好后把所有的gv号加进去，就能实现批量给gv号群发短信）
4.在[GroupMe Dev](https://dev.groupme.com/bots)建立 bot 机器人。**group** 选刚建的群名； **name** 取英文；**callback URL** 输入`http://localhost`；其他留空。获得 Bot_ID 记下来。
5.继续在这个页面右上角点 **access token** 获得个人 API_KEY 记下来。
6.在你刚新建的 GitHub 项目里面点 **Settings**（设置）然后点 **Secrets**（隐私）新建`GM_BOT_ID`和`GM_API_KEY`分别对应前面的Bot_ID和API_KEY
7.在你刚建的 GitHub 项目里点 **Actions** 然后点左侧 **Autosend** 切换，然后点 **Run workflow** 开始第一次运行。运行成功你应该会收到 bot 的短信。 (看不到 Autosend 的话，点开 .yml 文件随便加一空行保存)
8.设置 Gmail 自动回复 GoogleVoice 短信，可以设定触发关键词为`keepGV`。（这一步网上很多教程）