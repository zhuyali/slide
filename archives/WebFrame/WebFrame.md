## jQuery

- - -

库 or 框架？

jQuery实际是一个JavaScript脚本库，它并不能帮我们解决脚本的引用管理和功能管理，只是帮我们完成编码逻辑，实现业务功能。

- - -

HTML 元素选取及操作,CSS 操作

$(document).ready(function() {
$(selector).action()
});

selector:
- 元素选择器 $("p#id")
- 属性选择器 $("[href$='.jpg']")
- CSS 选择器 $("p").css("","")

    存在命名冲突
    var jq = jQuery.noConflict()

    JavaScript 特效和动画
- 链式调用

    HTML DOM 遍历和修改
- 根据元素层级关系进行遍历查找
- 过滤元素，基于一组元素中的位置来选择一个特定的元素

- - -

    jQuery 其实就是一个函数库
- 封装了复杂的 DOM 原生操作
    (元素选取，层级关系，元素操作，属性控制)
- 对 DOM 进行操作
    (元素插入，元素删除，元素克隆，元素替代)
- 建立了 DOM 与 CSS 的联系
    (改变元素样式)
- 封装了网络请求
    (AJAX 进行异步网络请求)


- - -

## React

- - -

HTML 模板
<script src="../build/react.js"></script> react核心库
<script src="../build/react-dom.js"></script> 提供与 DOM 相关的功能
<script src="../build/browser.min.js"></script> 解析 JSX 语法为 JavaScript 语法
<script type="text/babel" src=""></script>

- - -

ReactDOM.render()
将模板转换为 HTML 语言，并插入到指定的 DOM 节点

- - -

JSX 语法
遇到 HTML 标签就用 HTML 规则解析；遇到代码块，就用 JavaScript 规则解析

- - -

Component 组件
- var Name = React.createClass({})
- 只能包含一个顶层标签
- 组件属性通过 this.props.属性名 来获取
- render()：用于输出组件
- propTypes：验证组件参数是否符合要求
- getDefaultProps()：设置组件属性的默认值
- getInitialState()：定义初始状态

this.props.children
- 无子节点，undefined
- 有一个子节点，object
- 有多个子节点，array


- - -

虚拟 DOM
- render 产生的并不是真正存在的 DOM 节点，而是轻量级的 JavaScript 对象
- 相比于每次有所改变就渲染整个 HTML 页面来说，只对页面上真正变化的部分进行实际的 DOM 操作，更加高效
- 获取真实的 DOM 节点，ref 属性


- - -

this.state
- 每次状态的变化，会导致页面重新渲染

this.props
- 一旦定义，就不再改变


- - -

组件生命周期
- Mounting：已插入真实DOM
- Updating：正在被重新渲染
- Unmounting：已移出真实DOM


- - -

Ajax
- 组件的数据来源可以异步获取
- 获取数据后，通过 this.setState 重新渲染页面

- - -

## Vue

- - -

语法

插值
- 文本：纯文本{{  }}，纯HTML v-html="rawHtml"
- 属性：v-bind:属性名
- JavaScript 语法支持：单个表达式
- 过滤器：{{ message | capitalize }}

指令
- v-：职责就是当其表达式的值改变时相应地将某些行为应用到 DOM 上
- v-model：双向绑定
- v-bind：响应地更新 HTML 属性
- v-on：监听 DOM 事件
- 修饰符：.指明后缀，v-on:submit.prevent 告诉 v-on 指令对于触发的事件调用 event.preventDefault()

缩写
- v-bind => :
- v-on => @

- - -

计算属性
- computed:{计算属性:function(){}}
- 计算缓存 VS Methods：仅当依赖属性变化时计算属性才会重新计算，而方法每次都会被调用
- 计算属性 VS Watched Property：都能够及时更新，计算属性可扩展性更好
- getter(默认)和setter
- Watchers：想要数据变化响应时，执行异步操作或者昂贵操作


- - -

Class 与 style 绑定

绑定 HTML Class
- v-bind:class 可以与 class 共存
- 对象语法：{className: bool}，可以绑定对象的计算属性
- 数组语法：[]
- 对象+数组

绑定内联样式

- - -

条件渲染
- v-if：切换消耗
- template v-if
- v-show：初始消耗
- v-else

- - -

列表渲染

v-for
- 数组迭代 v-for="item in/of items"
- 对父作用域有完全的访问权限
- template v-for
- 对象迭代
- 整数迭代
- 组件和v-for：子组件获取父组件中的数据，使用props

数组更新检测
- 变异方法和非变异方法

- - -

事件处理器
- 监听事件
v-on:event="JavaScript Code"
v-on:event="Method Name"
- 事件修饰符
.stop/.prevent/.capture/.self
- 按键修饰符

- - -

表单控件绑定
- v-model
- 修饰符

- - -

组件

- 注册
全局注册：Vue.component(tagName, options)
局部注册：Vue components属性
- DOM 模板解析时，会受到 HTML 限制，可以通过 is
- data 必须是函数

props
- 父组件向子组件传递数据
- 动态 props，每当父组件的数据变化时，将该变化传导给子组件
- 字面量语法 vs 动态语法
- 当 props 是对象时，包含验证要求

自定义事件
- 子组件向父组件传递数据
- v-on监听事件，v-emit处罚事件

使用 slot 分发内容

动态组件

- - -
