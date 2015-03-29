# 4.1.1. Request Object

> 服务请求对象



### 定义

---
```
Class Request extend StdClass {
    public uuid request_id;
    public enum service;
};
```
---


### 属性


* #### request_id

> type :　`uuid`

> desc : 当前应答的请求唯一ID

> value : 请求ID，使用UUID


* #### service

> type :　`enum`

> desc : 当前应答的请求服务的名称

> value : 服务名称，see [4.2.1. Status Code Enum](/definition/service_enum.html#421-service-enum)



### DUMP

```
object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    }
```
