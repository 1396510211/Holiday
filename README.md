
![logo](https://github.com/1396510211/Holiday/blob/master/logo.png)

# 假期查询接口文档
## 简介 

该接口是一个**免费**的假期查询接口，可以查询指定日期是否为法定节假日或者调休日。
对单个ip限流10000/次每天，程序后台自动抓取国务院数据，会在每年11月更新下一年的数据。

## 接口地址
```
http://116.205.225.100:8888/holiday
```
## 请求方式
```
GET
```
## 请求参数

| 参数名 |  类型  | 是否必填 |      描述      |
| :----: | :----: | :------: | :------------: |
|  year  | int32 |    是    | 目标查询的年份 |
| month  | int32 |    否    | 目标查询的月份 |
|  day   | int32 |    否    |  目标查询的天  |

## 响应参数

|   参数名   |  类型  |             描述             |
| :--------: | :----: | :--------------------------: |
|    year    | int32 |          年（阳历）          |
|   month    | int32 |          月（阳历）          |
|    day     | int32 |          日（阳历）          |
| lunarYear  | int32 |          年（农历）          |
| lunarMonth | int32 |          月（农历）          |
| lunarDate  | int32 |          日（农历）          |
|   status   | int32 | 节假日状态（1-休假，2-补班） |
|   weekDay    | int32 |  星期描述（0-6 0表示周日）  |
|   lDate    | string |        日（农历描述）        |
|   lMonth   | string |        月（农历描述）        |
|    term    | string |     节假日描述     |
|   solarTerm   | string | 节气 |

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

### 示例3
```
http://116.205.225.100:8888/holiday?year=2023 // 查询某一年的信息
```

### 错误码



