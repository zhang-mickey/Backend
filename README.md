# 技术选型
#
Java执行Python代码的两种方法（Jython与ProcessBuilder）
# Elasticsearch	搜索引擎
SQL 的 LIKE 也能实现匹配
全表扫描 模糊匹配

## 倒排索引（Inverted Index）
倒排索引怎么构建的呢？当我们往 ES 写入商品记录的时候，ES 会先对需要搜索的字段，也就是商品标题进行分词。然后以分词为索引组成一个查找树，这样就把一个全文匹配的查找转换成了对树的查找，这是倒排索引能够快速进行搜索的根本原因。

但是，倒排索引相比于一般数据库采用的 B 树索引，它的写入和更新性能都比较差，因此倒排索引也只是适合全文搜索，不适合更新频繁的交易类数据。


##   class 反编译 
.java 文件经过 JAVA编译器（javac）编译成中间代码字节码 .class 文件
### javap命令
 javap -c -l LikeAdminApplication.class 

### Recaf


### JD-GUI

## Java Agent机制

# Swagger
## @Api
用于 Swagger 文档生成，描述该控制器的功能。
## @ApiOperation
用于 Swagger 文档生成，描述方法的功能。
## @ApiModelProperty

# ID

有的业务直接通过 DB 自增的方式生成 ID，有的业务通过 Redis 缓存来生成 ID，也有的业务直接用 UUID 这种方式来生成 ID

## 雪花算法

# Value Object 值对象
通常是不可变的，这意味着一旦创建，它们的状态不能再被修改。这有助于确保数据的一致性和可靠性
![image](https://github.com/zhang-mickey/Backend/assets/145342600/9b040632-64d9-4788-ab8d-97835ac84670)

# spring boost
Spring Initializr Java Support


lsof -i :8080 显示占用8080端口的进程信息
## Spring Quartz
定时任务的调度框架
## Spring MVC

### 拦截器(Interceptor)
类似于ServLet中的过滤器(Filter)，它主要用于拦截用户请求并作出相应的处理。例如通过拦截器可以进行权限验证、记录请求信息的日志、判断用户是否登录等。

想要在Spring Boot生效其实很简单，只需要定义一个配置类，实现WebMvcConfigurer这个接口，并且实现其中的addInterceptiors()方法即可
## 类使用implements关键字实现接口
一个类可以同时实现多个接口

除非实现接口的类是抽象类，否则该类要定义接口中的所有方法

## @Validated
在方法参数前添加，表示对该参数进行验证
## META-INF

## BOOT-INF
Spring Boot应用程序从Boot-INF文件夹加载

应用程序类放在嵌套的BOOT-INF/classes目录中。依赖关系放在嵌套的BOOT-INF/lib目录中
## @RequestBody

## @RestController
将一个类标记为 RESTful Web 服务的控制器,
是 @Controller 和 @ResponseBody 注解的组合

## @RequestMapping
可以用在类级别和方法级别

## @GetMapping
专门用于处理 HTTP GET 请求的注解。它是 @RequestMapping 的简化版本，专门用于处理 GET 请求
## JDBC Java DataBase Connectivity
使用Java程序访问数据库时，Java代码并不是直接通过TCP连接去访问数据库，而是通过JDBC接口来访问，而JDBC接口则通过JDBC驱动来实现真正对数据库的访问
![image](https://github.com/zhang-mickey/android/assets/145342600/efe4ba38-451e-4082-91ce-ff8b6fbe0c7e)


### 使用 JPA 访问数据库
JPA不仅允许我们与数据库交互，还可以将记录从数据库直接映射到java对象，而无需开发人员方面的任何手动操作
### Mybatis
ORM 就是一种为了解决面向对象与关系型数据库中数据类型不匹配的技术，它通过描述Java对象与数据库表之间的映射关系，自动将Java应用程序中的对象持久化到关系型数据库的表中
### Hibernate

全表映射的框架

### WebSocket
HTTP 协议有一个缺陷：通信只能由客户端发起   做不到服务器主动向客户端推送信息 
![image](https://github.com/zhang-mickey/android/assets/145342600/b0bc9109-c5ba-48f2-b3ec-6324a4c89253)

这种单向请求的特点，注定了如果服务器有连续的状态变化，客户端要获知就非常麻烦。我们只能使用"轮询"：每隔一段时候，就发出一个询问，了解服务器有没有新的信息。最典型的场景就是聊天室。

轮询的效率低，非常浪费资源（因为必须不停连接，或者 HTTP 连接始终打开）
### Bean


使用 java 配置完全代替 XML 配置，java 配置是通过 @Configration 和 @Bean 注解实现的

@Configration 注解：声明当前类是一个配置类，相当于 Spring 中的一个 XML 文件

@Bean 注解：作用在方法上，声明当前方法的返回值是一个 Bean

结合Configuration来定义bean，首先是声明一个配置类，然后在配置类中，通过返回bean对象的方法形式来声明bean

**Autowired注入**
将注解@Autowired 添加到成员变量上，即表示这个成员变量会由Spring容器注入对应的Bean对象

**setter方法**



![image](https://github.com/zhang-mickey/Backend/assets/145342600/af66c57d-3bdf-46fd-8bdb-b52a8f7945a3)





