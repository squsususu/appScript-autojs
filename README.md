# autojs

> android autojs 签到类脚本

## NEW

- **今日校园**打卡
- **飞猪**里程
- **京东**京豆
- **简书**抽奖转盘
- **口袋梦三国**签到
- **哔哩哔哩**签到
- **支付宝**签到积分
- **淘宝**每日签到
- **QQ 音乐**签到
- **百度地图**签到
- **饿了么**签到
- **拼多多**签到
- **起点读书**签到
- **网易云音乐**签到

### 说明

脚本主要用于签到类自动处理

- 百度地图签到
- 大众点评签到
- 叮咚买菜签到
- 飞猪签到里程
- 京东签到京豆
- 京东金融签到钢镚
- 联想签到延保
- 拼多多签到
- 上海移动和你签到
- 什么值得买签到
- 苏宁易购签到
- 淘宝签到淘金币
- 腾讯 wifi 管家签到
- 微信读书(TODO)
- 小米商城抢购 web(TODO)
- 新浪微博早起打卡(TODO)
- 云闪付签到积分
- 支付宝签到积分
- 支付宝每日花呗红包
- 支付宝体育服务早期打卡(TODO)

### TODO

1. 添加早起打卡类应用
2. 添加秒杀类应用(例如京东话费券，具体领券页面需要参考"券老大""券妈妈"等 APP )
3. 对于无法通过 id\text\desc 找到控件的, 使用找图方式 click(posX, posY)等点击位置写死的 ==> 截图找图定位
4. 当指定控件\文字\id 不存在时，后续的延时操作取消
5. 分享到微信"文件传输助手"创建单独方法便于调用
6. APP 更新较快，可能导致脚本失效，为脚本增加超时处理(Maid.js 中增加)，防止某一脚本一致运行导致耗电
7. 判断处理是否成功(通过以下方式判断：如弹出框文字\弹出成功图层\积分增加\跳转成功页面)
8. 在可以判断处理是否成功的前提下，写入日志，后续通过展示日志图表快速预览所有任务情况

### other

1. 目前所使用机型[魅族 16x][1080 x 2160][开发者选项中最小宽度设值 380]
2. 如果要通过 shell 直接运行脚本：

```bash
am start -n org.autojs.autojs/.external.open.RunIntentActivity -d file:///storage/emulated/0/脚本/大众点评-签到.js -t text/javascript
```

3. autojs 自带定时功能可靠性较差，因此使用 tasker 处理[autojs.prj.xml]
4. 编写代码[代码尽量在 PC 端 vscode 中编写，使用 Auto.js-VSCodeExt 插件调试脚本，使用 xftp 同步到手机端]
5. 执行任务在半夜；白天使用手机时，可以在[最近任务面板]查看任务是否执行成功(最好关闭最近任务模糊效果, 如支付宝, 便于验证查看)
