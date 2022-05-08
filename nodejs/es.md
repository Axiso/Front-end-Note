

## ESLint

ESLint，插件化的javascript代码检测工具。



Configuring ESLint
ESlint 被设计为完全可配置的，这意味着你可以关闭每一个规则而只运行基本语法验证，或混合和匹配 ESLint 默认绑定的规则和你的自定义规则，以让 ESLint 更适合你的项目。有两种主要的方式来配置 ESLint：

1. Configuration Comments - 使用 JavaScript 注释把配置信息直接嵌入到一个代码源文件中。
2. Configuration Files - 使用 JavaScript、JSON 或者 YAML 文件为整个目录（处理你的主目录）和它的子目录指定配置信息。可以配置一个独立的 .eslintrc.* 文件，或者直接在 package.json 文件里的 eslintConfig 字段指定配置，ESLint 会查找和自动读取它们，再者，你可以在命令行运行时指定一个任意的配置文件。

如果你在你的主目录（通常 ~/）有一个配置文件，ESLint 只有在无法找到其他配置文件时才使用它。

有很多信息可以配置：

* Environments - 指定脚本的运行环境。每种环境都有一组特定的预定义全局变量。
* Globals - 脚本在执行期间访问的额外的全局变量。
* Rules - 启用的规则及其各自的错误级别。

所有这些选项让你可以细粒度地控制 ESLint 如何对待你的代码。

## TSLint

typescript