
## 方法论

使用 [ValveResourceFormat](https://github.com/ValveResourceFormat/ValveResourceFormat) 来提取和反编译游戏布局、样式和图像,使用以下命令:

```
Decompiler -d \
	-i Deadlock/game/citadel/pak01_dir.vpk \
	--vpk_filepath panorama/images,panorama/layout,panorama/styles \
	-o exported
```

提取这些资源后,对 XML 和 CSS 文件进行手动分析,创建新的静态 HTML 文档,并修改 CSS 规则,将 Valve 自定义的 CSS 属性(如 `wash-color`)转换为使用 `mask-image` 和 `background-color` 或 `mix-blend-mode` 的实现。
