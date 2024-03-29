# idiom

成语相关

可以按照汉字/声母/韵母/声调过滤成语，用来玩「[汉兜 - 汉字 Wordle](https://handle.antfu.me/?utm_source=https://shadiao.pro)」

## 成语数据

[idioms.json](./idiom.json)

原始数据来自于 [https://github.com/crazywhalecc/idiom-database](https://github.com/crazywhalecc/idiom-database)

修复了一部分开发中发现的错误拼音，现在拼音中可能还有一些不对的

## 搜索成语

### 搜索功能梳理

![成语查找.png](./成语查找.png)

### python 脚本

[search_idiom.py](./search_idiom.py)

* 搜索成语的一次性脚本
* 通过修改 INPUT_LIMIT_LIST 来标明过滤条件
* 最后会输出过滤后的成语，以及各个位置的可选汉字、声母、韵母、声调，按照频次倒序
* 打开调试模式(DEBUG = True)可以获取更多日志
* 目前所有 u、ü 相关的过滤结果不保证正确，尽量不要使用

## TODO

* [ ] 增加 html 的方式
* [ ] ü 的问题
  * 方案 1：把所有拼音中发 ü 音的 u 都改正确
  * 方案 2：找到所有拼音中标 u 但发 ü 音的情况，在 load 中做处理
