Less学习笔记

快速入门：
Less是CSS预处理语言，它扩展了CSS语言，增加了变量、Mixin、函数等特性，使CSS更易维护和扩展。
Less可以运行在Node或浏览器端。

使用方法
安装
npm install -g less
命令行用法
lessc styles.less
lessc styles.less styles.css
lessc --clean-css styles.less styles.min.css
代码用法
var less = require('less');

less.render('.class { width: (1 + 1) }', function (e, output) {
  console.log(output.css);
});

var less = require('less');

less.render('.class { width: (1 + 1) }',
    {
      paths: ['.', './lib'],  // Specify search paths for @import directives
      filename: 'style.less', // Specify a filename, for better error messages
      compress: true          // Minify CSS output
    },
    function (e, output) {
       console.log(output.css);
    });

