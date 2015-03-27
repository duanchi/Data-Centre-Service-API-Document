# 融合信息查询[^1]

> - 根据号码查询所属的沃家庭信息
> - 根据号码或身份证号查询相关号码信息


## API说明

### API名称

cu.ecs.user-service.fusion

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

`http://DATA-API.SERV/user_service`

### API方法

```
public function get_fusion(string user_number, enum[] scope = []) : object(Fusion_Response) {}
```

## 参数说明

### 请求参数

> -1. `string(11)` user_number

> 用户号码

> -2. `enum[]` scope, (default : `[]`)

> 融合类型范围定义，以数字下标数组填充查询范围，或填充空数组返回全部融合类型的查询结果

> - `wo_family` 沃家庭
> - `2` 沃享套餐
> - `4` 其他融合套餐
> - `[]` 返回用户全部已知融合类型查询结果

### 应答对象

> - object(Fusion_Response)         `融合信息应答对象`

### 应答示例

```
object(Fusion_Response) {
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
                }
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
---
[^1]: 目前只支持沃家庭融合信息查询
