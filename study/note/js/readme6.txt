回顾JavaScript第五天内容:
 * 特殊函数
   * 匿名函数 - 没有名的函数
     * 问题 - JavaScript语法并不支持匿名函数(不能直接使用)
   * 自调函数 - 自己调用自己的函数(没有调用)
     * 特点
       * 定义即调用
       * 只能被调用一次
     * 语法结构
       * 第一个小括号 - 定义函数
       * 第二个小括号 - 调用函数
   * 回调函数 - 作为另一个函数的参数出现的函数
     * 回调函数
     * 匿名回调函数 - 将匿名函数作为另一个函数的参数
   * 内部函数 - 被定义在一个函数中的函数
     * 特点 - 只能在当前函数作用域被访问
   * 作为值的函数 - 将内部函数放在return语句
     * 在全局作用域中访问到内部函数
     * 在全局作用域中访问到局部变量
 * 对象
   * 概念
     * 万物皆对象 - 将任何事物都看作是一个对象
       * 属性 - 用于描述对象的信息
       * 方法 - 用于描述对象的行为
     * 封装 - 函数
       * 只关心输入(我给对方什么)和输出(对方给我什么)
       * 并不关心过程是如何实现的
   * 定义对象
     * 初始化器
       var 对象名 = {
           属性名 : 属性值,
           方法名 : function(){}
       }
     * 构造函数
       var 对象名 = new Object();
       对象名.属性名 = 属性值;
       对象名.方法名 = function(){}
     * Object.create()方法
       var 对象名 = Object.create(null);
       对象名.属性名 = 属性值;
       对象名.方法名 = function(){}
   * 操作对象的属性和方法
     * 调用属性和方法
       * 方式一
         对象名.属性名
         对象名.方法名()
       * 方式二
         对象名['属性名']
         对象名['方法名']()
     * 新增
       对象名.新的属性名 = 属性值;
       对象名.新的方法名 = function(){}
     * 修改
       对象名.属性名 = 新的属性值;
       对象名.方法名 = function(){}
     * 删除
       delete 对象名.属性名
       delete 对象名.方法名
   * 遍历属性或方法
     * for...in循环语句
     * Object.keys()方法
   * 检测属性或方法
     * in 关键字
   * 访问不存在的属性时 - undefined
今天的内容:
 * JSON
   * 概念 - 是一种轻量级的数据交换格式
   * 格式
     * 被称为是 键/值 对的对象格式
     * 被称为 有序列表的数组格式
   * JSON - 支持独立的".json"文件
     * JSON中的字符串只能使用双引号
   * 支持的数据类型
     * string
     * number
     * boolean
     * null
     * object
     * array
 * 原型
   * 显式原型 - Function 的 prototype
     * 在真实的开发环境中使用
   * 隐式原型 - Function 的 __proto__
     * 不能被使用在真实的开发环境中
     * 用于开发过程中的测试
 * 引用类型
   * Date类型
     * 获取常规的日期+时间
     * getTime() - 距离 1970 年 1 月 1 日
       * 利用毫秒值进行时间的计算
       * 实现时间戳(标识)
   * Math类型
     * PI - 圆周率
     * 对数字的处理
     * 生成随机数