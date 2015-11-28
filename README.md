# IntentMapGuide
百度，高德，腾讯第三方Intent调整的技术文档整理

国内地图最大的三家:百度，高德，腾讯(最近地图事业部有点起色),当我们想使用导航功能的时候，如果业务很重那么可以使用上面任何一家的SDK，但是如果就是纯粹的附加功能，那么就可以选择Intent调整的方式，几行代码搞定一个要引入几M大的SDK的功能。

###下面是三家的调起说明

- 百度地图公交、驾车、步行导航

调起Android百度地图，展示指定导航模式下从起点到终点的路线规划。

//移动APP调起Android百度地图方式举例
```
intent = Intent.getIntent("intent://map/direction?origin=latlng:34.264642646862,108.95108518068|
name:我家&destination=大雁塔&mode=driving®ion=西安&src=yourCompanyName|yourAppName#Intent;scheme=bdapp;package=com.baidu.BaiduMap;end"); 
startActivity(intent); 
```

//网页应用调起Android百度地图方式举例
```
<a href="intent://map/direction?origin=latlng:34.264642646862,108.95108518068|name:我家&destinat
ion=大雁塔&mode=driving®ion=西安&src=yourCompanyName|yourAppName">线路规划</a>
```

- 高德地图路线规划

输入起点和终点，搜索公交、驾车或步行的线路。支持版本 V4.2.1 起。
使用示例：
 

```
act=android.intent.action.VIEW
cat=android.intent.category.DEFAULT
dat=androidamap://route?sourceApplication=softname&slat=36.2&slon=116.1&sname=abc&dlat=36.3&dlon=116.2&dname=def&dev=0&m=0&t=1
pkg=com.autonavi.minimap 
```

- 腾讯地图路线规划


```
qqmap://map/routeplan?type=drive&from=天坛南门&fromcoord=39.873145,116.413306&to=国家大剧院&tocoord=39.907380,116.388501
//移动端启动腾讯地图App，并显示从出发点[天坛南门] 到 [目的地坐标(国家大剧院)] 的驾车路线规划
```
