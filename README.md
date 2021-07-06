# Fuck Daily CP

## 🏆原作者及贡献者

[**Finch**](https://gitee.com/Finch1)

[**0x0**](https://gitee.com/xsw0)

[**柠火**](https://gitee.com/lemofire)

### 🌈简介

今日校园自动打卡脚本（不局限于健康打卡，包括收集表，通知确认）。

可以挂服务器上定时自动打卡。     

健康的人可以用一下（雾）。

![img](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//img.png)

### 🎈说明‼

* 理论上支持大部分学校（学号登录）和任意表单内容的自定义。

* **运行程序之前，请务必修改文件内的 `JSON` 文件** ❗❗❗

* 因为表单的内容多种多样，不可能共享给其他人使用，因此本脚本采用 “一次编辑，永久使用” 的思路（当然不排除导员更换了通知内容🐶）。

### 🍕食用方法

使用 `Github Action` 自动提交 **辅导员通知**

1. 在 `Github` 中 `Fork` 本仓库

![image-20210219161433765](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219161433765.png)

2. `Fork` 完成后，点击 `Settings` ，增加 `SCHOOL_NAME` 、 `ACCOUNT` 、 `PASSWORD` 、 `ADDRESS` 、`SCKEY` 共计 5 个 `Secrets`，分别对应你的**学校名称**(中文名全称)、**账号**、**密码**、**定位地址** 、 **[Server酱SCKEY](http://sc.ftqq.com/)**。

   ![image-20210219161928451](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219161928451.png)

3. **运行之前请务必删除 `formdb` 目录下 `79d6c...31b7acfa.json` 文件。**

![image-20210219163416535](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219163416535.png)

4. 依次点击`Actions` — `I understand ...` — `Enable workflow`

![image-20210219164821807](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219164821807.png)

![image-20210219165033296](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219165033296.png)

直至如图所示即可。

![image-20210219165110229](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219165110229.png)

5. 因为表单的内容多种多样，第一次运行需查看`GithubAction`运行详情，在`py`函数中我已经让程序输出`newForm`的`json`信息。用户需按照本`Github Action`的第一次执行结果在`formdb`文件夹下创建要求的`json`文件。

![image-20210219165626811](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210219165626811.png)

> 在此处我遇到很多问题，有几点需要提醒一下食用者们：
>
> * 要求创建的`json`文件内容务必和程序输出`newForm`内容一致。
> * 创建的`json`文件必须以自身情况进行填写，填写要求请参考`formdb`文件内`1129.json`与`1130.json`文件。
> * 创建的文件必须是`json`格式，不得有语法错误，例如
>   * 英文单引号必须转为英文双引号；
>   * `True`必须改为`true`;
>   * `None`必须改为`null`
>   * ……

6. 选择以下任一方式运行此`Action`项目。
   * 1.`push`
   * 2.自己给自己 `Star`
   * 3.每日 `11:00` 和`12:00` 分别自动运行一次

### 🎨效果截图

![image-20210220102213315](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210220102213315.png)

![image-20210220102338192](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210220102338192.png)

![image-20210220102137421](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//image-20210220102137421.png)

![img](https://gitee.com/bai_xiao_fei/picture/raw/master/pic//005AJQBUly1gnsvztwecsj31hc0qa0y2.jpg)

### 🎉后记

本项目版权归属其Gitee作者，如有侵权立删。本项目在原作品上增加了打印 **辅导员通知** 的`json`信息以及 **serve酱** 微信提醒。

- 如果你平时更喜欢使用QQ，你可以尝试接入**Qmsg酱** 进行QQ消息提醒。

- 如果你是新手，就按照本教程一步一步进行操作。

- 如果你熟悉python，你可以尝试自己魔改。
