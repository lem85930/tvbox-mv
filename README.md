# tvbox-mv
mv视频搜索服务

# 请求接口
http://localhost:7777/mv/search?maxCount=100&query=五月天后来的我们

请求参数定义
~~~
query ：搜索值，mv名称或者歌手名 都可以
maxCount：最大返回值，返回结果里面 list 最大数量。 最大值1000
~~~
返回参数结果
~~~
{
  "query": "五月天后来的我们",
  "totalHits": 2511,
  "list": [
    {
      "name": "五月天-后来的我们",
      // 歌曲名
      "songName": "后来的我们",
      // 歌手名
      "songUser": "五月天",
      // mv视频url
      "url": "http://em.21dtv.com/songs/60125089.mkv",
      // 匹配分数，越高越好
      "score": 12.460263
    },
    {
      "name": "五月天-我们",
      "songName": "我们",
      "songUser": "五月天",
      "url": "http://em.21dtv.com/songs/60045770.mkv",
      "score": 8.842199
    }
  ]
}
~~~


# TvBox配置
~~~ json
{
  "sites": [
    {
      "key": "MV_vod",
      "name": "👀┃MV┃视频",
      "type": 1,
      "api": "http://你自己域名:7777/mv/vod",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    }
  ]
~~~


## 感谢
### 直播MV来源：
小武哥 ：https://t.me/BoBaiBroo

直播文件：https://t.me/fongmi_offical/54024/244800