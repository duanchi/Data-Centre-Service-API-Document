# 3.1.3. 集团客户信息服务

> - 根据号码查询归属的集团客户、付费方式等



## 3.1.3.1. API说明

#### API名称

> cu.ecs.user-service.group

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


## 3.1.3.2. API URL

> [http://DATA-API.SERV/user_service](http://DATA-API.SERV/user_service)




## 3.1.3.3. API方法

```
public function get_group(string user) : object(Group_Response) {}
```



## 3.1.3.4. 请求参数


* #### user

> type :　`string`

> length : 11

> desc : 当前查询用户的用户号码

> value : 用户号码





## 3.1.3.5. 应答对象

> object(Group_Response)

>  集团客户信息应答对象，see [4.1.2.3. Group_Response Object](/definition/group_response_object.html#4123-group_response-object)




## 3.1.4.6. 应答示例

```
object(Group_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [
        object(Group_Data) {
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


