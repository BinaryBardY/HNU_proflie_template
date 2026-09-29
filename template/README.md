# HNU Profile LaTeX 模板

这是一个湖南大学个人简介模板。页首采用“左侧校徽、居中姓名与院系、右侧证件照”的布局，下面是两行基本信息；各板块使用红色加粗标题和红色横线。板块顺序为：

1. 基本信息
2. 教育经历
3. 科研经历
4. 竞赛获奖
5. 其他经历与荣誉

## 编译

在 `template` 目录执行：

```bash
xelatex -interaction=nonstopmode hnu_profile.tex
```

模板默认从 `../logo/hnu_logo_white_cropped.png` 读取左上角白底校徽。原始 `hnu_logo.png` 和未裁剪的白底版本均保留不变。若要显示证件照，将图片命名为 `photo.jpg` 放入 `profile/photo/` 目录（相对于 `template` 为 `../photo/photo.jpg`）；没有照片时会显示占位框。

## 修改内容

直接编辑 `hnu_profile.tex` 中的占位符即可。科研经历和竞赛获奖条目可以复制对应的 `\entrytitle` 块增加，右侧日期/奖项用 `\rightmeta{...}` 对齐。
