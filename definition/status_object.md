# 4.1.3. Status Object

> 服务应答状态对象



### 定义

---
```
Class Status extend StdClass {
    public enum code;
    public string message;
    public timestamp timestamp;
};
```
---


### 属性


* #### code

> type :　`enum`

> desc : 当前请求的应答状态编码

> value : 应答状态编码，see [4.2.2. Status Code Enum](/definition/status_code_enum.html#422-status-code-enum)


* #### message

> type :　`string`

> desc : 当前请求的应答状态描述

> value : 应答状态描述



### DUMP

```
object(Request) {
        id : uuid(550e8400-e29b-41d4-a716-446655440000),
        service : enum(cu.ecs.user-service.fusion)
    }
```

