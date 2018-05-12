# coordinates-transform

Tools for coordinates transformation between BD09, GCJ02 and WGS84。

（For coordinates in China Mainland only)

BD09: Baidu Map

GCJ02: Google Map / AutoNavi Map / Tencent Map

WGS84: World Geodetic System

## Install

```
npm install coord-transform
```

## Usage

```js
const {bd09togcj02, gcj02tobd09, wgs84togcj02, gcj02towgs84} = require('coordinates-transform');

// 百度转谷歌、高德、腾讯
// Baidu Map to Google Map / AutoNavi Map / Tencent Map
console.log(bd09togcj02(121.442869, 31.032034));
// [ 121.4364664212716, 31.025677793196795 ]

// 谷歌、高德、腾讯转百度
// Google Map / AutoNavi Map / Tencent Map to Baidu Map
console.log(gcj02tobd09(121.436466, 31.025677));
// [ 121.44286883589297, 31.03203364007244 ]

// 谷歌、高德转WGS通用
// Google Map or AutoNavi Map to World Geodetic System
console.log(gcj02towgs84(121.436466, 31.025677));
// [ 121.43186360201696, 31.0276475152394 ]

// WGS通用转谷歌、高德
// World Geodetic System to Google Map or AutoNavi Map
console.log(wgs84togcj02(121.431863, 31.027647));
// [ 121.43647333299322, 31.025684130869397 ]
```

## License

MIT © [Wang Sijie](http://sijie.wang)