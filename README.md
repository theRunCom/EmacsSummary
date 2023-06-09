<img src="./pics/EmacsIcon.png" align="right" width="200px" height="200px"/>

# EmacsSummary🏄

Emacs是一款自由软件，它是一款可扩展、自定义的文本编辑器。Emacs在1976年由Richard Stallman开发，并于1984年发布了GNU Emacs，现在由GNU项目维护。Emacs的特点是可以通过Lisp编程语言进行扩展，使得用户可以自定义编辑器的行为和功能。Emacs是一款非常强大的文本编辑器，它的强大功能和扩展性使得它成为了众多程序员的首选。

> An extensible, customizable, free/libre text editor  and more.

🫶我目前使用的配置是这位开发者的配置：[M-EMACS, a full-featured GNU Emacs configuration distribution](https://github.com/MatthewZMD/.emacs.d)

## 启动

图形界面可以直接打开程序。命令行输入命令启动 Emacs。

```bash
emacs
```

如果想要打开非图形界面版的 Emacs，输入：

```bash
emacs -nw # no window system
```

## Emacs学习资料

[org-mode简明教程笔记](https://github.com/EvanMeek/Learn-Org/blob/master/org-note.org)

[Emacs Lisp 简明教程](http://smacs.github.io/elisp/)

[配置指南](https://nyk.ma/posts/emacs-write-your-own/)

[Emacs Markdown-mode Cheat Sheet](https://cheatography.com/xaon/cheat-sheets/emacs-markdown-mode/)



## 关于键盘操作

| Emacs 功能键 | 缩写 | 对应键盘按键(PC/Mac) |
| --- | --- | --- |
| Control |	C |	Ctrl / Control |
| Meta  | M	| Alt / Option |
| Shift | S	| Shift / Shift |
| Super | s	| Win / Command |

| 操作描述 | 快捷键 | 命令名 |
| --- | --- | --- |
| 输入命令 | M-x | execute-extended-command |
| 退出程序 | C-x C-c | save-buffers-kill-terminal |
| 放弃当前输入 | C-g | keyboard-quit |
| 光标向上一行（方向键上） | C-p | previous-line |
| 光标向下一行（方向键下） | C-n | next-line |
| 光标向左一个字符（方向键左） | C-b | backward-char |
| 光标向右一个字符（方向键右） | C-f | forward-char |
| 光标向左移动一个词 | M-b | backward-word |
| 光标向右移动一个词 | M-f | forward-word |
| 光标移至行首 | C-a | move-beginning-of-line |
| 光标移至行尾 | C-e | move-end-of-line |
| 光标移动到一行缩进的开头 | M-m | back-to-indentation |
| 光标移至句首 | M-a | backward-sentence |
| 光标移至句尾 | M-e | forward-sentence |
| 光标移至文件开头 | M-< | beginning-of-buffer |
| 光标移至文件结尾 | M-> | end-of-buffer |
| 光标移动至窗口的中间、最上、最下 | M-r | move-to-window-line-top-bottom |
| 删除光标右侧字符 | C-d | delete-char |
| 移除光标右侧词 | M-d | kill-word |
| 移除光标左侧词 | M- | backward-kill-word |
| 移除右侧直到句子结尾 | M-k | kill-sentence |
| 移除右侧直到行尾 | C-k | kill-line |
| 设置标记以选择区域 | C-SPC | set-mark-command |
| 复制区域 | M-w | kill-region-save |
| 移除区域 | C-w | kill-region |
| 插入已移除文本 | C-y | yank |
| 插入历史移除文本 | M-y | yank-pop |
| 撤回 | C-/ 或 C-_ 或 C-x u | undo |
| 跳转到上一标记 | C-x C-SPC 或 C-u C-SPC | pop-global-mark |
| 跳转到行号 | M-g M-g | goto-line |
| 重复 | C-u | universal-argument |
| 向下一页 | C-v | scroll-up-command |
| 向上一页 | M-v | scroll-down-command |
| 移动页面使得光标在中央/最上方/最下方 | C-l | recenter-top-bottom |
| 向后搜索 | C-s | isearch-forward |
| 向前搜索 | C-r | isearch-backward |
| 交换前后字符 | C-t | transpose-chars |
| 交换前后词 | M-t | transpose-words |
| 交换前后两行 | C-x C-t | transpose-lines |
| 在下方新建一行 | C-o | open-line |
| 删除连续空行为一个空行 | C-x C-o | delete-blank-lines |
| 将后面的词变为小写 | M-l | downcase-word |
| 将后面的词变为大写 | M-u | upcase-word |
| 将后面的词变为首字母大写 | M-c | capitalize-word |
| 放大字号 | C-x C-= | text-scale-adjust |
| 缩小字号 | C-x C-- | text-scale-adjust |
| 重置字号 | C-x C-0 | text-scale-adjust |
| 简要描述快捷键功能 | C-h c | describe-key-briefly |
| 描述快捷键功能 | C-h k | describe-key |
| 描述函数功能 | C-h f | describe-function |
| 描述变量 | C-h v | describe-variable |
| 列出含某一关键词的命令 | C-h a | apropos-command |
| 列出含某一关键词的符号的文档 | C-h d | apropos-documentation |
| 帮助的帮助 | C-h ? | help-for-help |

## 关于M-EMACS

M-EMACS 是一个自定义的 GNU Emacs 安装和配置分发版本，旨在增强默认的 Emacs 使用体验。

### .emacs.d/early-init.el

early-init.el 是在 init.el 等文件之前运行的文件。作者这里为了运行的速度，进行了一些优化，设置了垃圾回收gc的阈值及关闭一些不必要的功能。

### .emacs.d/init.el

Emacs在启动时会加载init.el文件，并根据其中的配置进行初始化。

### .emacs.d/elisp/init-package.el

- 将镜像源进行修改，获取更快的下载速度。
```elisp
(setq package-user-dir (expand-file-name "elpa" user-emacs-directory)
      package-archives
      '(;;("gnu"   . "https://elpa.gnu.org/packages/")
        ;;("melpa" . "https://melpa.org/packages/")
        ("cselpa" . "https://elpa.thecybershadow.net/packages/")
        ("melpa-cn" . "http://mirrors.cloud.tencent.com/elpa/melpa/")
        ("gnu-cn"   . "http://mirrors.cloud.tencent.com/elpa/gnu/")
        ))
```

- 添加代理(更换对应的地址与端口)：
```elisp
;; (setq url-proxy-services
         ;; '(("http"  . "172.24.64.1:7890")
    	;; ("https" . "172.24.64.1:7890")))

```

- 使用[use-package](https://github.com/jwiegley/use-package)进行包管理

- 包自动更新

- 从 mode-line 中去除某些次要模式

### .emacs.d/elisp/init-avy.el

Avy是Emacs编辑器中一个快速跳转工具。它可以帮助用户快速浏览和跳转到文本缓冲区中的某个位置，从而提高编辑效率。Avy可以将全局的跳转操作对应到一个速记选择器（shortcut），然后通过选择对应的速记选择器，快速移动到缓冲区中的相应位置。

- avy-goto-char-timer 的作用是快速跳转到当前编辑文本中某个字符出现的位置。它和avy-goto-char 类似，但它会在按下按键后自动进入计时模式，列出候选项并根据您输入的字符筛选缩小候选项范围，当计时器到达 Timeout 时间时就会自动跳转。

- avy-goto-line 的作用是快速跳转到文本的某一行。它使用类似于上面的命令，但是不是输入字符，而是输入行号。此命令可以在当前缓冲区中快速跳转到指定行，并可以缩小可能的行号。这在编辑大型文本文件时特别有用。

| 功能 | 按键 |
| --- | --- |
| avy-goto-char-timer | C-z c |
| avy-goto-line | C-z l |

### .emacs.d/elisp/init-crux.el

Crux是一个实用工具函数集合，为了提高使用Emacs编辑器时的效率而构建。

- crux-move-beginning-of-line 函数使光标在当前行的开头和第一次调用之间切换。如果光标已经在行的开头，则将其移动到原始光标位置之前的非空字符。

- crux-transpose-windows 函数使当前窗口与其旁边的窗口直接的文本互换。

- crux-kill-other-buffers 函数关闭所有缓冲区，并且保留当前活动缓冲区。当您需要关闭Emacs中打开的所有文件时，这非常有用。注意，它不关闭任何Emacs的Minibuffer。

- crux-cleanup-buffer-or-region：删除空行、行尾空格以及注释、多余的空行等，进行编码格式化。

| 功能 | 按键 |
| --- | --- |
| crux-move-beginning-of-line | C-a |
| crux-transpose-windows | C-x 4 t |
| crux-kill-other-buffers | C-x K |
| crux-smart-kill-line | C-k |

 ### .emacs.d/elisp/init-dired.el

 Dired是Emacs中的一个模式，它允许您浏览和管理文件系统。您可以使用Dired执行各种文件管理操作，如复制、移动、删除和重命名文件。

 - dired-jump: 快速跳转到当前文件所在的目录。

| 功能 | 按键 |
| --- | --- |
| dired-jump | C-x C-j | 

Dired模式:
| 功能 | 按键 |
| --- | --- |
| 打开鼠标指针指向的文件或目录 | <mouse-2> |
| 打开所选文件或目录 | RET |
| 执行返回上一级目录的操作 | ^ |

Disk Usage,是一种文件系统分析工具，提供按大小排序的文件列表表格视图。

| 功能 | 按键 |
| --- | --- |
|  save-all-buffers | C-x C-s |

### .emacs.d/elisp/init-winner.el

winner允许您轻松切换窗口的大小和位置，以及撤消窗口分割等操作。winner 的工作原理类似于后退和前进浏览器的历史记录。在此基础上，它允许您定义哪些 Buffer 不会导致新的窗口布局被记录，从而帮助您获得更好的 Buffers 管理。

### .emacs.d/elisp/init-which-key.el

which key可以在您当前输入的不完整命令（前缀）后显示按键绑定。

### .emacs.d/elisp/init-popup-kill-ring.el

popup-kill-ring，它用于显示 Emacs 中所有剪贴板历史记录的列表，并允许用户选择要粘贴的剪贴板内容。这些历史记录包括之前复制或剪切的所有文本或图像，而不仅仅是最新的一次复制或剪切。

| 功能 | 按键 |
| --- | --- |
| popup-kill-ring | M-y |

### .emacs.d/elisp/init-undo-tree.el

undo-tree-visualizer-diff，允许您在撤消/重做树的可视化视图中看到不同版本之间的差异。

undo-tree-history-directory-alist，设置为一个由一个 key-value 对组成的链表，其中的 key 可以是用来匹配文件名，value 表示撤消历史文件保存的目录。

undo-tree-visualizer-timestamps，允许您在撤销/重做树的可视化视图中看到每个撤销/重做历史条目的时间戳信息。

### .emacs.d/elisp/init-discover-my-major.el

discover-my-major，提供了一种方便的方式来查看当前 Emacs 所支持的所有主要模式。

| 功能 | 按键 |
| --- | --- |
| discover-my-major | C-h C-m |

### .emacs.d/elisp/init-ace-window.el

ace-window，选择要切换的窗口

| 功能 | 按键 |
| --- | --- |
| ace-window | C-x C-o |

### .emacs.d/elisp/init-shell.el

关于终端使用

term-interrupt-subjob：用于终止当前的子进程

term-send-esc：用于将通常用于触发 Meta 命令的 ESC 键发送到终端

previous-line：在终端中向上滚动一行

next-line：在终端中向下滚动一行

term-send-return：发送回车符

term-paste：将剪贴板中的内容粘贴到终端

scroll-up-command：向上滚动终端

scroll-down-command：向下滚动终端

term-send-forward-word：向前跳到下一个单词

term-send-backward-word：向后跳到上一个单词

term-send-backspace：向后删除一个字符

term-send-up：向上滚动终端历史记录

term-send-down：向下滚动终端历史记录

term-send-forward-kill-word：删除当前光标位置到下一个单词的内容

term-send-backward-kill-word：删除当前光标位置到上一个单词的内容

term-send-reverse-search-history：向上搜索匹配的历史记录项

term-send-delete-word：删除当前光标位置到下一个单词的内容

term-send-raw：将当前按键发送到终端

comint-dynamic-complete：自动完成终端命令

| 功能 | 按键 |
| --- | --- |
| aweshell | M-# |
| shell-here | M-~ |
| multi-term | M-$ |
| multi-term-term-interrupt-subjob | C-c C-c |
| multi-term-term-send-esc | C-c C-e |
| multi-term-previous-line | C-p |
| multi-term-next-line | C-n |
| multi-term-term-send-return | C-m |
| multi-term-term-paste | C-y |
| multi-term-scroll-up-command | C-v |
| multi-term-scroll-down-command | M-v |
| multi-term-term-send-forward-word | M-f |
| multi-term-term-send-backward-word | M-b |
| multi-term-term-send-backspace | M-o |
| multi-term-term-send-up | M-p |
| multi-term-term-send-down | M-n |
| multi-term-term-send-forward-kill-word | M-M |
| multi-term-term-send-backward-kill-word | M-N |
| multi-term-term-send-backward-kill-word | < C-backspace > |
| multi-term-term-send-backward-kill-word | < M-backspace > |
| multi-term-term-send-reverse-search-history | M-r |
| multi-term-term-send-delete-word | M-d |
| multi-term-term-send-raw | M-, |
| multi-term-comint-dynamic-complete | M-. |

### .emacs.d/elisp/init-buffer.el

| 功能 | 按键 |
| --- | --- |
| 打开ibuffer | C-x C-b |

### .emacs.d/elisp/init-func.el

调整窗口宽度/高度

| 功能 | 按键 |
| --- | --- |
| resize-window-width | C-z w |
| resize-window-height | C-z h |
| window-width-increase | M-W = |
| window-width-increase | M-W M-+ |
| window-width-decrease | M-W - |
| window-width-decrease | M-W M-_ |
| window-height-increase | M-E = |
| window-height-increase | M-E M-+ |
| window-height-decrease | M-E - |
| window-height-decrease | M-E M-_ |

编辑此配置文件的快捷方式

| 功能 | 按键 |
| --- | --- |
| edit-configs | C-z e |

### .emacs.d/elisp/init-theme.el

Doom Themes 和 Doom Modeline 相关配置

### .emacs.d/elisp/init-dashboard.el

Dashboard 启动面板

| 功能 | 按键 |
| --- | --- |
| open-dashboard | C-z d |

Page Break Lines 该插件能将丑陋的分页符字符显示为整洁的横线

### .emacs.d/elisp/init-magit.el

Magit是一个Emacs的Git客户端，它提供了一种更好的方式来使用Git。Magit提供了一个交互式的界面，可以让你更容易地查看和管理你的Git存储库。Magit还提供了一些有用的功能，例如在提交之前查看差异，合并分支，重置提交等

| 功能 | 按键 |
| --- | --- |
| magit-status | C-x g |
| magit-diff-visit-file-other-window | M-RET |

### .emacs.d/elisp/init-projectile.el

Projectile是一个Emacs的插件，它提供了项目管理的功能，可以让你在一个项目中快速地切换文件，查找文件，以及在项目中执行命令。它可以自动地识别项目的根目录，并且可以在项目中搜索文件，而不需要你手动指定根目录。

projectile-command-map: 打开 Projectile 的命令列表

| 功能 | 按键 |
| --- | --- |
| projectile-command-map | C-c p |

### .emacs.d/elisp/init-yasnippet.el

YASnippet是一个用于Emacs的模板系统，它可以让你在编写代码时快速输入常用的代码块。例如，你可以定义一个模板，当你输入“for”时，它会自动展开为一个for循环的代码块。YASnippet还支持变量和嵌套代码块，这使得它非常灵活和强大

| 功能 | 按键 |
| --- | --- |
| yas-expand-from-trigger-key | C-c C-n |

### .emacs.d/elisp/init-syntax.el

Flycheck是一个Emacs的语法检查工具，它可以在你编辑代码时自动检查语法错误，并在编辑器中显示错误信息。

Flyspell是一个Emacs的拼写检查工具，它可以在你编辑代码时自动检查拼写错误，并在编辑器中显示错误信息。

### .emacs.d/elisp/init-dump-jump.el

Dumb Jump--"jump to definition" 

- dumb-jump-go 命令用于跳转到光标下的定义位置。如果有多个定义位置，可以使用 dumb-jump-selector 指定选择器选择具体的跳转目标。
- dumb-jump-go-other-window 命令与 dumb-jump-go 命令类似，不同的是跳转到的位置会在新的窗口中打开。
- dumb-jump-go-prompt 命令用于在 minibuffer 中提示用户输入要跳转的符号名称，然后跳转到该名称的定义位置。

| 功能 | 按键 |
| --- | --- |
| dumb-jump-go-other-window | C-c C-o |
| dumb-jump-go | C-c C-j |
| dumb-jump-go-prompt | C-c C-i |

### .emacs.d/elisp/init-parens.el

Smartparens 处理pairs

- sp-forward-sexp，将光标向前移动到当前平衡表达式（sexp）的末尾。如果光标已经在当前sexp的末尾，则将光标移动到下一个sexp的末尾。
- sp-backward-sexp，将光标向后移动到当前平衡表达式的开头。如果光标已经在当前sexp的开头，则将光标移动到上一个sexp的开头。
- sp-backward-down-sexp，将光标向后移动到当前sexp的外层sexp的开头。
- sp-up-sexp，将光标向后移动到当前sexp的外层sexp的末尾。
- sp-copy-sexp，将当前sexp复制到剪贴板。
- sp-change-enclosing，用另一对括号（或其他字符）替换当前sexp的括号。
- sp-kill-sexp，删除当前sexp。
- sp-splice-sexp-killing-backward，将当前sexp和前一个sexp合并在一起，并删除前一个sexp的括号。
- sp-splice-sexp-killing-around，将当前sexp和它的外层sexp合并在一起，并删除它的外层括号。
- sp-select-next-thing-exchange，选择下一个括号、引号或其他字符，并将其与当前sexp交换位置。 

| 功能 | 按键 |
| --- | --- |
| sp-forward-sexp | C-M-f |
| sp-backward-sexp | C-M-b |
| sp-up-sexp | C-M-e |
| sp-backward-down-sexp | C-M-a |
| sp-copy-sexp | C-M-w |
| sp-change-enclosing | C-M-k |
| sp-kill-sexp | M-k |
| sp-splice-sexp-killing-backward | C-M-< backspace > |
| sp-splice-sexp-killing-around | C-S-< backspace > | 
| sp-select-next-thing-exchange | C-] |

Match Parenthesis 自动匹配括号

### .emacs.d/elisp/init-indent.el

Highlight Indent Guides 高亮缩进级别

### .emacs.d/elisp/init-quickrun.el

Quickrun 快速编译和运行源代码

| 功能 | 按键 |
| --- | --- |
| quickrun | < f5 > 或 C-c e |
| quickrun-shell | M-< f5 > 或 C-c C-e |

### .emacs.d/elisp/init-format.el

Format all, auto-format source code

[Supported Languages](https://github.com/lassik/emacs-format-all-the-code#supported-languages)

| 功能 | 按键 |
| --- | --- |
| format-all-buffer | C-c C-f |

Ediff, 对比和合并工具。它可以对比并编辑两个文件之间的差异,也可以三向对比多个文件。

`M-x ediff`

Evil Nerd Commenter，一种帮助您高效注释代码的工具。

- c-toggle-comment-style，切换注释风格

- evilnc-comment-or-uncomment-lines，either comment or uncomment the selected line

| 功能 | 按键 |
| --- | --- |
| c-toggle-comment-style | C-c M-; |
| evilnc-comment-or-uncomment-lines | M-; |

### .emacs.d/elisp/init-edit.el

Iedit是一种次要模式，可以在缓冲区或区域中同时编辑多个区域。

| 功能 | 按键 |
| --- | --- |
| iedit-mode | C-z |

Awesome Pair可以提供语法括号自动补全。

- awesome-pair-kill，如果光标在两个括号之间，如此：(光标)，调用 awesome-pair-kill 将删除两个括号并使光标变为空。如果光标在任何括号之外，调用 awesome-pair-kill 将简单地删除光标下的字符。

- awesome-pair-space，插入一个空格字符并自动添加相应的括号或引号对。

- awesome-pair-equal，插入一个等号 "=" 字符并自动添加相应的括号或引号对。

- awesome-pair-jump-right，将使光标向右移动到下一个括号、方括号或引号对的右侧。

- awesome-pair-jump-left，将使光标向左移动到上一个括号、方括号或引号对的左侧。

| 功能 | 按键 |
| --- | --- |
| awesome-pair-kill | M-D |
| awesome-pair-space | SPC |
| awesome-pair-equal | = |
| awesome-pair-jump-right | M-F |
| awesome-pair-jump-left | M-B |

Delete Block，有效快速删除块的功能。

- delete-block-forward，删除光标所在位置到下一个空行或代码块结束位置的所有内容。

- delete-block-backward，删除光标所在位置到上一个空行或代码块开始位置的所有内容。

| 功能 | 按键 |
| --- | --- |
| delete-block-forward | M-d |
| delete-block-backward | C-< backspace > or M-< backspace > or M-DEL |

### .emacs.d/elisp/init-header.el

Header2，用于创建和更新文件头的支持。在 Emacs Lisp 编程模式下自动添加文件头部信息。

### .emacs.d/elisp/init-ein.el

a Jupyter (formerly IPython) client in Emacs.

- Execute M-x ein:run to launch a local Jupyter session

- Login with M-x ein:login to a local or remote session

| 功能 | 按键 |
| --- | --- |
| ein:worksheet-execute-cell | C-c e |
| ein:worksheet-execute-all-cells | C-c C-e |

### .emacs.d/elisp/init-lsp.el

### .emacs.d/elisp/init-company.el

Company是一款Emacs的文本自动填充框架。

Company TabNine，是支持所有语言自动补全的TabNine的company-mode后端。

