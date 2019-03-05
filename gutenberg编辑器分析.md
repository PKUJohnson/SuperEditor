## gutenberg

以尝试将 `gutenberg-js`集成至 `React` 中：https://github.com/QiShaoXuan/gutenberg-js-demo

### 验证

1. 支持类型
   -  基本上所有富文本所支持的标签都有
2. 存储格式
   - 带注释的HTML代码
     - 解析为 JSON（虚拟 DOM ）可以参考现有框架的转换方式（未考察）
3. 转化 H5
   - 可直接将 HTML 代码写入
4. 转化小程序
   - 可能需要第三方库
5. 扩展工作
   - 参考 https://github.com/WordPress/gutenberg-examples
     - 应该需要 PHP 文件配合编译
6. 如何动态解析
   - 直接将 HTML 代码段写入页面，没有动态解析


### 可能遇到的问题

1. `React` 源码版本低，在当前集成至 `React 16+` 版本存在 warning。列举已知如下：
   - 生命周期 `componentWillUpdate` （会在 `React 17` 后废弃）
   - `findDOMNode ` 
2. 存在报错，影响使用，暂未找到解决方法，列举已知如下：
   - Formatting -> Classic （报错）
   - Formatting -> Table （创建200列 table 卡死）
3. 编写 gutenberg 的扩展插件需要 `React` +`PHP`，暂未发现纯 JS 的开发方式。官方扩展参考 https://github.com/WordPress/gutenberg-examples

## 综合比较

gutenberg 已有插件更丰富，已有交互也更好，但是相对更封闭（个人感觉）。

slate 生态基本为零，需要自己编写大量扩展。

个人认为应该针对需求的富文本要求来选择两个编辑器，如果本身要求不多，更侧重于开发新的插件我觉得 slate 更方便一点。







