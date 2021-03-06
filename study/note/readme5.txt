回顾CSS的第二天内容:
 * 盒子模型
   * 作用 - 实现页面的布局效果
   * 内容
     * 内容区 - HTML的元素
     * 内边距 - 内容区到边框的距离
     * 边框
     * 外边距 - 边框到页面的边缘的距离
 * 边框
   * border - 同时边框的宽度、颜色和样式
     * border-width - 设置边框的宽度
     * border-color - 设置边框的颜色
     * border-style - 设置边框的样式
     
     * 特点 - 同时设置四个边框
   * 分别设置四个边框
     * border-top - 上
     * border-right - 右
     * border-bottom - 下
     * border-left - 左
 * 内边距
   * padding - 设置四个方向的内边距
     * 如果一个值 - 同时设置四个方向
     * 如果二个值 - 上下、左右
     * 如果三个值 - 上、左右、下
     * 如果四个值 - 上、右、下、左
   * 分别进行设置
     * padding-top
     * padding-right
     * padding-bottom
     * padding-left
 * 外边距
   * margin - 设置四个方向的内边距
     * 如果一个值 - 同时设置四个方向
     * 如果二个值 - 上下、左右
     * 如果三个值 - 上、左右、下
     * 如果四个值 - 上、右、下、左
   * 分别进行设置
     * margin-top
     * margin-right
     * margin-bottom
     * margin-left
   * 存在的问题
     * 如果存在两个元素，之间是相邻兄弟关系的话
       * 上一个元素设置下外边距，下一个元素设置上外边距
       * 结果 - 取两者之间的最大值，而并不是相加的结果
       * 解决 - 只设置其中一个的外边距
     * 如果存在两个元素，之间是相邻兄弟关系的话
       * 下一个元素设置上外边距为负值时
       * 结果 - 下一个元素会覆盖上一个元素
     * 如果元素设置做外边距为负值时
       * 结果 - 当前元素移出页面
     * 如果存在两个元素，之间是父级与子级元素的关系
       * 为子级元素设置上外边距时
       * 结果 - 子级元素的上外边距会传递给父级元素
       * 解决 - 为父级元素设置上内边距
 * 行内元素的盒子模型
   * 设置宽度和高度 - 无效
     * 行内元素的宽度和高度取决于文本内容
   * 设置外边距时的问题
     * 水平方向的左外边距和右外边距 - 有效
     * 垂直方向的上外边距和下外边距 - 无效
       * 设置其父级元素的上内边距和下内边距
 * 盒子模型的分类
   * 默认盒子模型 - content-box
     实际的宽度 = width + padding + border
   * 怪异盒子模型 - border-box
     实际的宽度 = width
今天的内容:
 * 显示与隐藏
   * display属性
     * none - 隐藏元素，不会再占有页面的任何空间
     * inline - 默认值。将元素显示为内联元素
       * 注意 - 与HTML元素本身并无关系
     * block - 将元素显示为块级元素
       * 注意 - 与HTML元素本身并无关系
     * inline-block - 将元素显示行内块级元素
       * 每个元素呈现的是块级元素的效果(宽度和高度是有效的)
       * 每个元素之间呈现的是内联元素的效果(不会独占一行)
   * visibility属性
     * hidden - 隐藏元素，依旧占有页面的空间位置
     * visible - 默认值
 * overflow属性
   * 内容溢出 - 文本内容超出当前元素的显示范围
   * 解决内容溢出的最好方式
     overflow : auto
 * 文档流
   * 概念 - 垂直方向从上到下的顺序排列，水平方向从左到右的顺序排列
   * 注意 - 默认情况下，排列的顺序是不能改变的
 * 浮动
   * 特点 - 将当前元素脱离文档流
   * 可选值
     * left - 左浮动
     * right - 右浮动
   * 特殊场景
     * 父与子元素，设置子元素浮动 - 不能超出父元素的范围
     * 兄弟元素都设置为浮动时 - 自动排列(水平方向)
     * 兄弟元素，后一个元素设置为浮动，前一个元素不浮动
       * 后一个元素的位置不能超过前一个元素的位置
     * 文字内容不会被浮动的元素所覆盖 - 环绕在浮动的元素周围
 * 高度塌陷
   * BFC块级格式化环境
     * BFC是元素的隐含属性。默认情况下，BFC是关闭的
     * 如何开启BFC
       * 将当前元素设置为浮动
       * 将当前元素的 overflow 设置为 非visible 的值(一般为hidden)
       * 在所有子元素的最后，新增一个子元素，并且设置 clear 属性值为 both
   * 解决高度塌陷
     * 最好的方式 - overflow : hidden
 * 定义(position)
   * 可选的值
     * static - 默认值。表示静态定位(没有开启定位)
     * relative - 表示相对定位
     * absolute - 表示绝对定位
     * fixed - 表示固定定位
   * 绝对定位(absolute)
     * 效果
       * 相对于HTML页面进行的定位
         * 页面的元素设置为绝对定位时
         * 父级与子级元素，只有子级设置为绝对定位时
       * 相对于父级元素进行的定位
         * 父级与子级元素都设置为绝对定位时
     * 开发绝对定位
       * 从文档流中脱离
       * 行内元素呈现出块级元素的特点(宽度和高度有效)
     * 设置定位的值
       * left和top - 设置距离左边和上边的值
       * right和bottom - 设置距离右边和下边的值
   * 固定定位(fixed)
     * 效果 - 只相对于HTML页面进行的定位
   * 