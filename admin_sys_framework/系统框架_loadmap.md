#系统框架 roadmap

##目的

###1.能用（功能性）
现阶段：一些功能不支持
框架层面不支持的功能？

###2.好用（用户体验）
优化能用不好用的功能
1. 在老的框架里优化
2. 新建一个框架

###3.很有用（数据分析）
数据分析，帮助我们分析和改进

###4.more 代码迁移


##现状 不足之处
1. 登录 （循环重定向）
2. 使用不方便
3. 不支持一些业务实现
4. 权限判断问题
5. 城市
6. 接口调用 超时控制 【在页面告知用户&^接口速度慢】
7. 菜单问题

##steps

###第一阶段、新框架实现上线 1month

####1、backend 框架实现
1w
note：新开app

#####基本类
1. controller basic
2. bll basic
3. dao basic（继承新框架dao）
4. pager basic
5. component basic
6. data from service basic
7. auth basic （独立的类，不要只限于controller）

####2、frontend 协助  【不够详细】
1w todo
click热点收集（用于数据统计【不够详细】）
anglerjs + bootstrip + awsome + bigpip

####3、通用功能优化
1w

1）登陆 【循环重定向】
i. 循环重定向
ii. 登录验证漏洞
iii. 登录接口不稳定（需要加上监控，和java方商量优化方式）
iv. 登录后跳回到原来的页面

2）城市选择
（如果在单页，应该自动跳转到列表）
（优化所有单页）
方案一、统一的redirect url(list)： 只要发生城市变更，就跳到该url
方案二、进入单页后判断，确定是否跳转

####4、过渡方案
1）替换父类【测试功能】【重构代码】

====================================

###第二阶段、数据统计处理

####1、数据来源 （前段框架）【记录用户身份，如何实现，log？】

- 页面访问量 (access log)
- 页面停留时间(component ， load, unload)
- 页面区域热点(button、输入框、form各种元素) 


####2、储存
db

####3、使用
i. 页面访问量、页面停留时间 =》 哪些页面是最重要
ii. 页面热点图  =》重要的页面分析 【开源工具】

====================================

###第三阶段、代码迁移 ？

迁移？【这个工作量很大】
