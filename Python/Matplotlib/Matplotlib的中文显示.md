Matplotlib 中文显示不是特别友好，要在 Matplotlib 中显示中文，我们可以通过两个方法：
	设置 Matplotlib 的字体参数。
		我们可以先获取系统的字体库列表：
		`from matplotlib import pyplot as plt`
		`import matplotlib`
		`a=sorted([f.name for f in matplotlib.font_manager.fontManager.ttflist])`
		`for i in a:`
		    `print(i)`
		![[Pasted image 20251029084038.png]]
		以上代码输出 font_manager 的 ttflist 中所有注册的名字，找一个看中文字体例如：STFangsong(仿宋）、Heiti TC（黑体）,然后添加以下代码即可：
		`plt.rcParams['font.family'] = 'SimHei'  # 替换为你选择的字体（Win可用）`
		通过设置 plt.rcParams['font.family']，你告诉 Matplotlib 使用选择的字体来渲染文本，从而在图表中正确显示中文。
	下载使用支持中文的字体库。
		Matplotlib 默认情况不支持中文，我们可以使用以下简单的方法来解决。
		这里我们使用思源黑体，思源黑体是 Adobe 与 Google 推出的一款开源字体。
		可以下载个 OTF 字体，比如 SourceHanSansSC-Bold.otf，将该文件文件放在当前执行的代码文件中：
		SourceHanSansSC-Bold.otf 文件放在当前执行的代码文件中：![[Pasted image 20251029084838.png]]
	![[Pasted image 20251029083940.png]]