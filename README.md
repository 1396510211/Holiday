```
截屏2023-10-08 21.30.18.png
```
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



