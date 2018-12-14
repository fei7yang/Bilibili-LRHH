# Bilibili直播间挂机助手/Bilibili-LRHH/BLRHH

![ECMAScript 5](https://img.shields.io/badge/ECMAScript_5-unsupport-red.svg?longCache=true) ![ECMAScript 6](https://img.shields.io/badge/ECMAScript_6-pass-green.svg?longCache=true) ![TamperMonkey 4.8](https://img.shields.io/badge/TamperMonkey_4.8-pass-green.svg?longCache=true) ![Chromium 69](https://img.shields.io/badge/Chromium_69-pass-green.svg?longCache=true) ![Firefox 63](https://img.shields.io/badge/Firefox_63-pass-green.svg?longCache=true) [![Issues](https://img.shields.io/github/issues/SeaLoong/Bilibili-LRHH.svg)](https://github.com/SeaLoong/Bilibili-LRHH/issues)

> 该脚本为TamperMonkey脚本，只在该环境下测试通过，使用其它脚本插件来加载此脚本的，不能保证正常运行  
> 当脚本无法正常运行时，请把广告拦截插件关闭后重试

-----------------

## 如何使用
1. 见[GreasyFork](https://greasyfork.org/zh-CN) 首页说明
2. 进入[Bilibili直播间挂机助手](https://greasyfork.org/zh-CN/scripts/37095-bilibili%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B)页面，点击"安装此脚本"即可从GreasyFork更新此脚本
3. 或者点击[Bilibili直播间挂机助手](https://raw.githubusercontent.com/SeaLoong/Bilibili-LRHH/master/Bilibili%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B.js)，将代码复制下来。然后从脚本管理器中新建一个脚本，将自动生成的内容删除，粘贴复制的代码即可从Github更新此脚本
4. 进入直播间页面，右下角多出个"挂机助手设置"，选择自己需要的功能，保存刷新即可

-----------------

## 已实现功能
+ 自动签到
+ 自动领取银瓜子
+ 自动应援团签到
+ 移动端心跳
+ 自动抽奖
  + 礼物抽奖
  + 舰队领奖
  + 实物抽奖
+ 自动完成任务
+ 自动送礼物
+ 自动每日奖励
+ 银瓜子换硬币

-----------------

## 说明
+ 自动抽奖功能大多是基于广播的，如果广播不会通知(比如其他房间的舰长)，则不会参加对应的抽奖

-----------------

## 常见问题
1. OCRAD初始化失败/脚本需要加载很久/不能正常使用
    + 尝试替换脚本require源
    + 在代码中找到以下几段代码中的一段，替换为其他的一段，然后刷新页面试试
     ```js
    [greasyfork源]
    // @require      https://greasyfork.org/scripts/38140-bilibiliapi/code/BilibiliAPI.js
    // @require      https://greasyfork.org/scripts/44866-ocrad/code/OCRAD.js
    [github源]
    // @require      https://raw.githubusercontent.com/SeaLoong/Bilibili-LRHH/master/BilibiliAPI.js
    // @require      https://raw.githubusercontent.com/SeaLoong/Bilibili-LRHH/master/OCRAD.min.js
    [gitee源]
    // @require      https://gitee.com/SeaLoong/Bilibili-LRHH/raw/master/BilibiliAPI.js
    // @require      https://gitee.com/SeaLoong/Bilibili-LRHH/raw/master/OCRAD.min.js
    [腾讯云源]
    // @require      https://js-1258131272.file.myqcloud.com/BilibiliAPI-1.3.4.js
    // @require      https://js-1258131272.file.myqcloud.com/OCRAD.min.js
    ```
2. 开启自动抽奖后，直播间页面经常崩溃
    + 在设置中找到"刷新间隔"，设置为一个合适的数值
    + 这个情况目前暂无更好的解决方法
3. 可以领取瓜子却显示"今日已领完"
    + 我也不知道啊QWQ，清理下缓存试试
4. 自动抽奖功能不能正常运行
    + 关闭广告拦截插件试试
5. 脚本显示完成了每日经验奖励，但个人中心显示未完成
    + 正常现象，过段时间就会正常显示了

-----------------

## 注意事项/关于反馈
    开启自动抽奖->礼物抽奖功能后，很容易在控制台看到许多Error，这些大多是B站的脚本错误，不用理会
    要检索此脚本的控制台输出只要过滤显示带有"[BLRHH]"字样的输出即可
    在脚本代码中找到有关"DEBUGMODE"的地方，将其设置为true可在控制台输出调试信息，反馈(包括bug、B站更新等)时请带上有关信息

-----------------

## 捐赠作者

+ 支付宝 => ![支付宝二维码](https://i.loli.net/2018/11/05/5be02cd439623.png) 微信 => ![微信二维码](https://i.loli.net/2018/10/30/5bd867645d5b4.png)

-----------------

## 许可证
[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?longCache=true)](https://github.com/SeaLoong/Bilibili-LRHH/blob/master/LICENSE)

-----------------

## 更新日志
> ###  2018-12-4 (Version 2.3.3)
> ###  2018-12-1 (Version 2.3.2)
> ###  2018-11-27 (Version 2.3.1)
>     修复了一些逻辑问题
> ###  2018-11-26 (Version 2.3.0)
>     修复了应援团签到不能正常使用的问题
>     增加了自动完成每日奖励任务的功能
> ###  2018-11-10 (Version 2.2.6)
> ###  2018-11-10 (Version 2.2.5)
>     增加了自动抽奖的内置延迟
>     增加了对自动送礼功能的限制
> ###  2018-11-07 (Version 2.2.4)
> ###  2018-11-05 (Version 2.2.3)
>     修复了有时出现抽奖参数不正确的问题
> ###  2018-11-04 (Version 2.2.2)
>     优化了代码逻辑
>     修复了重复抽奖的问题
> ###  2018-11-03 (Version 2.2.1)
>     修复了舰队领奖不能正常工作的问题
>     增加了自定义监听房间数的功能
>     优化了代码逻辑
> ###  2018-11-03 (Version 2.2.0)
>     修改了自动抽奖->礼物抽奖的参与方式
>     修改了自动抽奖->舰队领奖的参与方式
>     移除了部分设置项及其功能
> ###  2018-11-01 (Version 2.1.3)
>     修复了不能礼物抽奖的问题
> ###  2018-11-01 (Version 2.1.2)
>     修复了舰队领奖有时候会疯狂重试的问题
> ###  2018-10-31 (Version 2.1.1)
>     修复了脚本可以在多个直播间页面运行的问题
>     修复了舰长奖励无法领取的问题
> ###  2018-10-30 (Version 2.1.0)
>     优化了重试机制
>     增加了对四大分区都监听的功能
>     (可能)修复了一些奇怪的bug
> ###  2018-09-28 (Version 2.0.12)
>     修改和移除了部分设置项
>     提高了使用稳定性
> ###  2018-08-26 (Version 2.0.11)
>     修复了在有实物抽奖的直播间不能运行脚本的问题
> ###  2018-08-21 (Version 2.0.10)
>     增加了对超时情况的处理
>     调整了部分代码逻辑以保证功能的持续运行
> ###  2018-08-17 (Version 2.0.9)
>     调整了实物抽奖代码逻辑
> ###  2018-08-13 (Version 2.0.8)
>     调整了一小部分代码
> ###  2018-08-09 (Version 2.0.7)
>     增加了自动刷新页面的功能
>     增加了只允许单个直播间页面的脚本运行的功能
> ###  2018-08-08 (Version 2.0.6)
>     修复了自动领取瓜子有时候会停止不领取的逻辑问题
>     修复了自动抽奖->实物抽奖有时候会疯狂访问接口的问题
>     移除了银瓜子换硬币的旧接口及其设置项
> ###  2018-08-05 (Version 2.0.5)
>     修复了"防止自动完成任务、自动送礼在同日/同时间段多次运行的功能"无效的问题
>     修复了在当日银瓜子领取完后，再次运行脚本后，自动领取银瓜子界面会显示"自动领取中"的问题
> ###  2018-08-05 (Version 2.0.4)
>     增加了防止自动签到、自动应援团签到、银瓜子换硬币、自动完成任务、自动送礼在同日/同时间段多次运行的功能
> ###  2018-08-04 (Version 2.0.3)
>     修复了自动抽奖部分设置项无效的问题
> ###  2018-08-03 (Version 2.0.2)
>     修复了自动抽奖->礼物抽奖在运行时会出现其他直播间声音的问题
>     优化了自动抽奖->礼物抽奖的参与方式
> ###  2018-08-03 (Version 2.0.1)
>     优化了自动抽奖->礼物抽奖的参与方式
>     增加了移动端心跳5分钟后自动进行一次完成任务的功能
>     修复了自动送礼不能持续运行的问题
>     增加了保存设置时会自动修正设置的功能
> ###  2018-08-02 (Version 2.0.0)
>     增加了自动应援团签到的功能
>     增加了移动端心跳的功能(可配合自动完成任务来完成双端观看)
>     增加了银瓜子换硬币的旧API兑换功能
>     增加了自动抽奖->总督领奖的功能
>     增加了自动抽奖->实物抽奖的功能
>     重新命名了自动抽奖功能，现为自动抽奖->礼物抽奖功能
>     增加了自动抽奖->礼物抽奖的自定义设置
>     修改了自动抽奖->礼物抽奖的检测方式
>     修改了自动抽奖->礼物抽奖的参与方式
>     降低了自动抽奖->礼物抽奖功能的内存占用
>     调整了浮动提示的位置
>     优化了设置界面的生成方式
>     移除了未实现的节奏风暴代码部分
>     在GreasyFork上恢复脚本
> ### 2018-05-19
>     更新API，优化代码，第二次尝试规避封号
> ### 2018-05-12
>     更新API相关，优化逻辑，尝试规避封号
> ### 2018-04-30
>     更新验证码识别算法，修复无法正常领取瓜子的问题
>     增加新的设置项
> ### 2018-03-31
>     更新总督API相关(缺少数据,功能未实装)
> ### 2018-03-10
>     在Github上创建脚本仓库
>     更新领取银瓜子的功能
> ### 2018-02-15
>     修正了节奏风暴有关功能的实现逻辑
>     在GreasyFork上删除脚本
> ### 2018-02-12
>     解决了不能在任意直播间参加抽奖的问题(实验性)(需在设置中勾选)
> ### 2018-02-10
>     修复了不能领取银瓜子的问题
> ### 2018-02-04
>     增加了银瓜子兑换硬币的功能
>     修改了默认设置
>     调整了设置界面的位置
> ### 2018-01-28
>     调整了设置界面
>     修改了送礼逻辑
> ### 2018-01-22
>     增加了可视设置界面和保存设置的功能
>     增加了新的设置项
>     移除了使用银瓜子送礼的功能
>     修复了会自动送出永久期限礼物的bug(未测试)
>     优化了领取瓜子信息的界面设计
>     优化了抽奖计时逻辑
> ### 2018-01-20
>     优化了抽奖功能，调整了浮动提示
> ### 2018-01-18
>     修复了不能正常参加新春抽奖的问题
> ### 2018-01-13
>     修复了领取宝箱的有关bug
> ### 2018-01-12
>     增加了自定义送礼等功能，优化了脚本逻辑
> ### 2018-01-09
>     修复了脚本不能运行的问题
> ### 2018-01-06
>     在GreasyFork上创建脚本

-----------------