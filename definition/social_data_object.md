# 4.1.4.8. Social_Data Objects



> 社交帐号信息对象


### 定义

---
```
Class Social_Data extend StdClass {
    public enum type;
    public string user;
};
```
---



### 属性


* #### type

> type :　`enum`

> desc : 社交帐号类型

> value :

> - `weixin` 微信

> - `weibo` 微博

> - `qq` QQ


* #### user

> type :　`string`

> desc : 社交帐号

> value : 社交帐号



### DUMP

```
object(Social_Data) {
    "type" : enum(weibo),
    "user" : string("duanchi")
}
```

