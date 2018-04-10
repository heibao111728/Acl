# Acl
ACL （全称 Advanced C Library），是一组跨平台的 C/C++ 网络通讯及服务器框架库，目前支持的平台：Windows/Linux/BSD/Solaris/MAC 

ACL 还包括网络应用常用的功能库，如：xml，json，http，icmp，dns，memcache，redis，mime，smtp，mysql/sqlite，handlersocket，beanstalk，
多种编码（如：base64/mime base64，urlcode，qp，hex，charset，etc），常用数据结构（如：hash，array，ring，fifo，二分块查找，stack，avl，etc），
线程池，etc
ACL 的设计原则：从实用角度 出发，结合常见应用场景，为开发者提供快速开发、稳定可靠的通信框架及服务框架

主要包含 6 个库及大量示例，6 个库的说明如下：
1) lib_acl: 基础核心库,其它库均依赖于该库( C 语言)
2) lib_protocol: 实现了 http/icmp 协议(C语言)
3) lib_acl_cpp: 封装了 lib_acl/lib_protocol 两个库，同时增加了一些其它有价值的功能(C++语言)
4) lib_dict: 实现了 KEY-VALUE 的字典式存储库，该库还依赖于 BDB, CDB 以及 tokyocabinet 库(C语言）
5) lib_tls: 封装了 openssl 库(C语言)
6) lib_rpc：目前仅支持 google protocol-buffer(C++)

大量示例：
1）acl/lib_acl/samples:  主要是 lib_acl 库的例子
2）acl/lib_protocols/samples:  主要是 lib_protocol 库的例子
3）acl/lib_acl_cpp/samples: 主要是 lib_acl_cpp 库的例子

基础库
stdlib: 配置文件、日志记录、网络/文件流读写、内存管理、常用数据结构、字符串处理、目录遍历等
net: 客户端/服务端接口、DNS查询、网络套接字、常用TCP控制等
aio: 非阻塞 IO 模块(读、写、连接、监听)
master: 服务器编程框架（进程池模式、多进程多线程模式、多进程非阻塞模式、多进程触发器模式）
thread: 线程、线程池、线程锁等
event: IO 事件引擎（支持 select、poll、epoll、kqueue、devpoll、iocp、win32 消息)
json/xml: 支持josn/xml编解码
db: 内存DB库、mysql 客户端库、zdb 数字K-V库
unit_test: 配置选项驱动的单元测试模块
http 协议库：比较完整的HTTP协议库，支持HTTP1.0/1.1版本数据传输、协议解析等功能，可用于客户端，也可用于服务端；同时支持阻塞及非阻塞方式传输
smtp 协议库: 客户端传输库，支持SASL身份验证
icmp/ping: 客户端库，支持阻塞及非阻塞方式
stdlib: 含字符串处理、字符集转换(Linux下封装了iconv库，win32下封装了平台相关库）、xml/json编解码、日志、md5、zlib封装等
stream: 网络/文件流，支持阻塞非阻塞方式及ssl 加密传输、客户端/服务端套接字
http: 功能丰富的 HTTP 协议库，支持客户端/服务端模式，http cookie/session 管理、类似Java HttpServlet 编程接口、HTTP mime 格式等
master: 服务器框架库，支持进程池(master_proc类)、多进程多线程(master_threads类)、多进程非阻塞(master_aio)、udp非阻塞通信(master_udp)、触发器(master_trigger) 四种服务器方式
mime: 完整的流式mime解析库，含mime、rfc2047、rfc822 等格式解析
ipc:  阻塞非阻塞模式通讯的交互接口，支持win32窗口消息
queue: 磁盘文件队列管理模块
其它常用协议客户端库：
connpool：通用 TCP 连接池及连接池集群管理框架
db: 数据库操作客户端库(支持mysql/sqlite)，支持连接池
memcache : memcached 协议的客户端库，支持连接池、集群管理、长连接重试
redis : redis 协议的客户端库，支持连接池、集群管理、长连接重试
hsocket:  mysqld 的 nosql 插件 handlersocket  的客户端库，支持连接池及连接重试
beanstalk:  消息队列服务 beanstalkd  的客户端库，支持连接池及连接重试


