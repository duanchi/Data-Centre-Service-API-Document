# 3.1.4. 合约信息查询服务

> - 根据号码查询合约计划信息



## 3.1.4.1. API说明

#### API名称

> cu.ecs.user-service.contract

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


## 3.1.4.2. API URL

> [http://DATA-API.SERV/user_service](http://DATA-API.SERV/user_service)




## 3.1.4.3. API方法

```
public function get_contract(string user, user_type = USER_NUMBER) : object(Contract_Response) {}
```



## 3.1.4.4. 请求参数


* #### user

> type :　`string`

> length : 11 or 18

> desc : 当前查询用户的用户号码或身份证号码

> value : 用户号码或身份证号码


* #### user_type

> type :　`enum`

> desc : 当前沃家庭成员号码信息集合

> value :

> - `USER_NUMBER` 用户号码

> - `ID_CARD` 身份证号码





## 3.1.4.5. 应答对象

> object(Contract_Response)

>  合约信息应答对象，see [4.1.2.4. Contract_Response Object](/definition/contract_response_object.html#4124-contract_response-object)




## 3.1.4.6. 应答示例

```
object(Contract_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [object(Contract_Data) {
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


