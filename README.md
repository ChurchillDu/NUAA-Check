# Bug南航- i南航 自动打卡系统

---

关于想实现i南航自动打卡的艰难历程：

- http canary 抓包，勉强能看懂抓出来的是什么东西
- 学了学python，自己不会写，拿到别人写的轮子自己多少会用了
- 因为自己是重度telegram使用者，学会了如何把打卡结果转发到telegram，比微信可好用多了
![image](https://user-images.githubusercontent.com/62705137/133776485-1ecdc980-368a-4447-846c-88bfdabbd7b0.png)
- 了解了github action，看的不是太懂，但是好好用，直接省了一个服务器,amazing

----

正文分割线

## 使用方法
1. fork（就是整个页面右上角那个fork）本项目到自己的仓库
2. 在settings(对，就是上面一栏code issues最后一个，点进去左边找到secrets里面设置以下secrets,详见[参数配置](#canshu)
3. 提交一次，你可以删除本文档中任何一个字符然后提交一次（对就是文档右上角那个铅笔图标，点进去随便编辑点东西，然后有个commit changes，点他，剩下的全自动。

<h2 id="canshu">参数配置</h2>
student_id 学号  

password 密码  

sckey 在 [Server酱-发送消息](http://sc.ftqq.com/?c=code) 绑定微信找到SCKEY填入  

address XX省XX市（区）(XX县)XXX  

## 注意：
1. config.ini中所有的参数都是提交时提交上去的，默认全否，也就是不影响进校的最正常状态。
2. 如果您要修改打卡时间，请修改nuaa.yaml中的` - cron: '01 16 * * *'`,01代表分钟，16代表小时。请注时间是GMT时间，也就是比北京时间慢8个小时。
3. 程序设定每天00:01打卡，但是经过实际测试有很长延迟，可能为一小时左右

### 免责声明
本程序仅供学习参考，请在下载或fork后24小时内删除，否则后果自负！

