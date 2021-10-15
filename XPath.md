### XPath规则套娃（需v2.0.4及以上版本）
----
套娃依赖自定义爬虫jar，同样需要在自定义json中加入相应的配置，**type=3, api为csp_XPath**，套娃相关规则配置在`ext`字段中，注意：ext字段值**只能是json字符串**
```json
{
    "key": "csp_xpath_94sm",
    "name": "94神马(XPath)",
    "type": 3,
    "api": "csp_XPath",
    "searchable": 1,
    "quickSearch": 1,
    "filterable": 1,
    "ext": "{\r\n\t\"ua\": \"\",\r\n\t\"homeUrl\": \"http://www.9rmb.com\",\r\n\t\"cateNode\": \"//ul[contains(@class,'navbar-nav')]/li/a[contains(@href, '.html') and not(contains(@href, '6'))]\",\r\n\t\"cateName\": \"/text()\",\r\n\t\"cateId\": \"/@href\",\r\n\t\"cateIdR\": \"/type/(\\\\d+).html\",\r\n\t\"cateManual\": {},\r\n\t\"homeVodNode\": \"//div[@class='col-md-12 movie-item-out']//a[not(contains(@href, '6'))]/parent::*/parent::*/parent::*/div[contains(@class, 'movie-item-out') and position()<10]/div[@class='movie-item']/a\",\r\n\t\"homeVodName\": \"/@title\",\r\n\t\"homeVodId\": \"/@href\",\r\n\t\"homeVodIdR\": \"/show/(\\\\w+).html\",\r\n\t\"homeVodImg\": \"/img/@src\",\r\n\t\"homeVodMark\": \"/button/text()\",\r\n\t\"cateUrl\": \"http://www.9rmb.com/type/{cateId}/{catePg}.html\",\r\n\t\"cateVodNode\": \"//div[@class='movie-item']/a\",\r\n\t\"cateVodName\": \"/@title\",\r\n\t\"cateVodId\": \"/@href\",\r\n\t\"cateVodIdR\": \"/show/(\\\\w+).html\",\r\n\t\"cateVodImg\": \"/img/@src\",\r\n\t\"cateVodMark\": \"/button/text()\",\r\n\t\"dtUrl\": \"http://www.9rmb.com/show/{vid}.html\",\r\n\t\"dtNode\": \"//div[@class='container-fluid']\",\r\n\t\"dtName\": \"//div[@class='col-md-9']//div[@class='col-md-4']//img/@alt\",\r\n\t\"dtNameR\": \"\",\r\n\t\"dtImg\": \"//div[@class='col-md-9']//div[@class='col-md-4']//img/@src\",\r\n\t\"dtImgR\": \"\",\r\n\t\"dtCate\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '类型')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtCateR\": \"\",\r\n\t\"dtYear\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '日期')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtYearR\": \"\",\r\n\t\"dtArea\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '国家')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtAreaR\": \"\",\r\n\t\"dtMark\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '状态')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtMarkR\": \"\",\r\n\t\"dtActor\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '主演')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtActorR\": \"\",\r\n\t\"dtDirector\": \"//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '导演')]/parent::*/following-sibling::*/text()\",\r\n\t\"dtDirectorR\": \"\",\r\n\t\"dtDesc\": \"//p[@class='summary']/text()\",\r\n\t\"dtDescR\": \"\",\r\n\t\"dtFromNode\": \"//div[contains(@class,'resource-list')]/div[@class='panel-heading']/strong\",\r\n\t\"dtFromName\": \"/text()\",\r\n\t\"dtFromNameR\": \"\\\\S+\\\\.(\\\\S+) \\\\(\",\r\n\t\"dtUrlNode\": \"//div[contains(@class,'resource-list')]/ul[@class='dslist-group']\",\r\n\t\"dtUrlSubNode\": \"/li/a\",\r\n\t\"dtUrlId\": \"@href\",\r\n\t\"dtUrlIdR\": \"/play/(\\\\S+).html\",\r\n\t\"dtUrlName\": \"/text()\",\r\n\t\"dtUrlNameR\": \"\",\r\n\t\"playUrl\": \"http://www.9rmb.com/play/{playUrl}.html\",\r\n\t\"playUa\": \"\",\r\n\t\"searchUrl\": \"http://www.9rmb.com/search?wd={wd}\",\r\n\t\"scVodNode\": \"//div[@class='movie-item']/a\",\r\n\t\"scVodName\": \"/@title\",\r\n\t\"scVodId\": \"/@href\",\r\n\t\"scVodIdR\": \"/show/(\\\\w+).html\",\r\n\t\"scVodImg\": \"/img/@src\",\r\n\t\"scVodMark\": \"/button/text()\"\r\n}"
},
{
    "key": "csp_xpath_jpys",
    "name": "极品影视(XPath)",
    "type": 3,
    "api": "csp_XPath",
    "searchable": 1,
    "quickSearch": 1,
    "filterable": 1,
    "ext": "{\r\n  \"ua\": \"\",\r\n  \"homeUrl\": \"https://www.jpysvip.net\",\r\n  \"cateNode\": \"//ul[contains(@class,'myui-header__menu')]/li[@class='dropdown-hover']//ul/li/a[contains(@href, 'vodtype') and not(contains(@href, '26'))]\",\r\n  \"cateName\": \"/text()\",\r\n  \"cateId\": \"/@href\",\r\n  \"cateIdR\": \"/vodtype/(\\\\d+).html\",\r\n  \"cateManual\": {},\r\n  \"homeVodNode\": \"//div[contains(@class, 'col-lg-wide-75')]//ul[contains(@class,'myui-vodlist')]/li//a[contains(@class,'myui-vodlist__thumb')]\",\r\n  \"homeVodName\": \"/@title\",\r\n  \"homeVodId\": \"/@href\",\r\n  \"homeVodIdR\": \"/voddetail/(\\\\w+).html\",\r\n  \"homeVodImg\": \"@data-original\",\r\n  \"homeVodImgR\": \"\\\\S+(http\\\\S+)\",\r\n  \"homeVodMark\": \"/span[contains(@class,'pic-text')]/text()\",\r\n  \"cateUrl\": \"https://www.jpysvip.net/vodtype/{cateId}-{catePg}.html\",\r\n  \"cateVodNode\": \"//ul[contains(@class,'myui-vodlist')]//li//a[contains(@class,'myui-vodlist__thumb')]\",\r\n  \"cateVodName\": \"/@title\",\r\n  \"cateVodId\": \"/@href\",\r\n  \"cateVodIdR\": \"/voddetail/(\\\\w+).html\",\r\n  \"cateVodImg\": \"@data-original\",\r\n  \"cateVodImgR\": \"\\\\S+(http\\\\S+)\",\r\n  \"cateVodMark\": \"/span[contains(@class,'pic-text')]/text()\",\r\n  \"dtUrl\": \"https://www.jpysvip.net/voddetail/{vid}.html\",\r\n  \"dtNode\": \"//div[contains(@class,'col-lg-wide-75')]\",\r\n  \"dtName\": \"//div[@class='myui-content__thumb']/a[contains(@class,'myui-vodlist__thumb')]/@title\",\r\n  \"dtNameR\": \"\",\r\n  \"dtImg\": \"//div[@class='myui-content__thumb']/a[contains(@class,'myui-vodlist__thumb')]/img/@data-original\",\r\n  \"dtImgR\": \"\\\\S+(http\\\\S+)\",\r\n  \"dtCate\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '分类')]/following-sibling::*/text()\",\r\n  \"dtCateR\": \"\",\r\n  \"dtYear\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '年份')]/following-sibling::*/text()\",\r\n  \"dtYearR\": \"\",\r\n  \"dtArea\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '地区')]/following-sibling::*/text()\",\r\n  \"dtAreaR\": \"\",\r\n  \"dtMark\": \"\",\r\n  \"dtMarkR\": \"\",\r\n  \"dtActor\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '主演')]/following-sibling::*/text()\",\r\n  \"dtActorR\": \"\",\r\n  \"dtDirector\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '导演')]/following-sibling::*/text()\",\r\n  \"dtDirectorR\": \"\",\r\n  \"dtDesc\": \"//div[@class='myui-content__detail']//span[@class='text-muted'  and contains(text(), '简介')]/parent::text()\",\r\n  \"dtDescR\": \"\",\r\n  \"dtFromNode\": \"//a[@data-toggle='tab' and contains(@href, 'playlist')]\",\r\n  \"dtFromName\": \"/text()\",\r\n  \"dtFromNameR\": \"\",\r\n  \"dtUrlNode\": \"//div[contains(@class,'tab-content')]/div[contains(@id, 'playlist')]\",\r\n  \"dtUrlSubNode\": \"//li/a\",\r\n  \"dtUrlId\": \"@href\",\r\n  \"dtUrlIdR\": \"/vodplay/(\\\\S+).html\",\r\n  \"dtUrlName\": \"/text()\",\r\n  \"dtUrlNameR\": \"\",\r\n  \"playUrl\": \"https://www.jpysvip.net/vodplay/{playUrl}.html\",\r\n  \"playUa\": \"\",\r\n  \"searchUrl\": \"https://www.jpysvip.net/index.php/ajax/suggest?mid=1&wd={wd}&limit=10\",\r\n  \"scVodNode\": \"json:list\",\r\n  \"scVodName\": \"name\",\r\n  \"scVodId\": \"id\",\r\n  \"scVodIdR\": \"\",\r\n  \"scVodImg\": \"pic\",\r\n  \"scVodMark\": \"\"\r\n}\r\n"
}
```

### 套娃规则

demo配置写的比较细，不一定所有字段都要有，具体还是自己多试一试

```json
{
	"ua": "",
    // 首页地址 用于获取 分类和首页推荐
	"homeUrl": "http://www.9rmb.com",
    // 分类节点
	"cateNode": "//ul[contains(@class,'navbar-nav')]/li/a[contains(@href, '.html') and not(contains(@href, '6'))]",
    // 分类名
	"cateName": "/text()",
    // 分类id
	"cateId": "/@href",
    // 分类id二次处理正则
	"cateIdR": "/type/(\\d+).html",
    // 手动设置分类，如果手动设置了分类则不使用上面的分类xpath获取分类  例如 "cateManual": {"电影": "1", "电视剧": "2"},
	"cateManual": {},
    // 首页推荐视频的节点
	"homeVodNode": "//div[@class='col-md-12 movie-item-out']//a[not(contains(@href, '6'))]/parent::*/parent::*/parent::*/div[contains(@class, 'movie-item-out') and position()<10]/div[@class='movie-item']/a",
    // 首页推荐视频的名称
	"homeVodName": "/@title",
    // 二次处理正则
    "homeVodNameR": "",
    // 首页推荐视频的id
	"homeVodId": "/@href",
    // 二次处理正则
	"homeVodIdR": "/show/(\\w+).html",
    // 首页推荐视频的图片
	"homeVodImg": "/img/@src",
    // 二次处理正则
    "homeVodImgR": "",
    // 首页推荐视频的简介
	"homeVodMark": "/button/text()",
    // 二次处理正则
    "homeVodMarkR": "",
    // 分类页地址 {cateId} 分类id {catePg} 当前页
	"cateUrl": "http://www.9rmb.com/type/{cateId}/{catePg}.html",
    // 同上面的homeVod字段 分类列表中的视频信息
	"cateVodNode": "//div[@class='movie-item']/a",
	"cateVodName": "/@title",
	"cateVodId": "/@href",
	"cateVodIdR": "/show/(\\w+).html",
	"cateVodImg": "/img/@src",
	"cateVodMark": "/button/text()",
    // 详情页地址 用于获取详情页信息 及 播放列表和地址
	"dtUrl": "http://www.9rmb.com/show/{vid}.html",
    // 详情节点
	"dtNode": "//div[@class='container-fluid']",
    // 视频名
	"dtName": "//div[@class='col-md-9']//div[@class='col-md-4']//img/@alt",
	"dtNameR": "",
    // 视频图片
	"dtImg": "//div[@class='col-md-9']//div[@class='col-md-4']//img/@src",
	"dtImgR": "",
    // 视频分类
	"dtCate": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '类型')]/parent::*/following-sibling::*/text()",
	"dtCateR": "",
    // 视频年份
	"dtYear": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '日期')]/parent::*/following-sibling::*/text()",
	"dtYearR": "",
    // 视频地区
	"dtArea": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '国家')]/parent::*/following-sibling::*/text()",
	"dtAreaR": "",
    // 视频状态
	"dtMark": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '状态')]/parent::*/following-sibling::*/text()",
	"dtMarkR": "",
    // 主演
	"dtActor": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '主演')]/parent::*/following-sibling::*/text()",
	"dtActorR": "",
    // 导演
	"dtDirector": "//div[@class='col-md-8']//span[@class='info-label' and contains(text(), '导演')]/parent::*/following-sibling::*/text()",
	"dtDirectorR": "",
    // 视频简介
	"dtDesc": "//p[@class='summary']/text()",
	"dtDescR": "",
    // 播放源节点
	"dtFromNode": "//div[contains(@class,'resource-list')]/div[@class='panel-heading']/strong",
    // 播放源名称
	"dtFromName": "/text()",
    // 二次处理正则
	"dtFromNameR": "\\S+\\.(\\S+) \\(",
    // 播放列表节点
	"dtUrlNode": "//div[contains(@class,'resource-list')]/ul[@class='dslist-group']",
    // 播放地址节点
	"dtUrlSubNode": "/li/a",
    // 播放地址
	"dtUrlId": "@href",
    // 二次处理正则
	"dtUrlIdR": "/play/(\\S+).html",
    // 剧集名称
	"dtUrlName": "/text()",
    // 二次处理正则
	"dtUrlNameR": "",
    // 播放页面的地址 {playUrl} 对应上面 dtUrlId 获取到的地址
	"playUrl": "http://www.9rmb.com/play/{playUrl}.html",
    // 解析webview的user-agent
	"playUa": "",
    // 搜索地址
	"searchUrl": "http://www.9rmb.com/search?wd={wd}",
    // 同上面的homeVod字段 搜索结果中的视频信息
	"scVodNode": "//div[@class='movie-item']/a",
	"scVodName": "/@title",
	"scVodId": "/@href",
	"scVodIdR": "/show/(\\w+).html",
	"scVodImg": "/img/@src",
	"scVodMark": "/button/text()"
}
```