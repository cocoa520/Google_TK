Google TK参数 
============

几个月前，google统一修改了Google API的调用接口，导致很多接口失效，其中有歌曲封面搜索、在线翻译接口，查了下原因，竟然是变成收费了的，看来Google也是差钱用了，虽然花钱购买服务是合情合理的，但是作为一名不富裕的程序员，还是要自己动手了。

通过抓包分析[http://translate.google.cn](http://translate.google.cn)的访问，发现其中有一个tk参数比较难搞，无奈之下，硬着头皮分析混淆过的js代码，生成tk的js链接为[desktop_module_main.js](http://translate.google.cn/translate/releases/twsfe_w_20151214_RC03/r/js/desktop_module_main.js)，花了一个晚上终于将tk参数的生成提取出来，测试能够正常使用，现在分享出来给大家参考，有兴趣的也可以自己分析，得多花点时间和耐心。

备注：Google又作了小的调整，已完成修改。
