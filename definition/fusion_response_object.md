# 4.1.2.1. Fusion_Response Object

> 融合信息服务应答对象



### 定义

---
```
Class Fusion_Response extend Response {
    public Request request;
    public Fusion_Data[] data = [];
    public Status status;
};
```
---


### 属性


* #### request

> type :　`object(Request)`

> desc : 服务名称

> value : see [4.1.1. Request Object](/definition/request_object.html#411-request-object)



* #### data

> type :　`object(Fusion_Data)[]`

> length: 0 ... 1

> desc : 融合信息服务请求应答的数据对象集合；当服务调用异常时，可以为空，查询成功时，集合长度可为0或1

> value : see [4.1.4.1. Fusion_Data Object](/definition/fusion_data_object.html#4143-fusion_data-object)



* #### status

> type :　`object(Status)`

> desc : 当前服务请求的服务应答状态

> value : see [4.1.3. Status Object](/definition/status_object.html#413-status-object)



### DUMP

```
object(Response) {
    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : object(Fusion_Data) {}
    "status" : object(Status) {
        "code" : enum(0000),
        "message" : string("success!"),
        "timestamp" : float(1427259974.2252)
    }
}
```
