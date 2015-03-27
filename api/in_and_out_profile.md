# 入网离网信息查询

> - 根据身份证号查询入网、离网信息




## API说明

### API名称

cu.ecs.user-profile.InAndOut-profile

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
public  get_InAndOut_profile(string user_idnumber) : object(InAndOut_Profile_Response) {}
```

## 参数说明



### 请求参数

> -1. `string(18+)` user_idnumber

> 用户身份证号码



### 应答对象

> - object(InAndOut_Profile_Response)         `合约信息应答对象`

### 应答示例

```
object(Response) {
    "data" : object(InAndOut_Profile) {
        "1" : object(MyInAndOut_Profile) {
            "product" : object(MyInAndOut_Product) {
                "Entry" : object(User_Profile) {
                "number" : string("010xxxxxxxx")
                 },
                "statime": Datetime(xxxx-xx-xx),
                 InAndOut_type : enum(1),
                "endtime": Datetime(xxxx-xx-xx),
            },

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


