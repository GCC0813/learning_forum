# learning_forum
<a>learning_forum是基于Java的论坛系统。前端使用Html+CSS+JS实现，后端使用Java语言开发，技术栈包括但不限于Spring/SpringMVC/SpringBoot、MyBatis、Redis、PageHelper、MySQL、Maven等，开发工具为Eclipse。</a>

# 功能
1、登录和注册<br>
2、（分类）浏览话题<br>
3、发表话题<br>
4、上传照片<br>
5、评论以及评论赞踩<br>
6、站内信通知<br>
7、用户积分排行榜<br>
8、关注和共同关注<br>

# 主要功能实现
1、登录注册：使用SpringSecurity4框架，即使用已经包装好的接口来实现，简单易用。<br>
2、上传照片：照片是存储在第三方服务器，即七牛云。<br>
3、站内信通知：通过异步队列来实现的站内信通知，其中选择Redis来作为队列。<br>
4、排行榜：排行榜是通过Redis的有序集合来实现的，可以快速实现topK排序。<br>
5、关注和共同关注：通过Redis的集合数据结构实现。<br>


备注：
1、本项目的Redis已经换成集群了，本地跑的时候先建立集群，否则自行将集群换成单机Redis，具体修改application.propertie和com.xzp.forum.util.JedisAdapter.java即可（再具体如何修改可以参考提交记录或联系我~）

2、因项目中七牛云过期了，上传的所有照片都失效了，所以项目中有照片的都被和谐了~

