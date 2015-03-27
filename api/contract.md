# 合约信息查询

> - 根据号码查询合约计划信息



## API说明

### API名称

cu.ecs.user-profile.contract-profile

## API类型

用户信息服务

### 请求方式

WebService HTTP-GET

## 数据格式

SOAP XML

## API 授权类型

需要授权

## 版本

1.0.0

### API URL

`http://DATA-API.SERV/user_profile`

### API方法

```
public  get_contract_profile(string user_number) : object(Contract_Profile_Response) {}
```

## 参数说明



### 请求参数

> -1. `string(11+)` user_number

> 用户号码



### 应答对象

> - object(Contract_Profile_Response)         `合约信息应答对象`

### 应答示例

```
object(Response) {
    "data" : object(Contract_Profile) {
        "1" : object(MyContract_Profile) {
            "product" : object(Mycontract_Product) {
                "name" : string("iPhone 96元合约套餐"),
            },
            "statime": Datetime(xxxx-xx-xx),
            "endtime": Datetime(xxxx-xx-xx),
        }
    }

    "status" : object(Status) {
        code : enum(0),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}
```
---


