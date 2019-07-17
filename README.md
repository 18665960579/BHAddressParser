# 地址智能解析器
收货人或寄件人


## 简介
 1. 能够识别多种结构的地址信息
 2. 兼容解析常用平台App的复制地址信息
 3. 结合NSDataDetector智能高效识别，未直接使用地址库检索
 
### 支持的格式

* **姓名+地址+电话：**马云北京市朝阳区富康路姚家园3楼15000000000
* **姓名+电话+地址：**马云150-0000-0000北京市朝阳区富康路姚家园3楼
* **地址+电话+姓名：**北京市朝阳区富康路姚家园3楼15000000000马云
* **地址+姓名+电话：**北京市朝阳区富康路姚家园3号楼5单元3305马云15000000000
* **电话+姓名+地址：**15000000000马云北京市朝阳区富康路姚家园3号楼5单元3305邮编038300
* **电话+地址+姓名：**15000000000北京市朝阳区富康路姚家园3号楼5单元3305马云
* **复制-淘宝-收货人:**            
    * 收货人: 学宝\n手机号码: 13888888888\n所在地区: 浙江省杭州市江干区白杨街道\n详细地址: 天真小区顽皮苑6幢3单元2019室
* **复制-微信-我的地址:**
    * 联系人：学宝\n手机号码：05716666888\n地区：浙江省 杭州市 江干区\n详细地址：经济技术开发区新加坡杭州科技园188幢\n邮政编码：310016
* **复制-京东-地址管理:**
    * 姓名：学宝\n地址：安徽合肥市瑶海区城区 合肥市瑶海区胜利路126号


### 不支持的格式

* 马云北京市朝阳区富康路姚家园3楼150-0000-0000
* 北京市朝阳区富康路姚家园3楼150-0000-0000马云

**说明：**
1. 因电话用短线分割，且电话位于地址后面，解析时，会认为此处在描述详细地址，譬如16-1612室的场景。
2. 只是不支持对姓名和电话的解析。

    
## 使用
 
 ```
 pod BHAddressParser
 ```
 
**方式一:** 获取地址信息**字典**
 
 ```
 + (nonnull NSDictionary<BHAddressParserKey, NSString *> *)bh_parserToAddressDictionaryWithText:(nonnull NSString *)text;

 ```
 
**方式二:** 获取地址信息**对象**

```
+ (nonnull BHAddressModel *)bh_parserToAddressModelWithText:(nonnull NSString *)text;
``` 
 

## 作者
学宝  zhanxuebao@outlook.com


**写出你能看懂的代码，而不只是机器能读懂的代码。**


