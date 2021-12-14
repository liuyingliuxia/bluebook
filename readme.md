# Bluebook（蓝宝书）

Bluebook 是一款开源自由的协作管理工具，采用 Node.js 开发。  
数据表设计精简，内部核心7张表，外部核心4张表，代码优美简洁，易拆分，扩展性强。

对内采用计划经济，投票决定事项，按需分配。  
对外保留市场经济的接口，允许生产团队对外倾销和购买生产资料。

基本操作流程是：

+ 需求团队/个人发起任务单，填写预估数量
+ 需求团队进行投票表决，填写需求数量
+ 生产团队进行投票表决，填写计划数量
+ 物料生产/任务进行中，完成后填写实际数量
+ 物料分配中，用户领取并填写反馈信息
+ 任务结束，有生产剩余的部分进入外部倾销阶段
+ 系统随机在生产团队内选取至少两名用户进行销售工作
+ 销售货款打入生产团队账户
+ 销售货款平均分配给生产团队成员，按团队设定的数值确定保留在团队内的比例（默认是 0）
+ 任务结束

关于投票，团队可以设置任务自动通过的百分比值，默认是 50%。  
团队管理员具有一票否决权，保证了任务的科学性，然后同时也加入了排除管理员重新表决，达到 90%（也可以设置）则继续进行的民主机制（称为反否阈值）。

目前项目还在初始阶段，只有基础框架，但架构上已经可以轻松愉悦地搬砖了。  
关于数据表的信息，可以在[这里](control/app_init.js)查看，有完善的注释。

目前 ui 还不完善，但已经实现了基本可看的响应式设计，从宽屏到手机丝滑切换，从5列到两列都有合适的显示和操作逻辑。  
可以下载模板单页以进行操作预览：[首页](theme/default/index_preview.html) / [登录页](theme/default/login_preview.html)，图片预览和详细流程在[这里](https://github.com/gearkey/bluebook_doc)可以查阅。

当前的工作计划：

+ 写完一些基础逻辑
+ 确定主题和模块模板，并征求开发
+ 开发内置扩展模块

设计的核心思路是在团队内将一般等价物由货币改为时间，目前看起来还是很美好的。  
大体是生产过剩的问题被解决，化劣势为优势，个人和团队自由组合，分散式的投票制，有兴趣的加群 805567091 。

## 软件依赖模块

涉及到数据库的基本操作、主题模板的渲染，所以需要以下依赖：

```
npm install mysql --save
npm install art-template --save
```

最后，祝玩得开心。

## 更新日志

采用 npm 推荐的版本号形式。

```
v0.1.0-20211212：基本框架的建立
v0.1.1-20211213：现在模板可以跑起来了
```

## 截图预览

![0-当前基本预览.png](https://disk.vvnote.org/gearkey/post-285/1.png)

