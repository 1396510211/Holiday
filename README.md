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

|参数名|类型|是否必填｜描述
｜---｜---｜---｜---|
｜example｜example|example|example|

## 响应参数

|参数名|类型|描述｜
｜---｜---｜---｜
｜example｜example|example|

### data参数说明

## 响应示例
### 成功响应

```json
{
    "dates":{ 
        "2023-9-29":  {
        "weekday":5,   
        "weekday_str_cn":"星期五",
        "weekday_str":"Friday",
        "isLeapYear":false,
        "holiday":{
            "name":"中秋节",
            "work":false
            },
        "lunar":{
            "year":2023,
            "month":8,
            "day":15,
            "solar":""
            }
        }
    }
}
```
### 失败响应

```json

```
### 错误码



