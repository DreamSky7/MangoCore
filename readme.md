### 版本记录
> 记录每个版本的功能迭代和API变更，以及修复的历史记录

* #### 1.0.0
  项目的第一个版本，实现了基本的功能，包括：基本的消息处理器，动态注册指令，注解绑定补全器，配置文件管理器等。
* #### 1.0.1
  支持配置文件的URL地址加载，支持Java对象序列化至Yaml文件，支持Yaml文件反序列化至Java对象。已支持大部分的复杂结构如List<Map<String,Object>>，更深层次的结构数据暂时不支持，后续考虑会逐步完善。
* #### 1.0.2
  - 修复YamlUtils反序列Map<String, 对象>时的错误，
  - 修改MessageUtils使其在变量为List的情况下进行多行消息的发送
  - 修改MessageUtils使其支持扩展消息类型，如[title],[actionbar],[command]等消息类型
  - 新增MessageUtils方法senderMessageByList，支持自定义List<String>的消息发送，支持扩展消息类型
* #### 1.0.3
  - 新增数据库工具类，支持MySQL，内置Druid连接池，提供增删改产的快速使用方法
* #### 1.0.4
  - 修复了一些小BUG，我忘记了
* #### 1.0.5
  - 对消息工具类进行了重新设计，该版本与前版本有较大差距，无法平替。
  - 重新设计文件管理器，并引入了自创建的MangoFile类，支持Yaml和Json文件的读写
  - 对于配置文件推荐使用MangoConfiguration对象进行读取，以下是已支持的结构读取
    * `Object` [包括Object内部的List<Object>和Object结构的读取]
    * `List<Object>`
    * `Map<String, Object>`
    * `Map<String, List<Object>>`
  - **感谢千千一路上的帮助，我直接就是原地结婚**
