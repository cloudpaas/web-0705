课程介绍:
 * 第一个阶段 - HTML、CSS和JavaScript
 * 第二个阶段 - HTML5、CSS3和移动端
 * 第三个阶段 - (服务器端)Node.js
 * 第四个阶段 - 框架类AngularJs、React.js和Vue.js
上课安排:
 * 8:25到校
   * 读单词 - 每天 20 个单词，读两遍
   * 晨测 - 测试前一天学习的内容，5道题
   * 每天 - 复习前一天的内容
 * 9:00 - 12:00 ~ 上午上课
 * 2:00 - 5:00 ~ 下午上课
 * 6:00 - 9:30 ~ 自习
课程资料:
 * CODE - 存放当天的课程代码
 * DATA - 存放当天的课程资料
   * 上课所需要的资料
   * 上课画一些解析图
 * VIDEO - 存放当天的课程视频
 * NOTE - 存放当天的课程笔记
 * readme.txt - 当前随堂笔记
SVN的使用:
 * 鼠标右键 -> SVN检出
 * 输入 SVN地址 -> svn://192.168.10.165
HTML
 * 概念
   * HTML+CSS+JavaScript - 这三者之间是什么关系?
     * HTML -> 结构 -> 素描
     * CSS -> 样式 -> 水彩
     * JavaScript -> 行为 -> 动画
   * 全称 Hyper Text Markup Language，译为超文本标记语言
     * 超文本 -> 文本(就是普通的文字) -> 在文本的基础上添加了超链接
       * 目前的情况 -> 在普通的文本基础上，添加了超链接、图片、音频或视频等复杂内容
     * 标记 -> 特点:<a>
     * 语言 -> 目前目标所能识别的
   * 版本
     * HTML 4.01 -> 注意 4.01 与 4.0 不是一个版本
     * HTML 5 -> 目前主流的最新版本
   * XHTML -> 严格版本的HTML
 * HTML元素(标签)
   * 空元素 - 只有开始标签，没有结束标签
   * 起始元素 - 具有开始标签和结束标签
   * 注意
     * 元素名 - W3C预定义，建议使用小写
 * HTML属性
   * HTML元素中定义属性 - 扩展当前元素的信息
   * 属性必须定义在开始标签中
   * 格式 - 属性名="属性值"
   * 同一个元素具有多个属性
   * 分类
     * 通用属性 - 几乎所有的HTML元素都具有的属性
       * id - 表示当前元素的标识(唯一的)
       * name - 表示当前元素的名称
       * style - 表示定义CSS样式
       * class - 表示定义CSS样式
     * 私有属性 - HTML中指定某个元素具有的属性
 * HTML注释
   * 作用 - 解释当前的元素的作用
   * 特点 - 不会显示在浏览器的页面中
   * 格式 - <!-- 注释内容 -->
   * 快捷键 - CTRL + ?
 * HTML标题
   * <h1> ~ <h6> - 字体由大到小
   * 在实际开发中，比较常用的
     * <h1>、<h2>和<h3>
   * <h1>标签
     搜索引擎抓取HTML页面时
     1. <title>元素中的内容
     2. <meta name="keywords" content="">
     3. <h1>元素
   * 快捷键 - 标签名 + TAB
 * HTML段落
   * <p> - 表示段落
   * <hr> - 表示水平线
   * <br> - 表示换行
 * HTML列表
   * 有序列表 - <ol>
     * 列表项 - <li>
   * 无序列表 - <ul>
     * 列表项 - <li>
   * (自)定义列表
     * <dl> - 表示定义列表
     * <dt> - 表示列表项(列表的标题)
     * <dd> - 表示列表项的描述(列表项)
   * 快捷键
     * 标签名*数量 + TAB
     * ALT + 鼠标左键
 * 链接元素
   * <a>标签 - 起始标签
   * 必要属性 - href
浏览器的开发者工具
 * 快捷键 - F12