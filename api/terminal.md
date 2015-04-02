# 3.3.1. 用户终端使用信息查询服务[^1]

> - 根据号码查询终端情况



## 3.3.1.1. API说明

#### API名称

> cu.ecs.extend-service.terminal

#### API类型

> 用户信息服务

#### 请求方式

> WebService HTTP-GET

#### 数据格式

> SOAP XML

#### API 授权类型

> 需要授权

#### 版本

> 1.0.0


## 3.3.1.2. API URL

> [http://DATA-API.SERV/extend_service](http://DATA-API.SERV/extend_service)




## 3.3.1.3. API方法

```
public function get_terminal(string user, enum scope = CURRENT, date start = NULL, date end = NULL) : object(Terminal_Response) {}
```



## 3.3.1.4. 请求参数


* #### user

> type :　`string`

> length : 11

> desc : 当前查询用户的用户号码

> value : 用户号码


* #### scope

> type :　`enum`

> desc : 范围定义

> value :

> - `CURRENT` 只返回当前或最后一次使用的终端

> - `ALL` 返回用户所有使用过的终端

> - `INTERVAL` 按照时间区间返回使用过的终端列表

> 范围定义


* #### start

> type :　`datetime`

> desc : 开始日期

> value : 开始日期


* #### end

> type :　`datetime`

> desc : 结束日期

> value : 结束日期



## 3.3.1.5. 应答对象

> object(Terminal_Response)

>  用户使用终端信息应答对象，see [4.1.2.6. Terminal_Response Object](/definition/terminal_response_object.html#4126-terminal_response-object)




## 3.3.1.6. 应答示例

```
object(Terminal_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [
        object(Terminal_Data) {
            ...
        }
    ],
    "status" : object(Status) {
        code : enum(0000),
        message : string("success!"),
        timestamp : timestamp(1427259974.2252)
    }
}
```


---
[^1]: 只支持3年内用户终端信息查询
