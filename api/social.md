# 3.3.1. 社交帐号信息查询服务[^1]

> - 根据号码查询对应的微博、微信、QQ等账号



## 3.3.1.1. API说明

#### API名称

> cu.ecs.extend-service.social

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
public function get_social(string user) : object(Social_Response) {}
```



## 3.3.1.4. 请求参数


* #### user

> type :　`string`

> length : 11

> desc : 当前查询用户的用户号码

> value : 用户号码



## 3.3.1.5. 应答对象

> object(Social_Response)

>  社交帐号信息查询服务应答对象，see [4.1.2.7. Social_Response Object](/definition/social_response_object.html#4127-social_response-object)




## 3.3.1.6. 应答示例

```
object(Social_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [
        object(Social_Response) {
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
