# flypy-clover

结合rime小鹤双拼和[clover](https://github.com/fkxxyz/rime-cloverpinyin)词库的开箱即用的配置文件。

1. 从[clover](https://github.com/fkxxyz/rime-cloverpinyin)引入的拼音和基础词库，导入了几个很好用的词库：

   - 用 [pypinyin](https://github.com/mozillazg/python-pinyin) 项目生成所有字词的拼音
   - 合并[结巴中文分词](https://github.com/fxsjy/jieba)项目、[rime八股文](https://github.com/rime/rime-essay)和[袖珍简化字拼音](https://github.com/rime/rime-pinyin-simp)的字的字频
   - 由百度搜索到某个人基于大数据做过的[360万中文词库+词性+词频](https://download.csdn.net/download/xmp3x/8621683)，该词库是用ansj分词对270G新闻语料进行分词统计词频获得
   - [清华大学开源词库](https://github.com/thunlp/THUOCL)，统计来自各大主流网站如CSDN博客、新浪新闻、搜狗语料
   - 搜狗细胞词库 [网络流行新词【官方推荐】](https://pinyin.sogou.com/dict/detail/index/4)

## Install

1. Install fcitx5 and rime

```shell
# I use arch
yay fcitx5 fcitx5-configtool fcitx5-rime
```
- fcitx5: main package for fcitx5
- fcitx5-configtool: GUI to configure fcitx5 
- fcitx5-rime: rime binding for fcitx5

2. copy all file into `~/.local/share/fcitx5/rime`

```shell
cd ~/.local/share/fcitx5
rm -rf rime
git clone https://github.com/dingiso/flypy-clover rime
# optional
cd rime 
rm -rf .git
```

3. open fcitx5, switch to rime, and wait for sync
