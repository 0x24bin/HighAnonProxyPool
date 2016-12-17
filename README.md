# ProxyPool

**12月17日**
- 将爬虫模块整合为多线程，一发制动全部
- 修复了requests代理全部失败的Bug（大小写）
- 增加了验证代理时的各类异常捕捉机制
- 待做：
	- 数据库在同步操作的时候会上锁，影响效率，应想办法优化
	- 目前是需要分别打开爬虫程序与验证程序，比较麻烦，应实现爬虫与验证程序一体化。
	- 一体化实现后应做到实时CUI界面交互。
	- 开发更多代理爬虫，以实现类似Unit Testing的功能

**12月16日**
- 将数据库记录定义为ip、端口、协议，必须满足全部三项才可指定（比如删除）一条记录
- 实现了代理验证的多线程特性
- 优化了代理模块的部分逻辑关系
- 设计了爬虫管理模块的运行模式：单文件多函数，每个函数为一个爬虫，运行时进行多线程爬取

**（中间的这段时间我去折腾机器学习了。。。）**

**12月3日**
- 重新设计了整个高匿代理池项目的组成模块。
- 完成数据库模块的Add功能，改进Sqlite命令的去重
- 完成数据库模块的Delete及Fetch_all功能
- 完成代理库模块的check功能，暂时先使用icanhazip进行匿名检测，去除了多余的异常处理。
- 待学习：模块之间沟通的具体代码实现，是直接在模块内调用其他模块的代码还是在主程序中为各模块进行交互？

