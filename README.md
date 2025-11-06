# 华东师范大学幻灯片模板 1.0

本模板基于 beamer，推荐使用 XeLaTeX 编译。

## 编译

在项目根目录执行（macOS/zsh）：

```sh
xelatex ECNU_BeamerTemplate.tex
```

如需生成参考文献索引或多次交叉引用，请运行 2–3 次。

## 缺失图片的占位显示

示例文档中引用了若干图片文件（如 `async_benefit.png` 等）。若这些图片不在同一路径下，模板会自动显示带红色边框的占位框，并继续编译，不会中断。

占位由宏 `\maybeincludegraphics[<选项>]{<文件名>}` 实现，其用法与 `\includegraphics` 相同。例如：

```tex
\maybeincludegraphics[width=0.8\textwidth]{async_benefit.png}
```

当文件存在时正常插图；当文件不存在时显示占位框和文件名提示。

## 字体与数学

已改为使用 `\usefonttheme[onlymath]{serif}`，仅数学部分采用衬线字体，避免 `mathserif` 过时选项的警告。

## 效果图
![](https://godweiyang.com/2017/12/29/ecnu-ppt/1.png)
