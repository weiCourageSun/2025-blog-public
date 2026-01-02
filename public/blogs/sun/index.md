# **markdown基础语法介绍**

## 标题

#为1级大标题(ctrl+1)
##为2级标题(ctrl+2)
###为3级标题(ctrl+3)
........
一共有6级标题(ctrl+6)

**选中**  要选择的文字作为标题(按下ctrl+对应数字)，即可产生各级标题(其中#数量可以视为标题等级)

## 段落与换行

体验过才知道，“enter键”--直接换行就是 换一个段落另起一行，有点像自然段段间距。例如

example1

example2
example3

可以明显看到1与2，3的间距是不一样的，1与2和3是段落区别，2和3则是行间距区别。普通换行快捷键为(shift+enter)

## 强调

没啥多说的，多用多写，给出快捷键即可
斜体----*斜体*     (ctrl+I)
加粗----**加粗**  （ctri+B）
斜体+加粗---- ***斜体+加粗***(ctrl+I + ctrl +B)

## 列表

markdown给出无序列表(没有序号)和有序列表(子项目有序号并自动帮你更新)

“-”“+”“*”这些符号都可以作为无序列表的第一个输入，然后紧跟“空格”即可弹出无序列表的格式
“1”“2”基于数字打头然后再接“空格”会弹出有序序列列表的格式

- “无序列表”
- “自动添加

“shift + Tab”退出所在序列，另起一行

## 链接

个人觉得最方便的是先选择好你要跳转的网址，粘贴最方便，然后在markdown中给它起个名字，选中后“ctrl+K”后 会自动附上链接，手动输入比较麻烦。

https://www.google.com
[Google](https://www.google.com)
[搜索 - Microsoft 必应 (bing.com)](https://cn.bing.com/)

## 图片

这里的图片分为本地图片和网络图片，网络图片又被称为图床

本地图片可以直接复制粘贴或者直接拖拽进去，markdown自动给出图片地址，操作便捷

对于网络图片，给出地址即可，该方法不会存在路径错位找不到的问题，在上传本地图片一定要注意文件的相对路径在markdown的图像文件下，以免丢失（建议勾选 **`复制图片到./${filename}.assets 文件夹`**）。这一步是配置Typora的操作，b站有教程参考

# 代码块：Markdown 语法与展示

## 1. 行内代码

**语法**：用一个反引号 ` 包裹简短代码


**实际效果**：
这是 `行内代码` 示例，比如 `print("Hello")` 或 `git status`。

## 2. 基本代码块

**语法**：用三个反引号 ``` 包裹多行代码

// JavaScript 代码示例
function calculateSum(a, b) {
    return a + b;
}

// 使用箭头函数
const multiply = (x, y) => x * y;

console.log(calculateSum(5, 3));
console.log(multiply(4, 7));

**实际效果**：
```javascript
// JavaScript 代码示例
function calculateSum(a, b) {
    return a + b;
}

// 使用箭头函数
const multiply = (x, y) => x * y;

console.log(calculateSum(5, 3));
console.log(multiply(4, 7));
```

