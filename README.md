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