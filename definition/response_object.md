# 4.1.2. Response Object

> 服务应答对象



### 定义

---
```
Class Response extend StdClass {
    public Request request;
    public StdObject[] data = [];
    public Status status;
};
```
---


### 属性


* #### request

> type :　`object(Request)`

> desc : 当前服务请求的请求对象

> value : see [4.1.1. Request Object](/definition/request_object.html#411-request-object)



* #### data

> type :　`object(StdClass)[]`

> desc : 数据对象集合，当服务调用异常时，可以为空

> value : 需子类定义



* #### status

> type :　`object(Status)`

> desc : 当前服务请求的服务应答状态

> value : 服务应答状态对象



###DUMP

```
object(Response) {
    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : object(StdClass) {}
    "status" : object(Status) {
        code : enum(0000),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}
```
