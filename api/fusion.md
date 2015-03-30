# 3.1.2. 融合信息服务[^1]

> - 根据号码或身份证号查询所属的融合信息
> - 根据号码或身份证号查询相关号码信息




## 3.1.2.1. API说明

#### API名称

> cu.ecs.user-service.fusion

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




## 3.1.2.2. API URL

> [http://DATA-API.SERV/user_service](http://DATA-API.SERV/user_service)




## 3.1.2.3. API方法

```
public function get_fusion(
    string user,
    enum user_type = USER_NUMBER,
    enum[] scope = []
) : object(Fusion_Response) {}
```



## 3.1.2.4. 请求参数


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


* #### scope

> type :　`enum[]`

> desc : 融合类型范围定义，以数字下标数组填充查询范围，或填充空数组返回全部融合类型的查询结果

> value :

> - `wo_family` 沃家庭

> - `2` 沃享套餐

> - `4` 其他融合套餐

> - `[]` 返回用户全部已知融合类型查询结果




## 3.1.2.5. 应答对象

> object(Fusion_Response)

>  融合信息服务应答对象，see [4.1.2.1. Fusion_Response Object](/definition/fusion_response_object.html#4121-fusion_response-object)




## 3.1.2.5. 应答示例

```
object(Fusion_Response) {

    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    object(Fusion_Data) {
        "wo_family" : object(WoFamily_Data) {
            ...
        }
    }
    "status" : object(Status) {
        code : enum(0000),
        message : string("success!"),
        timestamp : timestamp(1427259974.2252)
    }
}
```
----
[^1]: 目前只支持沃家庭融合信息查询
