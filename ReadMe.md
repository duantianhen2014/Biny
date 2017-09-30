## 概况
Biny是一款高性能的超轻量级PHP框架

遵循 MVC 模式，用于快速开发现代 Web 应用程序

Biny代码简洁优雅，对应用层，数据层，模板渲染层的封装简单易懂，能够快速上手使用

高性能，框架响应时间在1ms以内，单机qps轻松上3000

## 功能介绍
支持跨库连表，条件复合筛选，查询PK缓存等

同步异步请求分离，类的自动化加载管理

支持Form表单验证，支持事件触发机制

支持浏览器端调试，快速定位程序问题和性能瓶颈

具有sql防注入，html自动防xss等特性

## 使用文档

框架Wiki地址：[http://www.billge.cc](http://www.billge.cc)

GitHub 地址：[https://github.com/Tencent/Biny](https://github.com/Tencent/Biny)

## FAQ

Q: 框架跟传统PHP框架区别在哪儿，有什么优势？

A: Biny是个自由度很高的框架，不像其他框架需要配置各种路由，自动加载类，复杂的命名空间。这些在Biny中都是不需要的，按照一个简单的规则就能快速使用这些功能。从开发者的角度出发，在功能上使用非常简单。而且具有相当强的安全性。从框架层面完全屏蔽了 SQL注入和 XSS注入两大安全难题，非常适合新人使用。

Q: Biny框架的性能如何？

A: 测试机：Intel Xeon Processor E5506 (4M Cache, 2.13 GHz, 4.80 GT/s Intel？ QPI)
一个普通查询数据页面（50%命中缓存）QPS 能轻松达到3000以上，同比Yii，性能是Yii的2倍以上。

Q: 我想使用Biny，请问有相关说明文档吗？

A: 文档都在[http://www.billge.cc](http://www.billge.cc)中

Q: Biny框架适配PHP7吗？

A: 可以完美运行，性能提高2倍以上。

Q: Biny现在是最终版了吗，还会继续更新吗？

A: 目前版本在多个项目中已经正常使用，相对成熟。后续会针对性能和功能上都会持续更新，届时只需更新替换 lib库 即可使用最新框架。

## 常见问题

Q：模版渲染出现错乱是为什么

A：请在php.ini中打开short_open_tag。Biny的示例中使用了PHP中原生的简写渲染方法，需要将系统配置中的简写配置打开才能正常使用。
当然如果是自己开发的模版页面，不用简写方式的话，就算不打开short_open_tag也是可以的。简写示例：<?php echo $string;?> => <?=$string?>