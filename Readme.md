JS源文件加密应做执行程序处理负责会导致上传CF失败或者IP访问错误

## ip 请求响应格式
```
{
"as": "AS13335 Cloudflare, Inc.",
"asname": "CLOUDFLARENET",
"city": "Montreal",
"continent": "North America",
"continentCode": "NA",
"country": "Canada",
"countryCode": "CA",
"currency": "CAD",
"district": "",
"hosting": true,
"isp": "Cloudflare, Inc.",
"lat": 45.5019,
"lon": -73.5674,
"mobile": false,
"offset": -14400,
"org": "Cloudflare, Inc.",
"proxy": false,
"query": "2606:4700:20::ac43:498a",
"region": "QC",
"regionName": "Quebec",
"status": "success",
"timezone": "America/Toronto",
"zip": "H4X"
}

```
### 具体意思

```
as: 自治系统编号（AS Number），表示该 IP 地址所属的自治系统的编号（如 AS13335 表示 Cloudflare）。
asname: 自治系统名称，指示与该 IP 地址关联的自治系统的名称（如 CLOUDFLARENET）。
city: 城市，表示 IP 地址所在的城市（如 Montreal）。
continent: 大洲，表示 IP 地址所在的大洲（如 North America）。
continentCode: 大洲代码，表示大洲的国际代码（如 NA 表示北美洲）。
country: 国家，表示 IP 地址所在的国家（如 Canada）。
countryCode: 国家代码，表示国家的 ISO 3166-1 两字母代码（如 CA 表示加拿大）。
currency: 货币，表示该地区使用的货币（如 CAD 表示加元）。
district: 区域，表示 IP 地址所在的具体区域（该字段为空）。
hosting: 托管标识，表示该 IP 地址是否用于托管服务（true 表示是，false 表示否）。
isp: 互联网服务提供商，表示提供该 IP 地址的互联网服务公司（如 Cloudflare, Inc.）。
lat: 纬度，表示 IP 地址的地理位置的纬度（如 45.5019）。
lon: 经度，表示 IP 地址的地理位置的经度（如 -73.5674）。
mobile: 移动设备标识，表示该 IP 地址是否来自移动设备（false 表示不是移动设备）。
offset: 时区偏移，表示相对于 UTC 的时间偏移（如 -14400 秒，即 UTC-4）。
org: 组织，表示管理该 IP 地址的组织（如 Cloudflare, Inc.）。
proxy: 代理标识，表示该 IP 地址是否为代理服务器（false 表示不是代理服务器）。
query: 查询的 IP 地址，表示执行查询的目标 IP 地址（如 2606:4700:20::ac43:498a）。
region: 省/区域代码，表示 IP 地址所在的省或区域的代码（如 QC 表示魁北克省）。
regionName: 省/区域名称，表示 IP 地址所在的省或区域的名称（如 Quebec）。
status: 查询状态，表示查询的结果状态（如 success 表示查询成功）。
timezone: 时区，表示 IP 地址所在的时区（如 America/Toronto）。
zip: 邮政编码，表示 IP 地址所在地区的邮政编码（如 H4X）。
```


域名 -->  cloudflare cdn server --> 源服务器

IP <-->  cloudflare cdn server --> 源服务器

Tunnel cloudflare 
    => Vless  UUID
    => Trojan  PASSWORD

```https://trojan.hebo.uk/[验证信息]?sub```

```https://cf.hebo.uk/{ipv4, ipv6, domain, country}.{txt, csv}@[ProxyIP]```

```https://vless.hebo.uk/[验证信息]?sub&IP_URL=[优选IP地址文本]```

PROXYIP 使用ip地址不使用域名 因为要考虑负载均衡
CFIP 

IP_URL

80系端口(HTTP)：80，8080，8880，2052，2082，2086，2095
443系端口(HTTPS)：443，2053，2083，2087，2096，8443