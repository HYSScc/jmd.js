# jmd.js
极小型、高性能、浏览器端Javascript模块化库

# 特点
  - 遵循 CMD 规范，可以像Node.js 一样来写模块代码
  - 完全异步，不对源码做任何改动、没eval、setTimeout，全速加载!
  - 只有一个函数：**define**，连学习文档都不需要了！
  - 代码小巧，方便扩展

# 如何使用
``` Html
<html>
  <head>
	<script src="jmd.js"></script>
	<script src="main.js"></script>
  </head>
  <body>
  </body>
</html>
```
main.js是你的程序的入口，名字也可任意的

# 定义模块:
``` Javascript
  // main.js
  define('main', function (require, module, exports){
    
    var util = require('util');
    var $ = require('jquery');
    
    //TODO:	
    
    module.exports = {
    	//TODO:
    };
  });
  
  // util.js
  define('util', function (require, module, exports){
    
    function trim(str){
    }
    
    module.exports.trim = trim;
    
  });
```
模块名称就是文件的名称

# 配置
- 修改加载目录:
``` Javascript
  define.config = {
    findPath: './' // 默认为当前页面所在目录
  };
```
