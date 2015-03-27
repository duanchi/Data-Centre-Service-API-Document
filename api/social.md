# 社交帐号信息查询

> - 根据号码查询对应的微博、微信、QQ等账号



## API说明

### API名称

cu.ecs.user-service.social

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
public function get_social(string user_number, enum[] scope = []) : object(Social_Response) {}
```

### 参数说明

### 请求参数

> -1. `string(11)` user_number

> 用户号码

> -2. `enum[]` scope, (default : `[]`)

> 范围定义，以数字下标数组填充查询范围，或填充空数组返回全部查询范围

> - `weibo` 返回用户微博帐号信息
> - `wechat` 返回用户微信帐号信息
> - `qq` 返回用户QQ帐号信息
> - `[]` 返回用户全部已知社交帐号


### 应答对象

> - object(Social_Response)             `社交帐号信息应答对象`

### 应答示例

```
object(Social_Response) {
    "data" : object(Social_Profile) {
        "weibo" : object(Weibo_Profile) {
            "scope" : enum("weibo"),
            "user" : string("07.duanchi@gmail.com"),
            "homepage" : string("weibo.com/shijingye"),
        },
        "wechat" : object(Wechat_Profile) {
            "scope" : enum("wechat"),
            "user" : string("68661364")
        },
        "qq" : object(Qq_Profile) {
            "scope" : enum("qq"),
            "user" : string("68661364")
        }
    },

    "status" : object(Status) {
        code : enum(0),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}
```
---
