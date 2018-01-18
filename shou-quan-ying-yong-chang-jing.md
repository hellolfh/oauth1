# 授权应用场景



  
开发者需要根据各自的应用场景，选择适用的OAuth2.0授权流程：  


* 网站或者站外Web应用，请参考：Authorization Code流程；
 
* 桌面和无线客户端应用，请参考：Authorization Code流程，无server端的也可以使用Implicit Grant流程，无线客户端可以直接使用官方SDK，通过WebView方式使用授权页；
 
* 针对云平台的API授权，只是针对开发者，参考：百度OAuth2.0对外提供的开发者授权方式Developer Credentials。
 

以下介绍了三种应用场景方便开发者熟悉授权流程。

### Server端使用百度OAuth2.0授权调用开放API流程

1. 引导用户到如下地址进行授权：

```
http://openapi.baidu.com/oauth/2.0/authorize?
	response_type=code
&

	client_id=YOUR_CLIENT_ID
&

	redirect_uri=YOUR_REGISTERED_REDIRECT_URI
&

	scope=email
&

	display=popup

```

2. 如果用户同意授权,页面跳转至 YOUR\_REGISTERED\_REDIRECT\_URI/?code=CODE 。  
3. 换取Access Token。

```
https://openapi.baidu.com/oauth/2.0/token?
	grant_type=authorization_code
&

	code=CODE
&

	client_id=YOUR_CLIENT_ID
&

	client_secret=YOUR_CLIENT_SECRET
&

	redirect_uri=YOUR_REGISTERED_REDIRECT_URI

```

返回值

```
{
    "access_token": "1.a6b7dbd428f731035f771b8d15063f61.86400.1292922000-2346678-124328",
    "expires_in": 86400,
    "refresh_token": "2.385d55f8615fdfd9edb7c4b5ebdc3e39.604800.1293440400-2346678-124328",
    "scope": "basic email",
    "session_key": "ANXxSNjwQDugf8615OnqeikRMu2bKaXCdlLxn",
    "session_secret": "248APxvxjCZ0VEC43EYrvxqaK4oZExMB",
}

```

4. 使用获得的OAuth2.0 Access Token调用API  


### 移动端使用百度OAuth2.0授权调用开放API流程

1. 引导用户到如下地址进行授权：

```
http://openapi.baidu.com/oauth/2.0/authorize?
	response_type=token
&

	client_id=YOUR_CLIENT_ID
&

	redirect_uri=YOUR_REGISTERED_REDIRECT_URI
&

	scope=email
&

	display=popup
&

	state=xxx

```

2. 如果用户同意授权,页面跳转至 YOUR\_REGISTERED\_REDIRECT\_URI 在Fragment中追加如下参数。  


```
YOUR_REGISTERED_REDIRECT_URI#access_token=1.a6b7dbd428f731035f771b8d15063f61.86400.1292922000-2346678-124328
&
expires_in=86400
&
scope=basic%20email
&
session_key=ANXxSNjwQDugf8615OnqeikRMu2bKaXCdlLxn
&
session_secret=248APxvxjCZ0VEC43EYrvxqaK4oZExMB
&
state=xxx

```

3. 截获OAuth2.0 Access Token调用API。  


### 设备使用百度OAuth2.0授权调用开放API流程

1. 获取User Code和Device Code ：

```
  https://openapi.baidu.com/oauth/2.0/device/code?
    client_id=YOUR_CLIENT_ID
&

    response_type=device_code
&
 
    scope=basic,netdisk

```

2. 授权服务会返回一段JSON文本，其中包含一个二维码图片地址。  


```
{
	"device_code":"a82hjs723h72h3a82hjs723h72h3vb",
	"user_code":"8sjiae3p", 
	"verification_url":"https:\/\/openapi.baidu.com\/oauth\/2\.0\/device", 
	"qrcode_url":"http:\/\/openapi.baidu.com\/device\/qrcode\/6c6a8afee394f99e55eb25858\/2c885vjk",
	"expires_in":1800, 
	"interval":5
}


```

3. 引导用户通过其他终端去百度填写User Code并授权。  


```
 用户可使用手持智能终端扫描上一步中的二维码图片(qrcode_url字段) ，或者在浏览器中直接访问设备展现的授权网址
https://openapi.baidu.com/device


```

4.通过Device Code获取Access Token。

```
https://openapi.baidu.com/oauth/2.0/token?
	grant_type=device_token
&

	code=Device Code
&

	client_id=YOUR_CLIENT_ID
&

	client_secret=YOUR_CLIENT_SECRET

```

5. 使用获得的OAuth2.0 Access Token调用API。

