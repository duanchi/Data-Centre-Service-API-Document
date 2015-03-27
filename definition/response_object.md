# 4.1.2. Response Object




### 定义

> Class Response_Abstract extend StdObject {};




### 属性


* #### service

> type :　`enum`

> desc : 服务名称

> value : 枚举值请参考 `4.2.1.`



* #### data

> type :　`object(StdObject)` [?]

> desc : 数据对象

> value : 需子类定义



* #### status

> type :　`object(Status)`

> desc : 当前服务请求的服务应答状态

> value : 服务应答状态对象

- service : enum              `服务名称`
- data : object(StdObject)[?] `数据对象`
- status : object(Status)     `状态对象`


```
object(Response) {
    "data" : object() {}
    "status" : object(Status) {
        code : int(0),
        message : string("success!"),
        timestamp : float(1427259974.2252)
    }
}

```
