# 一个简陋的微信新型冠状病毒疫情实时播报/查询机器人

感谢以下两个项目提供的API接口

- 微信机器人项目：https://github.com/Mocha-L/WechatPCAPI

- 2019新型冠状病毒疫情实时爬虫https://github.com/BlankerL/DXY-2019-nCoV-Crawler



特殊时期为了阻止家里长辈到处串门溜达...故写了个简陋的机器人自动往家里的群发送最新的疫情信息，潜移默化的改变他们的想法，效果确实不错hhh，成功达成目标



# 可以用来干什么

- 自动推送最新疫情消息给微信列表的所有人/群
- 自动回复省份地区确诊/疑似/治愈/死亡的查询请求



# 怎么用

##  运行

运行管理员模式下test.py即可，微信有版本限制，安装包在/src中



## 使用方法

查询数据是通过关键字查询的：

- 查询全国数据：/virus
- 查询省份数据，中间用空格隔开（如果没有数据会返回未查到数据）：/virus <省份>
- 查询城市数据，中间用空格隔开（如果没有数据会返回未查到数据）：/virus <省份> <城市>
- 查询省份所有数据，中间用空格隔开：/virusall <省份>

每120s会通过api获取最新的疫情新闻，如果有新的新闻则会推送给列表里面的所有好友和群



# 注意事项

20200204微信被封号，应该是和自动推送新闻有关，故代码默认将自动推送新闻的部分注释，谨慎开启
