# An example of LaTex project structure
```
.\
	.\Figure
	.\Section
	main.tex
	reference.bib
	README.md
```
# An example of latex document
```
\documentclass[12pt, twocolumn, a4paper]{article}



% 插入包
\usepackage{asmath} % 插入公式
\usepackage{booktabs} % 插入表格
\usepackage{geometry} % 页面尺寸设置

\usepackage{float} % 设置图片浮动位置的宏包
\usepackage{graphicx} % 插入图片的宏包
\usepackage{subfigure} % 插入多图时用子图显示的宏包



% 页面外观设置
\setlength\topmargin{-0.5in}
\setlength\headsep{0in}
\setlength\textwidth{6.5in}
\setlength\textheight{9in}
\setlength\oddsidemargin{0in}
\setlength\evensidemargin{0in}

\geometry{papersize={20cm,15cm}}
\geometry{left=1cm,right=2cm,top=3cm,bottom=4cm}



% 标题，作者，日期
\title{%
\bf{The title} \\
\vspace{0.1in}}

\author{Author \\
University
Email
}

\date{\today}



% 正文开始
\begin{document}
\maketitle



% 目录
\tableofcontents



% 分页操作
\newpage



% 摘要
\begin{abstract}
Abstract goes here!
\end{abstract}



% 关键词
\begin{IEEEkeywords}
A, B, C, D, E.
\end{IEEEkeywords}



% Input all sections from .\Section
\input{Section/Introduction}
\input{Section/Preliminaries}
\input{Section/Methodology}
\input{Section/Future directions}
\input{Section/Conclusion}



% Section, Paragraph, Chapter, Part
\section{Section one}
\subsection{Subsection one}
\subsubsection{Subsubsection one}

\paragraph{Paragraph one}
\subparagraph{Subparagraph one}

\chapter{Chapter one}

\part{Part one}



% Lable and Cross-Reference
\lable{sec:lablename}
\lable{eq:equationname}
\ref{sec:lablename}
\eqref{eq:equationname}



% 字体设置
\textbf{加粗的字体}
\textit{倾斜的字体}
\underline{} % 下划线
\hspace{0.65em} % 行内缩进
\vspace{2ex} % 段内间隔
\emph{mainly} % 强调文字



% 单双引号
`Single quotes'
``Double quotes''



% 特殊字符，需要进行转义
\$
\%
\&
\#



% 插入特殊内容
\Rmnum{1} % 插入罗马数字
\cite{key} % 插入参考文献
\citet{key one}
\citep{key two}

\todo{add results}
\todo[color=blue!20]{fix method}

\newcommand{\commandname}[1]{\todo[color=green!40]{#1}}
\commandname{add results}



% 无序列表
\begin{itemsize}
	\item A
	\item B
	\item C
\end{itemsize}

% 有序列表
\begin{enumerate}
	\item A
	\item B
	\item C
\end{enumerate}


% 插入图
\begin{figure}[htbp]
	\centering
	\includegraphics[
		width=0.5\textwidth,
		angle=90]{image}
	\caption{\lable{fig:image}figname}
\end{figure}

Figure \ref{fig:image}



% 插入表
\begin{table}[htbp]
    \centering
    \caption{tabname}
    \begin{tabular}{\textwidth}{lcc}
        \toprule
        Column one & Column two & Column three \\
        \midrule
        a & aa & aaa \\
        b & bb & bbb \\
        \bottomrule
        c & \quad & ccc \\
        \bottomrule
    \end{tabular}
\end{table}



% 插入公式
\begin{equation}
x = \frac{-b \pm \sqrt{b^2 - 4ac}}
		{2a}
\end{equation}
where $a$, $b$ and $c$ are \ldots

\vspace{-30pt}
\begin{align}
h_{t} = \overline{\boldsymbol{A}}h_{t-1} + \overline{\boldsymbol{B}}x_{t} \\
y_{t} = \boldsymbol{C}h_{t}
\end{align}
\vspace{-30pt}

\begin{gather}  
a = b+c+d \\  
x = y+z  
\end{gather}

\[\begin{aligned}  
x ={}& a+b+c+{} \\  
&d+e+f+g  
\end{aligned}\]

\[ y= \begin{cases}
-x,\quad x\leq 0 \\
x,\quad x>0
\end{cases} \]

$equation$ % 这是行内公式
\[equation\] % 插入无编号的行间公式

caret ^ for superscripts
underscore _ for subscripts
Use curly braces {} to group superscripts and subscripts

Here are commands for Greek letters, common notation, operator, ...
\mu
\Omega
\omega
\delta

\pm
\times
\div
\cdot
\cap
\cup
\geq
\leq
\neq
\approx
\equiv

\sum_{k=1}^{n}
\prod_{i=1}^{n}
\lim_{x\to0}x^2
\int_a^b x^2 dx
\iint
\iiint
\iiiint
\idotsint
\sqrt{*}
\frac{A}{B} % A为分子，B为分母

()
[]
\{\}
\lvert\rvert
\lVert\rVert
\big
\Big
\bigg
\Bigg

\dots % 用于有下标的序列
\cdots
\vdots
\ddots

\[ \begin{pmatrix} a&b\\c&d \end{pmatrix} \quad  
\begin{bmatrix} a&b\\c&d \end{bmatrix} \quad  
\begin{Bmatrix} a&b\\c&d \end{Bmatrix} \quad  
\begin{vmatrix} a&b\\c&d \end{vmatrix} \quad  
\begin{Vmatrix} a&b\\c&d \end{Vmatrix} \]
$ ( \begin{smallmatrix} a&b\\c&d \end{smallmatrix} ) $



% 声明参考文献格式与参考文献库
\bibliographystyle{IEEEtran}
\newpage
\bibliography{reference}



% 插入附录
\appendixpage
\addcontentsline{toc}{section}{Appendices}
\appendix
\chapter{Supporting Information}
\section{Formulation}
\section{Dataset Analysis}
\chapter{Additional Prediction and Simulation Results}



\end{document}
```
# An example of .bib file(bibtex database format)
```
@inproceedings{chen2019cooper,
  title={Cooper: Cooperative perception for connected autonomous vehicles based on 3d point clouds},
  author={Chen, Qi and Tang, Sihai and Yang, Qing and Fu, Song},
  booktitle={2019 IEEE 39th International Conference on Distributed Computing Systems (ICDCS)},
  pages={514--524},
  year={2019},
  organization={IEEE}
}

@misc{liu2020who2com,
      title={Who2com: Collaborative Perception via Learnable Handshake Communication}, 
      author={Yen-Cheng Liu and Junjiao Tian and Chih-Yao Ma and Nathan Glaser and Chia-Wen Kuo and Zsolt Kira},
      year={2020},
      eprint={2003.09575},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}

@article{hu2022where2comm,
  title={Where2comm: Communication-efficient collaborative perception via spatial confidence maps},
  author={Hu, Yue and Fang, Shaoheng and Lei, Zixing and Zhong, Yiqi and Chen, Siheng},
  journal={Advances in neural information processing systems},
  volume={35},
  pages={4874--4886},
  year={2022}
}
```