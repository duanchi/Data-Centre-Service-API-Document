# 3.1.5. 用户在网状态信息查询服务

> - 根据身份证号查询网络状态信息



## 3.1.5.1. API说明

#### API名称

> cu.ecs.user-service.status

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


## 3.1.5.2. API URL

> [http://DATA-API.SERV/user_service](http://DATA-API.SERV/user_service)




## 3.1.5.3. API方法

```
public function get_status(string user, enum scope = CURRENT, date start = NULL, date end = NULL) : object(Status_Response) {}
```



## 3.1.5.4. 请求参数


* #### user

> type :　`string`

> length : 18

> desc : 当前查询用户的身份证号码

> value : 身份证号码


* #### scope

> type :　`enum`

> desc : 范围定义

> value :

> - `CURRENT` 只返回当前或最后一次在网情况

> - `ALL` 返回用户所有在网、离网情况

> - `INTERVAL` 按照时间区间返回用户在网、离网情况

> 范围定义


* #### start

> type :　`datetime`

> desc : 开始日期

> value : 开始日期


* #### end

> type :　`datetime`

> desc : 结束日期

> value : 结束日期



## 3.1.5.5. 应答对象

> object(Status_Response)

>  合约信息应答对象，see [4.1.2.5. Status_Response Object](/definition/Status_response_object.html#4125-status_response-object)




## 3.1.5.6. 应答示例

```
object(Status_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [
        object(Status_Data) {
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

