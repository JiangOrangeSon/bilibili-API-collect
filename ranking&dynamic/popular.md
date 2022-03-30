# （当前）热门视频

---

> https://api.bilibili.com/x/web-interface/popular

*请求方式：GET*

**url参数：**

| 参数名 | 类型 | 内容        | 必要性 | 备注    |
| ------ | ---- | ----------- | ------ | ------- |
| pn     | num  | 页码        | 非必要 | 默认为1（最大值4） |
| ps     | num  | 每页项数    | 非必要 | 默认为20（最大值50） |

**json回复：**

根对象：

| 字段    | 类型 | 内容     | 备注                        |
| ------- | ---- | -------- | --------------------------- |
| code    | num  | 返回值   | 0：成功<br />-400：请求错误 |
| message | str  | 错误信息 | 默认为0                     |
| ttl     | num  | 1        |                             |
| data    | obj  | 信息本体 |                             |

`data`对象：

| 字段     | 类型   | 内容     | 备注 |
| -------- | ------ | -------- | ---- |
| list | array | 视频列表 |      |
| no_more     | bool    | 是否有下一页 | 默认为false：有下一页  |

`data`中的`list`数组：

| 项   | 类型 | 内容      | 备注 |
| ---- | ---- | --------- | ---- |
| 0    | obj  | 视频1     |      |
| n    | obj  | 视频(n+1) |      |
| ……   | obj  | ……        | ……   |

`data`中的`list`数组中的对象：

基本同[获取视频详细信息（web端）](/video/info.md#获取视频详细信息（web端）)中的data对象

**示例：**

获取当前热门中的前20个视频信息

```shell
curl -G 'https://api.bilibili.com/x/web-interface/popular' \
--data-urlencode 'ps=20' \
--data-urlencode 'pn=1' \
-b 'SESSDATA=xxx'
```

<details>
<summary>查看响应示例：</summary>

```json
{
    "code": 0,
    "message": "0",
    "ttl": 1,
    "data": {
        "list": [
            {
                "aid": 425182036,
                "videos": 1,
                "tid": 137,
                "tname": "明星综合",
                "copyright": 1,
                "pic": "http://i0.hdslb.com/bfs/archive/d748971319a5a494ab98b257b780413b016ddaca.jpg",
                "title": "我来B站“卖瓜”了！",
                "pubdate": 1648465396,
                "ctime": 1648465396,
                "desc": "瓜摊老板李广奇入驻b站啦！",
                "state": 0,
                "duration": 91,
                "rights": {
                    "bp": 0,
                    "elec": 0,
                    "download": 0,
                    "movie": 0,
                    "pay": 0,
                    "hd5": 0,
                    "no_reprint": 1,
                    "autoplay": 1,
                    "ugc_pay": 0,
                    "is_cooperation": 0,
                    "ugc_pay_preview": 0,
                    "no_background": 0
                },
                "owner": {
                    "mid": 1528617278,
                    "name": "演员李广奇",
                    "face": "http://i2.hdslb.com/bfs/face/1678614672909b204adc9016f8adefdb1891915b.jpg"
                },
                "stat": {
                    "aid": 425182036,
                    "view": 7029197,
                    "danmaku": 15591,
                    "reply": 34788,
                    "favorite": 114598,
                    "coin": 353820,
                    "share": 80645,
                    "now_rank": 0,
                    "his_rank": 1,
                    "like": 961822,
                    "dislike": 0
                },
                "dynamic": "",
                "cid": 561219907,
                "dimension": {
                    "width": 3840,
                    "height": 2160,
                    "rotate": 0
                },
                "short_link": "https://bili2233.cn/BV1g3411W7ye",
                "short_link_v2": "https://bili2233.cn/BV1g3411W7ye",
                "first_frame": "http://i2.hdslb.com/bfs/storyff/n220328a22yqj07sjoetw61xl3wz2a3i_firsti.jpg",
                "bvid": "BV1g3411W7ye",
                "season_type": 0,
                "is_ogv": false,
                "ogv_info": null,
                "rcmd_reason": {
                    "content": "百万播放",
                    "corner_mark": 0
                }
            },
            {
                "aid": 510131240,
                "videos": 1,
                "tid": 138,
                "tname": "搞笑",
                "copyright": 1,
                "pic": "http://i2.hdslb.com/bfs/archive/106920be6df92da9d7bc41a0f49acc0ebb428d5f.jpg",
                "title": "《梗王之王》多少梗，快来快来数一数，24678...",
                "pubdate": 1648556536,
                "ctime": 1648555908,
                "desc": "谭sir、二仙桥大爷与演员李广奇一起卖瓜，携手登台，进军娱乐圈。B站站友用爱发电，助力三位五旬老者，挑战金鸡、百花、柏林、戛纳。",
                "state": 0,
                "duration": 350,
                "mission_id": 517586,
                "rights": {
                    "bp": 0,
                    "elec": 0,
                    "download": 0,
                    "movie": 0,
                    "pay": 0,
                    "hd5": 1,
                    "no_reprint": 1,
                    "autoplay": 1,
                    "ugc_pay": 0,
                    "is_cooperation": 1,
                    "ugc_pay_preview": 0,
                    "no_background": 0
                },
                "owner": {
                    "mid": 330415548,
                    "name": "谭乔",
                    "face": "http://i0.hdslb.com/bfs/face/42efc41c022661fa3a8a4f87d5e4c34f956f5a66.jpg"
                },
                "stat": {
                    "aid": 510131240,
                    "view": 3905851,
                    "danmaku": 8826,
                    "reply": 4047,
                    "favorite": 41882,
                    "coin": 79950,
                    "share": 23156,
                    "now_rank": 0,
                    "his_rank": 5,
                    "like": 311779,
                    "dislike": 0
                },
                "dynamic": "【华强买瓜】梦幻联动【二仙桥】 ",
                "cid": 562085474,
                "dimension": {
                    "width": 1920,
                    "height": 1080,
                    "rotate": 0
                },
                "short_link": "https://bili2233.cn/BV1Ku411B7XR",
                "short_link_v2": "https://bili2233.cn/BV1Ku411B7XR",
                "first_frame": "http://i1.hdslb.com/bfs/storyff/n220329a225ghkxjskru3q1jaf7niymu_firsti.jpg",
                "bvid": "BV1Ku411B7XR",
                "season_type": 0,
                "is_ogv": false,
                "ogv_info": null,
                "rcmd_reason": {
                    "content": "百万播放",
                    "corner_mark": 0
                }
            },
            ……
            {
                "aid": 255203977,
                "videos": 1,
                "tid": 182,
                "tname": "影视杂谈",
                "copyright": 1,
                "pic": "http://i1.hdslb.com/bfs/archive/a0b3368a4c1655be59a84dbf6b045d066029fbc7.jpg",
                "title": "廉政公署被操纵，揭秘香港警方最高权力斗争！港片警匪佳作《寒战》解读！",
                "pubdate": 1648641962,
                "ctime": 1648641962,
                "desc": "2002年，《无间道》上映，成为千禧年之后第一个十年中最具代表性的香港警匪电影。十年后2012年，《寒战》上映，媒体纷纷给出了“《无间道》之后最好警匪片”的评价。《寒战》在警匪对垒之外，花了更多笔墨去描写港警内部的权力斗争，内容本身非常具有可看性。制作上也带有“10后”明显的现代感，那它到底能不能担得起《无间道》后最好警匪片这个名头呢，咱今天就来好好唠一唠！",
                "state": 0,
                "duration": 2631,
                "mission_id": 453764,
                "rights": {
                    "bp": 0,
                    "elec": 0,
                    "download": 0,
                    "movie": 0,
                    "pay": 0,
                    "hd5": 0,
                    "no_reprint": 1,
                    "autoplay": 1,
                    "ugc_pay": 0,
                    "is_cooperation": 0,
                    "ugc_pay_preview": 0,
                    "no_background": 0
                },
                "owner": {
                    "mid": 386869863,
                    "name": "培根悖论唠唠嗑",
                    "face": "http://i0.hdslb.com/bfs/face/225b8ef554ed65ac3c5e137262a252ef4b411e64.jpg"
                },
                "stat": {
                    "aid": 255203977,
                    "view": 59185,
                    "danmaku": 966,
                    "reply": 303,
                    "favorite": 1609,
                    "coin": 3170,
                    "share": 153,
                    "now_rank": 0,
                    "his_rank": 0,
                    "like": 7995,
                    "dislike": 0
                },
                "dynamic": "这一部，被盛赞为“《无间道》之后最好警匪片”！",
                "cid": 562815691,
                "dimension": {
                    "width": 1920,
                    "height": 1080,
                    "rotate": 0
                },
                "short_link": "https://bili2233.cn/BV1nY411J7Lq",
                "short_link_v2": "https://bili2233.cn/BV1nY411J7Lq",
                "first_frame": "http://i1.hdslb.com/bfs/storyff/n220330qnmg4fmvf19a5q3h23tgk7y5i_firsti.jpg",
                "bvid": "BV1nY411J7Lq",
                "season_type": 0,
                "is_ogv": false,
                "ogv_info": null,
                "rcmd_reason": {
                    "content": "影视杂谈·人气飙升",
                    "corner_mark": 1
                }
            }
        ],
        "no_more": false
    }
}
```
