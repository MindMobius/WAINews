# WAINews
该项目致力于使用户即便脱离外语环境，也能在真实语境中理解外语且能应用外语，而不是盲目的背单词和语法。项目使用新闻热点内容，通过使用外语替换一部分原始内容，让用户在阅读新闻热点的同时，还能够学到地道的外语表达，营造出一种本地化的外语环境，既不会脱离用户的生活环境，又能学到地道外语，还能了解新闻热点，多赢。

## 项目介绍
通过RSS订阅，获取新闻链接，再遍历链接获取具体新闻内容。
将最后汇总的新闻内容分类，择优选择内容作为素材。
选中的素材会展示在网站上，用户可以调整外语等级（目前只支持英文），外语等级从0到3，级别越高，新闻内容中外语含量越高。
0级就是原文，1级会在文章中替换基础外语词汇，2级会替换句子，3级替换段落。
用户可以随时点击替换的外语部分，查看对应的原文。

## 项目技术栈
使用remix.js，通过后端请求RSS订阅地址，获取具体新闻地址，然后通过后端请求具体新闻地址，获取具体新闻内容。
然后在前端与用户设置的LLM API进行交互，挑选出适合的新闻内容，然后将新闻内容替换成对应的外语内容。

## RSS订阅地址
### 中国新闻网
即时新闻	https://www.chinanews.com.cn/rss/scroll-news.xml
要闻导读	https://www.chinanews.com.cn/rss/importnews.xml
时政新闻	https://www.chinanews.com.cn/rss/china.xml
东西问	https://www.chinanews.com.cn/rss/dxw.xml
国际新闻	https://www.chinanews.com.cn/rss/world.xml
社会新闻	https://www.chinanews.com.cn/rss/society.xml
财经新闻	https://www.chinanews.com.cn/rss/finance.xml
健康·生活	https://www.chinanews.com.cn/rss/life.xml
大湾区	https://www.chinanews.com.cn/rss/dwq.xml
华人	https://www.chinanews.com.cn/rss/chinese.xml
文娱新闻	https://www.chinanews.com.cn/rss/culture.xml
体育新闻	https://www.chinanews.com.cn/rss/sports.xml