# Object Definition


## 4.1.1. Response Object


### Response Object

`Class Response extend StdObject {}`

> - service : enum              `服务名称`
> - data : object(StdObject)[?] `数据对象`
> - status : object(Status)     `状态对象`


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


### Fusion_Response Object

`Class Fusion_Response extend Response {}`

> - data : object(Fusion_Profile)   `融合信息对象`
> - service : enum                  `服务名称`
> - status : object(Status)         `状态对象`


```
object(Fusion_Response) {
    "service" : enum("cu.ecs.user-service.fusion"),
    "data" : object(Fusion_Profile) {},
    "status" : object(Status) {}
}
```

### Group_Response Object

`Class Group_Response extend Response {}`

> - data(Group_Profile)         `集团信息对象`
> - service(enum)               `服务名称`
> - status(Status)              `状态对象`

```
object(Group_Response) {
    "service" : enum("cu.ecs.user-profile.merge-profile"),
    "data" : object(Group_Profile) {},
    "status" : object(Status) {}
}
```
### Contract_Profile_Response Object

`Class Contract_Profile_Response extend Response {}`

> - data(Contract_Profile)         `合约信息对象`
> - service(enum)                  `服务名称`
> - status(Status)                 `状态对象`


```
object(Contract_Profile_Response) {
    "service" : enum("cu.ecs.user-profile.merge-profile"),
    "data" : object(Contract_Profile) {},
    "status" : object(Status) {}
}
```
`Class InAndOut_Profile_Response extend Response {}`

> - data(InAndOutt_Profile)         `入离网信息对象`
> - service(enum)                  `服务名称`
> - status(Status)                 `状态对象`


```
object(InAndOut_Profile_Response) {
    "service" : enum("cu.ecs.user-profile.merge-profile"),
    "data" : object(InAndOut_Profile) {},
    "status" : object(Status) {}
}
```


### Terminal_Response Object

`Class Terminal_Response extend Response {}`

> - data : object(Terminal_Profile) `终端信息对象`
> - service : enum                  `服务名称`
> - status : object(Status)         `状态对象`


```
object(Terminal_Response) {
    "service" : enum("cu.ecs.user-service.terminal"),
    "data" : object(Terminal_Profile) {},
    "status" : object(Status) {}
}
```

### Social_Response Object

`Class Social_Response extend Response {}`

> - data : object(Social_Response)  `社交帐号信息对象`
> - service : enum                  `服务名称`
> - status : object(Status)         `状态对象`


```
object(Social_Response) {
    "service" : enum("cu.ecs.user-service.social"),
    "data" : object(Social_Profile) {},
    "status" : object(Status) {}
}
```





##4.1.2. Status Object

`Class Status extend StdClass {}`

> - code : enum                 `服务应答状态`
> - message : string            `服务应答信息`
> - timestamp : float           `当前时间戳float(14,4)`


```
object(Status) {
    code : int(0),
    message : string("success!"),
    timestamp : float(1427259974.2252)
}
```









## 4.1.3. Profile Object


### Profile Object

`Class Profile extend StdClass {}`


```
object(Profile) {}
```


### User_Profile Object

`Class User_Profile extend Profile {}`

> - user_number : string        `用户号码`


```
object(User_Profile) {
    "user_number" : string("186xxxxxxxx")
}
```


### Fusion_Profile Object

`Class Fusion_Profile extend Profile {}`

> - wo_family : object(WOFamily_Profile)[?] `沃家庭对象`
> - 2 : NULL
> - 4 : NULL


```
object(Fusion_profile) {
    "wo_family" : object(WOFamily_Profile) {}
}
```


### WOFamily_Profile Object

`Class WOFamily_Profile extend Profile {}`

> - product : object(Wofamily_Product)  `沃家庭产品信息`
>   - name : string                     `沃家庭产品名称`
> - master : object(User_Profile)       `主用户对象`
> - slave : object(User_Profile)[+]     `成员用户对象`


```
object(WOFamily_Profile) {
    "product" : object(WOFamily_Product) {
        "name" : string("沃家庭91套餐"),
    },
    "master": object(User_Profile) {},
    "slave" : [
        object(User_Profile) {},
        ...
    ]
}
```


### Group_Profile Object

`Class Group_Profile extend StdClass {}`

> - product(Mygroup_Product)   `集团产品信息`
>   - name(string)               `集团名称`
> - master(User_Profile)        `主付费对象`
> - pay_type(enum)              `付费类型`


```
object(Mygroup_Profile) {
    "product" : object(Mygroup_Product) {
        "name" : string("中国联通集团"),
    },
    "master": object(User_Profile) {},
    "pay_type" :enum(1)
}

### Contract_Profile Object

`Class Contract_Profile extend StdClass {}`

> - 1(MyContract_Profile ?)       `集团对象`
> - 2(NULL)
> - 4(NULL)


```
object(MyContract_Profile) {
    "1" : object(MyContract_Profile) {}
}
```
### MyContract_Profile Object

`Class MyContract_Profile extend StdClass {}`

> - product(Mycontract_Product)   `合约产品信息`
>   - name(string)               `合约名称`
> - statime(Datetime)            `合约开始时间`
> - endtime(Datetime)            `合约结束时间`


```
object(MyContract_Profile) {
    "product" : object(Mycontract_Product) {
        "name" : string("iPhone 96元合约套餐"),
    },
    "statime": Datetime(xxxx-xx-xx),
    "endtime": Datetime(xxxx-xx-xx),
}

```
### InAndOut_Profile Object

`Class Contract_Profile extend StdClass {}`

> - 1(MyInAndOut_Profile ?)       `入离网对象`
> - 2(NULL)
> - 4(NULL)


```
object(MyInAndOut_Profile) {
    "1" : object(MyInAndOut_Profile) {}
}
```
### MyInAndOut_Profile Object

`Class MyInAndOut_Profile extend StdClass {}`

> - product(MyInAndOut_Product?)   `入离网信息`
>   - Entry(User_Profile)          `入网号码`
>   - statime(Datetime)            `入网时间`
>   - InAndOut_type(enum)           `是否离网`
>   - endtime(Datetime?)           `离网时间`
> - 注: 还在网的情况下endtime为空

```
object(MyContract_Profile) {
    "product" : object(Mycontract_Product) {
         "Entry" : object(User_Profile) {
                "number" : string("010xxxxxxxx")
                 },
         "statime": Datetime(xxxx-xx-xx),
         "InAndOut_type" : enum(2),
         "endtime": Datetime(xxxx-xx-xx),
    },

}

```



### Terminal_Profile Object

`Class Terminal_Profile extend Profile {}`

> - imei : string                       `设备号码`
> - phone : object(Phone_Profile)       `移动终端信息`
> - start_time : date                   `开始使用日期`
> - end_time : date[?]                  `结束使用信息`


```
object(Terminal_Profile) {
    "imei" : string("xxxxxxxxxxxxx"),
    "phone" : object(Phone_Profile) {},
    "start_time" : date("2015-01-12")
}
```



### Phone_Profile Object

`Class Phone_Profile extend Profile {}`

> - manufacturer : string               `移动终端厂商`
> - model : string                      `移动终端型号`


```
object(Phone_Profile) {
    "manufacturer" : string("Apple."),
    "model" : string("6,A1597")
}
```



### Social_Profile Object

`Class Social_Profile extend Profile {}`

> - weibo : object(Weibo_Profile)[?]    `微博帐号信息`
> - wechat : object(Wechat_Profile)[?]  `微信帐号信息`
> - qq : object(Qq_Profile)[?]          `QQ帐号信息`


```
object(Social_Profile) {
    "weibo" : object(Weibo_Profile) {
            "scope" : enum("weibo"),
            "user" : string("07.duanchi@gmail.com"),
            "homepage" : string("weibo.com/shijingye"),
        },
        "wechat" : object(Wechat_Social_Profile) {
            "scope" : enum("wechat"),
            "user" : string("68661364")
        },
        "qq" : object(Qq_Social_Profile) {
            "scope" : enum("qq"),
            "user" : string("68661364")
        },
}
```


### Weibo_Profile Object

`Class Weibo_Profile extend Profile {}`

> - scope : enum("weibo")               `帐号类别`
> - user : string                       `用户名`
> - homepage : string                   `主页`


```
object(Weibo_Profile) {
    "scope" : enum("weibo"),
    "user" : string("07.duanchi@gmail.com"),
    "homepage" : string("weibo.com/shijingye")
}
```


### Wechat_Profile Object

`Class Wechat_Profile extend Profile {}`

> - scope : enum("weichat")             `帐号类别`
> - user : string                       `用户名`


```
object(Weibo_Profile) {
    "scope" : enum("wechat"),
    "user" : string("68661364")
}
```


### Qq_Profile Object

`Class Qq_Profile extend Profile {}`

> - scope : enum("qq")                  `帐号类别`
> - user : string                       `用户名`


```
object(Qq_Profile) {
    "scope" : enum("qq"),
    "user" : string("68661364"),
}
```


## 4.1.4. Product Object
