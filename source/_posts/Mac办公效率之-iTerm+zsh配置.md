---
title: Mac办公效率之-iTerm+zsh配置
---
## 快捷键

苹果系统比较常见的单词间跳转快捷键是：

* ⌥（Alt） + ← or → 单词之间向前或者向后跳转 

* ⌘（Command） + ← or →  移到本段字符串的开始或者结尾

在zsh中通过ctrl + ← or → 可以实现跳到字符串开始或者结束，esc + W/B进行单词间的跳转。但是esc位置不是很方便，所以可以把单词间跳转的快捷键进行重新绑定。在~/.zshrc（iTerm默认打开的是zsh）中配置快捷键绑定。

在.zshrc中拷贝如下的内容：

```shell
#bindkey
bindkey "\e\e[D" backward-word
bindkey "\e\e[C" forward-word
```

这样zsh就实现了和苹果系统一样的单词间跳转功能。

