# 4.1.4.4. Group_Data Object

> 集团客户信息服务数据对象


### 定义

---
```
Class Group_Data extend StdClass {
    public string id;
    public string code;
    public string name;
    public string type;
    public string[] properties = [];
    public string address;
    public enum province;
    public enum city;
    public enum district;
    public string up_level_id = "";
};
```
---


### 属性


* #### id

> type :　`string`

> desc : 当前用户所在集团客户的集中集客系统标识

> value : 集中集客系统标识


* #### code

> type :　`string`

> desc : 当前用户所在集团客户的集团编码

> value : 集团编码


* #### name

> type :　`string`

> desc : 当前用户所在集团客户的集团名称

> value : 集团名称


* #### type

> type :　`string`

> desc : 当前用户所在集团客户的集团类型

> value : 集团类型


* #### properties

> type :　`string[]`

> desc : 当前用户所在集团客户的集团属性

> value : 集团属性集合


* #### province

> type :　`enum`

> desc : 当前用户所在集团客户的所属省

> value : 所属省，see [B-SDM Provice Code](/appendix/b-sdm_code.html/#province-code)


* #### city

> type :　`enum`

> desc : 当前用户所在集团客户的所属地市

> value : 所属地市，see [B-SDM City Code](/appendix/b-sdm_code.html/#city-code)


* #### district

> type :　`enum`

> desc : 当前用户所在集团客户的所属区域

> value : 所属区域，see [B-SDM District Code](/appendix/b-sdm_code.html/#district-code)


* #### up_level_id

> type :　`string`

> desc : 当前用户所在集团客户的上级集团客户编码

> value : 若存在上级集团客户，则值上级集团客户编码


### DUMP

```
object(Group_Data) {
    "id" : string("x89111011"),
    "code" : string("1101101011"),
    "name" : string("中国联通集团公司"),
    "type" : [
        string("通信"),
        string("国企")
    ],
    "province" : enum(10),
    "city" : enum(101),
    "district" : enum(101002)
    }
}
```
