# | AutoAnimeMV:超轻量化快速部署看番遥遥领先！
<p align="center">
  <a href="https://github.com/Abcuders/AutoAnimeMV">
    <img src="https://github.com/Abcuders/AutoAnimeMV/blob/main/Image/logo.png">
  </a>
<p>

***
[![ GitHub 许可证](https://img.shields.io/github/license/Abcuders/AutoAnimeMv)](https://github.com/Abcuders/AutoCartoonMv/LICENSE) [![GitHub release](https://img.shields.io/github/v/release/Abcuders/AutoAnimeMv)](https://github.com/Abcuders/AutoAnimeMv/releases/)

> 😊这是一个番剧自动识别剧名剧集+自动重命名+自动整理工具,用来配合QBittorrent实现Rss订阅下载全自动刮削一条龙到家式爽歪歪服务!
 
 **本工具现在支持Linux🐧和Windowsℹ️了👏👏👏**

# 🏕️ 环境支持
***
要使用本工具您必须需要`🐍Python3环境`支持，我们建议您搭配`🔵Qbittorrent`使用

# 💡 帮助&提醒
 ***
 * **`🐍Python3环境`**:您可以在[🐍Python官网](https://www.python.org/downloads/windows/)下载合适的版本进行安装,我们建议安装3.9及以上的版本
   >  🐍Python使用的依赖库:`sys` `os` `time` `re`
   以上依赖应该不需要您进行安装
 * 如果您直接使用pip进行install遇到 `❗Fatal error in launcher: Unable to create process using pip问题` ,请使用`python3 -m pip install`
## 🕹️ 工具的处理逻辑
***
开始Run之后会进行自动识别视频文件格式、番剧剧集、截断文件名、去除无效文字、剔除字幕组、保留剧名剧季，并将视频文件重命名为`S01E剧集.文件格式`再移至`下载路径` 下的`剧名\Season_剧季`文件夹（如果没有则会自动创建）就像下面一样:
```
[ANi] 无神世界的神明活动（仅限港澳台地区） - 01 [1080P][Bilibili][WEB-DL][AAC AVC][CHT CHS][MP4].MP4
>>无神世界的神明活动/Season_01/S01E01.mp4
```
> 我们将 判断是否属于`动漫分类功能注释了，现在它是一个可选功能，您可以根据不同的类型设置不同的Video保存路径

## 📻 常见问题建议
***
* 在群晖NAS中，套件中心安装的`🐍python3`环境可能出现奇奇怪怪的问题，请使用第三方套件源(第三方源需要手动为`🐍python3`创建软连接至/usr/local/bin/python3)

* 如果你使用的是群晖NAS `🐳Docker`版的`🔵QBitTorrent`,你可以在容器日志中直接看到`AutoCartoonMv.py`输出的日志信息
  
# 📝 使用方法 
***
 > `AutoCartoonMv.py`需要三个参数,`下载路径` `下载文件名` `文件分类`(可选) 
## 使用场景1-配合NAS Qbittorrent进行使用
  * 1.将`AutoCartoonMv.py`上传至`🔵QBittorrent`能访问的路径下
  
  * 2.在`🔵Qbittorrent`中创建`动漫`分类(非必须，你想要用什么名字都可以，去修改`AutoCartoonMv.py`中的判断即可，当然不要分类也可以)

  * 3.修改qb配置: `下载`勾选 `Torrent 完成时运行外部程序`, 下面填上(传入参数顺序不可更改)
  
    ```
    python3 AutoCartoonMv.py放置路径 下载路径 下载文件名 文件分类
    ```
    上面三个参数可以由`🔵Qbittorrent`传入，即
    ```
    python3 AutoCartoonMv.py放置路径 "%D" "%N" "%L"
    ```
  * 4.取消做种，修改qb配置: 将`🔵QBitTorrent `的`做种限制`改成`当分享率达到0当做种时间达到0分钟然后暂停torrent`

  * 5.现在你就可以下载一个番剧测试效果啦
    > 🚩举例，下面的文件名字都可以被识别`[Comicat][Jigokuraku][01][1080P][GB&JP][MP4].mp4` 
  
    >`【悠哈璃羽字幕社】[虚构推理_Kyokou Suiri ][09][x264 1080p][CHT].mp4`
  
    >` [桜都字幕组] 因为太怕痛就全点防御力了。第2季/ Itai No Wa Iya Nano De Bougyoryoku Ni Kyokufuri Shitai To Omoimasu. S2 [10][ 1080P@60FPS ][简繁内封].mp4`
  
    > 或者是带有干扰项的 `【喵萌奶茶屋】★01月新番★[英雄王，为了穷尽武道而转生～然后，成为世界最强的见习骑士♀～ / Eiyuuou, Bu wo Kiwameru Tame Tenseisu][10][720p][简体][招募翻译].mp4`

  # 🧉 BB一下
***
* 23/5/26:下周我推要播总集篇，每周的精神食粮要断粮了😭😭没有你我怎么活呀，燕子！
* ⚠️本程序显然存在诸多问题，在此恳请各位大佬不吝赐教


# 🧾 声明
***
**该仅供个人合法用途,任何使用该工具进行直接或者间接非法盈利活动的行为,均不属于授权范围,也不受到任何支持和认可**
