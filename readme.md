### 阿里云DDNS python脚本

建议使用python3运行此脚本，脚本所需模块如下：

```
json
os
re
sys
datetime
requests
aliyun-python-sdk-core-v3
aliyun-python-sdk-alidns

```

### 准备
需要准备的账户信息如下：

```
Access Key ID
Access Key Secret
账号ID
```

然后通过以上信息获取子域名的解析记录ID，请将`i_dont_know_record_id`设为`no`并运行脚本。

返还的内容如下：
```
Subdomain：esxi | RecordId：333434500000000
Subdomain：vcenter | RecordId：333434500000000
Subdomain：nas | RecordId：333434500000000
Subdomain：pfsense | RecordId：333434500000000
Subdomain：home | RecordId：333434500000000
Subdomain：kibana.home | RecordId：333434500000000
```

请选取需要作为DDNS使用的子域名并将其`RecordId`填写到脚本的指定位置即可。

### 获取IP的方式
脚本中有三个不同的`my_ip_method`，分别对应三个不同地址，请根据网络的实际情况选择速度最优的方式。
将选取好的方式填写到以下位置即可：
```
    rc_value = my_ip_method_3()
```

### 其他
建议将此脚本通过定时任务运行

### 联系
更多使用说明请浏览我的博客：
[通过python将阿里云DNS解析作为DDNS使用](https://enginx.cn/2016/08/22/%E9%80%9A%E8%BF%87python%E5%B0%86%E9%98%BF%E9%87%8C%E4%BA%91dns%E8%A7%A3%E6%9E%90%E4%BD%9C%E4%B8%BAddns%E4%BD%BF%E7%94%A8.html "通过python将阿里云DNS解析作为DDNS使用") 

或通过邮件与我联系：<contact@c4.hk>

### 协议授权
MPL 2.0