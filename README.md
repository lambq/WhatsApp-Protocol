---
title: WhatsApp Protocol Register API
language_tabs:
- shell: Shell
- http: HTTP
- javascript: JavaScript
- ruby: Ruby
- python: Python
- php: PHP
- java: Java
- go: Go
  toc_footers: []
  includes: []
  search: true
  code_clipboard: true
  highlight_theme: darkula
  headingLevel: 2
  generator: "@tarslib/widdershins v4.0.23"

---

# WhatsApp Protocol Register API


Base URLs:

* <a href="http://127.0.0.1:8000">开发环境: http://127.0.0.1:8000</a>

# Authentication

# Default

## POST 发送验证码

POST /api/v1/send

> Body 请求参数

```yaml
proxy: socks5://name:pass@8.217.88.255:19565
phone: "8613293590689"
name: Android
version: string
maker: OPPO
dname: PGBM10

```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |none|
|body|body|object| 否 |none|
|» proxy|body|string| 否 |socks5://username:password@111.222.111.222:1080 or socks5://111.222.111.222:1080|
|» phone|body|string| 否 |8613293590692|
|» name|body|string| 否 |设备名称 例如：Android|
|» version|body|string| 否 |设备版本 例如：13/10/11/12/14/8.0.0/9.1.0|
|» maker|body|string| 否 |设备制造商 例如：Google/Xiaomi/OPPO|
|» dname|body|string| 否 |设备型号 例如：Pixel_4/2201123C/PCLM50|

> 返回示例

> 成功

```json
{
  "status": "sent",
  "length": 6,
  "retry_after": 125,
  "method": "sms",
  "sms_wait": 125,
  "voice_wait": 125,
  "login": "8613293590665",
  "flash_type": 1,
  "wa_old_wait": 65,
  "email_otp_wait": 65,
  "notify_after": 86400
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## PUT 确认验证码

PUT /api/v1/send/8613293590665

> Body 请求参数

```yaml
proxy: socks5://name:pass@155.138.200.141:7305
code: "793630"
name: Android
version: "11"
maker: samsung
dname: SM-A525F

```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |none|
|body|body|object| 否 |none|
|» proxy|body|string| 否 |socks5://username:password@111.222.111.222:1080 or socks5://111.222.111.222:1080|
|» code|body|string| 否 |12123|
|» name|body|string| 否 |设备名称 例如：Android|
|» version|body|string| 否 |设备版本 例如：13/10/11/12/14/8.0.0/9.1.0|
|» maker|body|string| 否 |设备制造商 例如：Google/Xiaomi/OPPO|
|» dname|body|string| 否 |设备型号 例如：Pixel_4/2201123C/PCLM50|

> 返回示例

> 成功

```json
{
  "status": "ok",
  "type": "new",
  "lid": "130262600048846",
  "login": "8613293590665",
  "security_code_set": false,
  "autoconf_type": 1,
  "secure_verifier": false
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## GET 获取协议号

GET /api/v1/send/8613293590665

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|Authorization|header|string| 是 |none|

> 返回示例

> 成功

```json
{
  "status": "ok",
  "data": "8613293590665,f34kFAKdTUe2J6DCKZpvPZvaGk+jHmzKf7dsv2vkIFg=,X4le32gWbDNb2Wb95kKwIqdT5aAd5sCTBDkMnGgJdko=,BWVfd3e7Oe1Aqj6UttMNX4lrNxi7uaH3WzauK0RjH3Yl,h+aV2KOXqRyIm6zJTmsttm/Uhwjb9fSYsKgY+iE9x5o=,Yjg5OGUzMmItYTVhYi00NDgyLWJlNmYtMDBjYWEwN2MzODQ2"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# 数据模型

### Contact information 

> TG：@xq1233217
> TG：@whatappfly
