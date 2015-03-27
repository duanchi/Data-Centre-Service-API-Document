# 集客信息查询

> - 根据号码查询归属的集团客户、付费方式等



## API说明

### API名称

cu.ecs.user-profile.group-profile

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
public  get_group(string user_number) : object(Group_Response) {}
```

## 参数说明



### 请求参数

> -1. `string(11)` user_number

> 用户号码



### 应答对象

> - object(Group_Response)         `集团信息应答对象`

### 应答示例

```
object(Response) {
    "data" : object(Group_Profile) {
        "1" : object(MyGroup_Profile) {
            "product" : object(Mygroup_Product) {
                "name" : string("中国联通集团"),
            },
            "master": object(User_Profile) {
                "number" : string("010xxxxxxxx")
            },
            "pay_type" :enum(1)
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


