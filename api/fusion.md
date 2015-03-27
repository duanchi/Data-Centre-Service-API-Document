# 3.1.1. 融合信息服务[^1]

> - 根据号码或身份证号查询所属的融合信息
> - 根据号码或身份证号查询相关号码信息




## 3.1.1.1. API说明

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




## 3.1.1.2. API URL

> [http://DATA-API.SERV/user_service](http://DATA-API.SERV/user_service)




## 3.1.1.3. API方法

```
public function get_fusion(string user, enum user_type, enum[] scope = []) : object(Fusion_Response) {}
```



## 3.1.1.4. 请求参数

* ### user

> type :　`string(11 or 18)`

> 用户号码或身份证号码

> 用户号码可能为11位手机号码或11位区号+固定电话号码

* ### scope

> type : `enum[]`

> default : `[]`

> - `wo_family` 沃家庭
> - `2` 沃享套餐
> - `4` 其他融合套餐
> - `[]` 返回用户全部已知融合类型查询结果

> 融合类型范围定义，以数字下标数组填充查询范围，或填充空数组返回全部融合类型的查询结果




## 3.1.1.5. 应答对象

> object(Fusion_Response)       `融合信息应答对象`

>  对象内容参考 `4.1.1.5.`




## 3.1.1.5. 应答示例

```
object(Fusion_Response) {

    "service" : enum("cu.ecs.user-service.fusion"),
    "data" : object(Fusion_Profile) {
        "wo_family" : object(WOFamily_Profile) {
            "product" : object(WOFamily_Product) {
                "name" : string("沃家庭91套餐"),
            },
            "master": object(User_Profile) {
                "number" : string("010xxxxxxxx")
            },
            "slave" : [
                object(User_Profile) {
                    "number" : string("186xxxxxxxx")
                },
                ...
            ]
        }
    }
    "status" : object(Status) {
        code : enum(0),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}
```
----
[^1]: 目前只支持沃家庭融合信息查询
