# Flask 课程

1. 第1章 课程导语
 1-1 开宗明义试看
 1-2 课程维护与提问

2. 第2章 Flask的基本原理与核心知识
本章我们首先介绍Python官方推荐的最佳包与虚拟环境管理工具：Pipenv。接着我们来学习唯一URL原则、重定向、响应对象Response。

 2-1 鱼书是一个什么样的产品试看
 2-2 准备工作试看
 2-3 使用官方推荐的pipenv创建虚拟环境（很好用哦~）
 2-4 开发工具推荐
 2-5 设置开发工具的默认解释器
 2-6 flask最小原型与唯一URL原则
 2-7 路由的另一种注册方法
 2-8 app.run相关参数与flask配置文件
 2-9 你并没有真正理解 if __name__的作用
 2-10 响应对象：Response

3. 第3章 数据与flask路由
本章我们重点探讨数据获取、视图函数的编写规范、flask的路由原理（深入源码）。此外我们还将讲解常见的Python应用误区，比如循环导入所造成的问题。

 3-1 搜索而不是拍照上传
 3-2 书籍搜索与查询 1-数据API
 3-3 书籍搜索与查询 2-搜索关键字
 3-4 书籍搜索与查询 3-简单的重构
 3-5 获取书籍数据：调用鱼书API
 3-6 requests vs urllib
 3-7 从API获取数据
 3-8 使用jsonify
 3-9 将视图函数拆分到单独的文件中
 3-10 深入了解flask路由
 3-11 循环引入流程分析

4. 第4章 蓝图、模型与CodeFirst
本章我们尝试把单文件的flask重构为具有模块意义的分文件模型，接着我们会探讨如何使用CodeFirst的思想来创建数据库表。

 4-1 应用、蓝图与视图函数
 4-2 用蓝图注册视图函数
 4-3 单蓝图多模块拆分视图函数
 4-4 request 对象
 4-5 WTForms参数验证
 4-6 拆分配置文件
 4-7 Model First、Database First与Code First
 4-8 定义第一个模型类
 4-9 将模型映射到数据库中
 4-10 ORM与CodeFirst区别

5. 第5章 flask核心机制
flask最核心的是两个上下文，而这两个上下中包含大量的Python高级编程应用。我们需要理解上下文的意义，并且通过借鉴flask的下文机制，学习Python的上下文管理器（With）、栈结构的应用。我们还将学习，到底如何通过阅读源码来解决问题。...

 5-1 flask中经典错误 working outside application context
 5-2 AppContext、RequestContext、Flask与Request之间的关系
 5-3 详解flask上下文与出入栈
 5-4 flask上下文与with语句
 5-5 详解上下文管理器的__exit__方法
 5-6 阅读源码解决db.create_all的问题


6. 第6章 Flask中的多线程与线程隔离技术
对于Web，多线程是难以避免的。本章节，我们将借助flask的原理来学习进程、线程、什么是线程安全、什么又是线程隔离、如何在Python中实现线程隔离、LocalStack机制又是什么。学完本章，你将理解为什么由于GIL（全局解释器锁）的存在，Python的多线程依然是有意义的。...

 6-1 什么是进程
 6-2 线程的概念
 6-3 多线程
 6-4 多线程的优势与好处
 6-5 全局解释器锁GIL
 6-6 对于IO密集型程序，多线程是有意义的
 6-7 开启flask多线程所带来的问题
 6-8 线程隔离
 6-9 Flask中的线程隔离对象Local
 6-10 Flask 中的线程隔离栈：LocalStack
 6-11 LocalStack作为-Stack-的基本用法
 6-12 LocalStack作为线程隔离对象的意义
 6-13 flask中被线程隔离的对象
 6-14 梳理串接flask的一些名词

7. 第7章 书籍详情页面的构建（ViewModel、面向对象与重构）
本章我们提出一个概念ViewModel，并详细解释ViewModel的意义。此外面向对象虽然是老生常谈，但你真的理解面向对象吗？我们将在本章中通过重构来一步步揭示到底什么才是对象，如何写出面向对象的代码来。思维的训练，永远比业务要重要。...

 7-1 ViewModel的基本概念
 7-2 使用ViewModel处理书籍数据 上
 7-3 使用ViewModel处理书籍数据 下
 7-4 伪面向对象：披着面向对象外衣的面向过程
 7-5 重构鱼书核心对象：YuShuBook 上
 7-6 重构鱼书核心对象：YuShuBook 下
 7-7 从json序列化看代码解释权反转
 7-8 详解单页面与网站的区别

8. 第8章 静态文件、模板、消息闪现与Jinja2
本章，我们将通过借助学习flask的模板来间接学习：列表推导式的应用、三元表达式的应用、@Property属性描述符、filter函数的应用、管道过滤器。这些知识我们虽然在入门与进阶课程中学习过，但是他们到底如何使用？这是个问题。我们本章将一一解释。...

 8-1 静态文件访问原理
 8-2 模板文件的位置与修改方案_x264
 8-3 Jinja2的概念
 8-4 在Jinja2中读取字典和对象
 8-5 流程控制语句 if
 8-6 流程控制语句 for in 循环
 8-7 使用模板继承
 8-8 过滤器与管道命令
 8-9 反向构建URL
 8-10 消息闪现、SecretyKey与变量作用域
 8-11 显示搜索结果页面
 8-12 页面结构解析

9. 第9章 用户登录与注册
本章我们通过使用flask-login这个插件来处理用户的登录与注册。同时我们将借助登录与注册来学习Flask中的Cookie、重定向、与重定向的隐患：重定向攻击。此外，我们还会介绍Python的getter与setter的妙用。

 9-1 viewmodel意义的体现与filter函数的巧妙应用
 9-2 书籍详情页面业务逻辑分析
 9-3 实现书籍详情页面
 9-4 模型与模型关系
 9-5 自定义基类模型
 9-6 用户注册
 9-7 Python的动态赋值
 9-8 Python属性描述符实现getter与setter
 9-9 ORM的方式保存模型
 9-10 自定义验证器
 9-11 redirect重定向
 9-12 cookie
 9-13 cookie的应用
 9-14 login_user 将用户信息写入cookie
 9-15 访问权限控制
 9-16 重定向攻击

10. 第10章 书籍交易模型（数据库事务、重写Flask中的对象）
本章是一个综合应用章节。我们将看到如何使用多个Python的知识点综合解决问题。我们将进一步的使用@contextmanager来改善前面所学到的上下文管理器，并结合yield来优化数据库事务。此外，我们还将重写Flask中的一些对象的方法，来实现我们自己的业务逻辑。...

 10-1 鱼豆
 10-2 思维逻辑锻炼
 10-3 事务与回滚
 10-4 Python @contextmanager
 10-5 灵活使用@contextmanager
 10-6 结合继承、yield、contextmanager、rollback来解决问题
 10-7 类变量的陷阱
 10-8 合理使用ajax
 10-9 书籍交易视图模型
 10-10 处理时间
 10-11 书籍详情页面
 10-12 再谈MVC中的Model
 10-13 重写filter_by

11. 第11章 鱼书业务处理

本章我们将使用前面所学习的Flask与Python知识集中处理我们的业务。包括：最近上传的图书（首页）、礼物清单与赠送清单、鱼漂与个人中心等。

 11-1 最近的礼物（复杂SQL的编写方案）
 11-2 链式调用
 11-3 完成最近的礼物（业务的四种编写方案）
 11-4 我的礼物 一 （使用db.session和filter做查询）
 11-5 我的礼物 二（group_by与funct.count统计联合使用）
 11-6 我的礼物 三 (不要在函数中返回元组，而应该返回字典)
 11-7 我的礼物 四
 11-8 用户注销
 11-9 我的心愿 一
 11-10 我的心愿 二 （再谈循环导入的解决方案）
 11-11 我的心愿 三 (谈谈重复代码的封装技巧）

12. 第12章 Python与Flask的结合应用
在《Python3入门与进阶》中我们详细讲解了装饰器，但是装饰器到底应该怎么用？本章将通过使用带参数的高级装饰器来实现邮件发送的频率限制。同时我们将分析SQLAlchemy中的多继承特性、利用迭代器来改善和优化我们的代码。

 12-1 忘记密码（重置密码流程分析）
 12-2 first_or_404
 12-3 callable 可调用对象的意义
 12-4 HTTPException 一
 12-5 HTTPException 二
 12-6 装饰器app_errorhandler：AOP的应用
 12-7 发送电子邮件 一
 12-8 发送电子邮件 二
 12-9 使用itsdangerous生成令牌
 12-10 重置密码
 12-11 异步发送电子邮件
 12-12 鱼漂业务逻辑与Drift模型
 12-13 合理利用数据冗余记录历史状态
 12-14 鱼漂条件检测
 12-15 完成鱼漂业务逻辑
 12-16 交易记录页面
 12-17 Drift ViewModel 一
 12-18 Drift ViewModel 二
 12-19 三种类模式的总结与对比
 12-20 更好的使用枚举
 12-21 超权现象防范
 12-22 拒绝请求
 12-23 邮寄成功
 12-24 撤销礼物与心愿
 12-25 向他人赠送书籍