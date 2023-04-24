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
| multi-term-term-send-backward-kill-word | <C-backspace> |
| multi-term-term-send-backward-kill-word | <M-backspace> |
| multi-term-term-send-reverse-search-history | M-r |
| multi-term-term-send-delete-word | M-d |
| multi-term-term-send-raw | M-, |
| multi-term-comint-dynamic-complete | M-. |