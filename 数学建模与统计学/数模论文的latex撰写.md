![[Pasted image 20260129135252.png]]
\documentclass{mcmthesis}   %当使用laTeX套装时请注释上一行使用该行的设置\mcmsetup{tstyle=\color{black}\bfseries,    %修改题号，队号的颜色和加粗显示，黑色可以修改为black
tcn=123456,problem=A,    %修改队号，参赛题号
sheet = true, titleinsheet = true, keywordsinsheet = true,titlepage = false, abstract = true}
\usepackage{float}
%四款字体可以选择
\usepackage{times}
%\usepackage{newtxtext}
%\usepackage{palatino}
%\usepackage{txfonts}
\usepackage{ulem}
\usepackage{multirow}
\usepackage[utf8]{inputenc}
\usepackage{indentfirst}%首行缩进，注释掉，首行就不再缩进。\usepackage{lipsum}
\usepackage{lastpage}%解决LastPage引用未定义问题
%修改CTEX字体配置，使用adobe字体集替代mac
%\usepackage{ctex}
第一个重要的点在于latex原生不支持中文，那么我们先要解除ctex的注释
之后，如果用的是texstudio，![[Pasted image 20260129140123.png]]
在设置界面把编译器改成XeLaTex

\title{论文标题}
\begin{document}
\begin{abstract}
	这个地方写的是摘要
	\begin{keywords}
		这里写的的关键词
	\end{keywords}
\end{abstract}
\maketitle
\tableofcontents

一级标题用：\section{}
二级标题用：\subsection{}
三级标题用：\subsubsection{}
自己拟定的标题：\textbf{}

换页:\newpage
加粗：\textbf{这是加粗文本}
斜体：\textit{这是斜体文本}
下划线：\underline{这是下划线文本}

Latex的换行：![[Pasted image 20260129150336.png]]
在你想换行的文字之间要有明显的空行，你在编译器空出多少行，==都只会换一行==

无缩进换行，就在文字末尾加双" \\"，
带缩进换行，在文字末尾 双"\\"的基础上\indent
上面两种换行都不带段间距
只有空行的，才带段间距

有序列表：![[Pasted image 20260129151051.png]]
\begin{itemize}
	\item 第一点内容
	\item 第二点内容
	\item 第三点内容
	\begin{itemize} % 嵌套列表
		\item 子点1
		\item 子点2
	\end{itemize}
\end{itemize}

无序列表：![[Pasted image 20260129151113.png]]
\begin{enumerate}
	\item 第一步
	\item 第二步
	\item 第三步
	\begin{enumerate} % 嵌套列表
		\item 子步骤1
		\item 子步骤2
	\end{enumerate}
\end{enumerate}

描述性列表：![[Pasted image 20260129152216.png]]
\begin{description}
	\item[关键词1] 描述内容1
	\item[关键词2] 描述内容2
	\item[关键词3] 描述内容3
\end{description}

插入图片：首先先把图片放在Figure文件夹里面，然后直接拖进去，Overleaf也是一样
![[Pasted image 20260129152403.png]]

然后你会发现：![[Pasted image 20260129153225.png]]
原本用文字包裹的图片，现在被挤到了文字后面
![[Pasted image 20260129153318.png]]
解决方法就是在{figure}后面+[H]

插入表格：
\begin{table}[htbp]% 表格环境
	\centering % 表格居中
	\caption{表格标题} % 表格标题
	\label{tab:example} % 表格标签，用于引用
	\begin{tabular}{lcr} % 表格内容 
		列1 & 列2 & 列3 \\
		数据1 & 数据2 & 数据3 \\ 
		数据4 & 数据5 & 数据6 \\ 
	\end{tabular}
\end{table}
列格式可以这样设置：lcr左中右
![[Pasted image 20260129154538.png]]
没有线段，那么我们在表格内容里面+\toprule
三线表就再加上+\midrule和+\bottomrule
在文字里面的公式用：一对美元符号
独立成行的公式用：两对美元符号