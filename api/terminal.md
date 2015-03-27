# 终端信息查询[^1]

> - 根据号码查询终端情况



## API说明

### API名称

cu.ecs.user-service.terminal

### API类型

扩展信息服务

### 请求方式

WebService HTTP-GET

### 数据格式

SOAP XML

### API 授权类型

需要授权

### 版本

1.0.0

## API URL

`http://DATA-API.SERV/extend_service`

## API方法

```
public function get_terminal(string user_number, enum scope = 0, date start = NULL, date end = NULL) : object(Terminal_Response) {}
```

### 参数说明

### 请求参数

> -1. `string(11)` user_number

> 用户号码

> -2. `enum` scope, (default : `0`)

> 范围定义

> - `0` 只返回当前或最后一次使用的终端
> - `1` 返回用户所有使用过的终端
> - `2` 按照时间区间返回使用过的终端列表

> -3. `date` start, (default : `NULL`)

> 开始日期

> -4. `date` end, (default : `NULL`)

> 结束日期


### 应答对象

> - object(Terminal_Response)         `终端信息应答对象`

### 应答示例

```
object(Terminal_Response) {
    "data" : [
        object(Terminal_Profile) {
            "imei" : string("xxxxxxxxxxxxx"),
            "phone" : object(Phone_Profile) {
                "manufacturer" : string("Apple."),
                "model" : string("6,A1597")
            },
            "start_time" : date("2015-01-12")
        }
    ],

    "status" : object(Status) {
        code : enum(0),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}
```
---
[^1]: 只支持3年内用户终端信息查询
