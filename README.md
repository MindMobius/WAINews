# WAINews
该项目致力于使用户即便脱离外语环境，也能在真实语境中理解外语且能应用外语，而不是盲目的背单词和语法。项目使用新闻热点内容，通过使用外语替换一部分原始内容，让用户在阅读新闻热点的同时，还能够学到地道的外语表达，营造出一种本地化的外语环境，既不会脱离用户的生活环境，又能学到地道外语，还能了解新闻热点，多赢。

## 项目介绍
通过访问api，获取热点新闻数据（title、url），然后遍历访问url，获取具体新闻内容。
将最后汇总的新闻内容分类（政治、科技、娱乐、生活等），每种分类选择一篇内容作为素材。
选中的素材会展示在网站上，用户可以调整外语等级（目前只支持英文），外语等级从0到3，级别越高，新闻内容中外语含量越高。
0级就是原文，1级会在文章中替换基础外语词汇，2级会替换句子，3级替换段落。
用户可以随时点击替换的外语部分，查看对应的原文。

## 项目技术栈
使用Astro

## 开发
### 新闻获取api
https://newsnow.906051999.xyz/api/s?id=weibo

### 返回数据格式参考
```
{
  "status": "success",
  "id": "weibo",
  "updatedTime": 1746546443020,
  "items": [
    {
      "id": "斯凯奇宣布退市",
      "title": "斯凯奇宣布退市",
      "extra": {
        "icon": {
          "url": "/api/proxy/img.png?type=encodeURIComponent&url=https%3A%2F%2Fsimg.s.weibo.com%2Fmoter%2Fflags%2F2_0.png",
          "scale": 1.5
        }
      },
      "url": "https://s.weibo.com/weibo?q=%23%E6%96%AF%E5%87%AF%E5%A5%87%E5%AE%A3%E5%B8%83%E9%80%80%E5%B8%82%23",
      "mobileUrl": "https://m.weibo.cn/search?containerid=231522type%3D1%26q%3D%23%E6%96%AF%E5%87%AF%E5%A5%87%E5%AE%A3%E5%B8%83%E9%80%80%E5%B8%82%23&_T_WM=16922097837&v_p=42"
    },
    {
      "id": "刘畊宏方已报警",
      "title": "刘畊宏方已报警",
      "extra": {
        "icon": {
          "url": "/api/proxy/img.png?type=encodeURIComponent&url=https%3A%2F%2Fsimg.s.weibo.com%2Fmoter%2Fflags%2F2_0.png",
          "scale": 1.5
        }
      },
      "url": "https://s.weibo.com/weibo?q=%23%E5%88%98%E7%95%8A%E5%AE%8F%E6%96%B9%E5%B7%B2%E6%8A%A5%E8%AD%A6%23",
      "mobileUrl": "https://m.weibo.cn/search?containerid=231522type%3D1%26q%3D%23%E5%88%98%E7%95%8A%E5%AE%8F%E6%96%B9%E5%B7%B2%E6%8A%A5%E8%AD%A6%23&_T_WM=16922097837&v_p=42"
    },
```