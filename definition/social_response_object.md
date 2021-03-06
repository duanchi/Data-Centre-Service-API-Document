# 4.1.2.6. Social_Response Object

> 用户使用终端信息应答对象



### 定义

---
```
Class Terminal_Response extend Response {
    public Request request;
    public Terminal_Status[] data = NULL;
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

> type :　`object(Status_Data)[]`

> length: 0 ... n

> desc : 用户使用终端信息对象集合；当服务调用异常时，可以为空，查询成功时，集合长度可为0或n

> value : see [4.1.4.7. Terminal_Data Object](/definition/terminal_data_object.html#4147-terminal_data-object)



* #### status

> type :　`object(Status)`

> desc : 当前服务请求的服务应答状态

> value : see [4.1.3. Status Object](/definition/status_object.html#413-status-object)



### DUMP

```
object(Terminal_Response) {
    "request" : object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    },
    "data" : [
        object(Terminal_Data) {
            ...
        }
    ],
    "status" : object(Status) {
        "code" : enum(0000),
        "message" : string("success!"),
        "timestamp" : float(1427259974.2252)
    }
}
```

