# Android Intent Commands Reference

## Navigation

| App | Intent |
|-----|--------|
| AutoNavi (高德地图) | `am start -a android.intent.action.VIEW -d 'androidamap://route/plan/?sname=我的位置&dname={destination}&t=0'` |
| Baidu Maps (百度地图) | `am start -a android.intent.action.VIEW -d 'baidumap://map/direction?destination={destination}'` |
| Tencent Maps (腾讯地图) | `am start -a android.intent.action.VIEW -d 'qqmap://routeplan?type=drive&to={destination}'` |

## Food Delivery

| App | Intent |
|-----|--------|
| Ele.me (饿了么) | `am start -a android.intent.action.VIEW -d 'eleme://search?keyword={keyword}'` |
| Meituan (美团) | `am start -a android.intent.action.VIEW -d 'meituan://search?keyword={keyword}'` |

## Ride-Hailing

| App | Intent |
|-----|--------|
| DiDi (滴滴) | `am start -a android.intent.action.VIEW -d 'didi://home'` |
| Gaode Taxi (高德打车) | `am start -a android.intent.action.VIEW -d 'androidamap://taxi'` |

## Social Media

| App | Intent |
|-----|--------|
| WeChat (微信) | `am start -n com.tencent.mm/.ui.LauncherUI` |
| Weibo (微博) | `am start -n com.sina.weibo/.MainActivity` |
| Xiaohongshu (小红书) | `am start -n com.xingin.xhs/.index.v2.IndexActivityV2` |

## Payment

| App | Intent |
|-----|--------|
| Alipay (支付宝) | `am start -n com.eg.android.AlipayGphone/.AlipayLogin` |
| WeChat Pay (微信支付) | `am start -n com.tencent.mm/.plugin.wallet.ui.WalletBindUI` |

## AI Apps

| App | Intent |
|-----|--------|
| Doubao (豆包) | `am start -n com.doubao.ai/.MainActivity` |
| Kimi | `am start -n com.kimi.kimi/.MainActivity` |
| Jimeng (即梦) | `am start -n com.jimeng/.MainActivity` |

## System

| Action | Intent |
|--------|--------|
| Settings | `am start -a android.settings.SETTINGS` |
| WiFi settings | `am start -a android.settings.WIFI_SETTINGS` |
| Bluetooth settings | `am start -a android.settings.BLUETOOTH_SETTINGS` |
| Add calendar event | `am start -a android.intent.action.INSERT -t vnd.android.cursor.item/event --es title '{title}'` |
| Set alarm | `am start -a android.intent.action.SET_ALARM --ei hour {h} --ei minutes {m}` |