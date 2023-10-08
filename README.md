
![logo](https://github.com/1396510211/Holiday/blob/master/logo.png)

# 假期查询接口文档
## 简介
该接口是一个假期查询接口，可以查询指定日期是否为法定节假日或者调休日。

## 接口地址
```
http://www.landsea.top/holiday
```
## 请求方式
```
GET
```
## 请求参数

| 参数名 |  类型  | 是否必填 |      描述      |
| :----: | :----: | :------: | :------------: |
|  year  | string |    是    | 目标查询的年份 |
| month  | string |    否    | 目标查询的月份 |
|  day   | string |    否    |  目标查询的天  |

## 响应参数

|   参数名   |  类型  |             描述             |
| :--------: | :----: | :--------------------------: |
|    Year    | string |          年（阳历）          |
|   Month    | string |          月（阳历）          |
|    Day     | string |          日（阳历）          |
| LunarYear  | string |          年（农历）          |
| LunarMonth | string |          月（农历）          |
| LunarDate  | string |          日（农历）          |
|   LDate    | string |        日（农历描述）        |
|   LMonth   | string |        月（农历描述）        |
|   CnDay    | string |  星期描述（一二三四五六日）  |
|    Term    | string |     节假日描述（含节气）     |
|   Status   | string | 节假日状态（1-休假，2-补班） |

### data参数说明

## 请求响应示例
### 示例1:
```
http://116.205.225.100:8888/holiday?year=2023&month=10&day=1  // 查询某一天的信息
```

```json
{
	"code": 0,
	"message": "OK",
	"data": {
		"dates": [{
			"weekday": 6,
			"weekday_str_cn": "星期六",
			"weekday_str": "Saturday",
			"holiday": {
				"name": "国庆节",
				"work": false
			},
			"lunar": {
				"year": 2023,
				"month": 8,
				"day": 16,
				"solar": ""
			}
		}, {
			"weekday": 6,
			"weekday_str_cn": "星期六",
			"weekday_str": "Saturday",
			"holiday": {
				"name": "国庆节",
				"work": false
			},
			"lunar": {
				"year": 2023,
				"month": 8,
				"day": 16,
				"solar": ""
			}
		}]
	}
}
```

### 示例2
```
http://116.205.225.100:8888/holiday?year=2023&month=10 // 查询某一月的信息
```

```json
{
	"code": 0,
	"message": "OK",
	"data": {
		"dates": [{
			"year": 2020,
			"month": 10,
			"day": 1,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 15,
			"lDate": "十五",
			"lMonth": "八",
			"weekday": 4,
			"term": "国庆中秋",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 2,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 16,
			"lDate": "十六",
			"lMonth": "八",
			"weekday": 5,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 3,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 17,
			"lDate": "十七",
			"lMonth": "八",
			"weekday": 6,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 4,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 18,
			"lDate": "十八",
			"lMonth": "八",
			"weekday": 0,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 5,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 19,
			"lDate": "十九",
			"lMonth": "八",
			"weekday": 1,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 6,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 20,
			"lDate": "二十",
			"lMonth": "八",
			"weekday": 2,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 7,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 21,
			"lDate": "廿一",
			"lMonth": "八",
			"weekday": 3,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 8,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 22,
			"lDate": "廿二",
			"lMonth": "八",
			"weekday": 4,
			"term": "",
			"status": 1
		}, {
			"year": 2020,
			"month": 10,
			"day": 9,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 23,
			"lDate": "廿三",
			"lMonth": "八",
			"weekday": 5,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 10,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 24,
			"lDate": "廿四",
			"lMonth": "八",
			"weekday": 6,
			"term": "",
			"status": 2
		}, {
			"year": 2020,
			"month": 10,
			"day": 11,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 25,
			"lDate": "廿五",
			"lMonth": "八",
			"weekday": 0,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 12,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 26,
			"lDate": "廿六",
			"lMonth": "八",
			"weekday": 1,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 13,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 27,
			"lDate": "廿七",
			"lMonth": "八",
			"weekday": 2,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 14,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 28,
			"lDate": "廿八",
			"lMonth": "八",
			"weekday": 3,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 15,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 29,
			"lDate": "廿九",
			"lMonth": "八",
			"weekday": 4,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 16,
			"lunarYear": 2020,
			"lunarMonth": 8,
			"lunarDate": 30,
			"lDate": "三十",
			"lMonth": "八",
			"weekday": 5,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 17,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 1,
			"lDate": "初一",
			"lMonth": "九",
			"weekday": 6,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 18,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 2,
			"lDate": "初二",
			"lMonth": "九",
			"weekday": 0,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 19,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 3,
			"lDate": "初三",
			"lMonth": "九",
			"weekday": 1,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 20,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 4,
			"lDate": "初四",
			"lMonth": "九",
			"weekday": 2,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 21,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 5,
			"lDate": "初五",
			"lMonth": "九",
			"weekday": 3,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 22,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 6,
			"lDate": "初六",
			"lMonth": "九",
			"weekday": 4,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 23,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 7,
			"lDate": "初七",
			"lMonth": "九",
			"weekday": 5,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 24,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 8,
			"lDate": "初八",
			"lMonth": "九",
			"weekday": 6,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 25,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 9,
			"lDate": "初九",
			"lMonth": "九",
			"weekday": 0,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 26,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 10,
			"lDate": "初十",
			"lMonth": "九",
			"weekday": 1,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 27,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 11,
			"lDate": "十一",
			"lMonth": "九",
			"weekday": 2,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 28,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 12,
			"lDate": "十二",
			"lMonth": "九",
			"weekday": 3,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 29,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 13,
			"lDate": "十三",
			"lMonth": "九",
			"weekday": 4,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 30,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 14,
			"lDate": "十四",
			"lMonth": "九",
			"weekday": 5,
			"term": "",
			"status": 0
		}, {
			"year": 2020,
			"month": 10,
			"day": 31,
			"lunarYear": 2020,
			"lunarMonth": 9,
			"lunarDate": 15,
			"lDate": "十五",
			"lMonth": "九",
			"weekday": 6,
			"term": "",
			"status": 0
		}]
	}
}
```
### 示例3
```
http://116.205.225.100:8888/holiday?year=2023 // 查询某一年的信息
```

### 错误码



