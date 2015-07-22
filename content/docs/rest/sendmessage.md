---
title: REST API 开发指南
secondnavrest: true
sidebar: restsidebar
---

# 聊天相关API

## 发送消息的流程说明
1. 发送 ** 文字 ** / **透传** 消息直接编辑内容发送
2. 发送 **图片** / **语音** / **视频** 消息需要先上传这三类文件，从接口返回值中获取到相应的参数，按照API要求编辑到消息体中然后的发送。


## 发送文本消息 {#sendmsg}

> 给一个或者多个用户, 或者一个或者多个群组发送消息, 并且通过可选的 _from_ 字段让接收方看到发送方是不同的人,同时, 支持扩展字段, 通过 _ext_ 属性, app可以发送自己专属的消息结构.

> **接口限流说明: 同一个IP每秒最多可调用30次, 超过的部分会返回503错误, 所以在调用程序中, 如果碰到了这样的错误, 需要稍微暂停一下并且重试。如果该限流控制不满足需求，请联系商务经理开放更高的权限。**

- Path : /{org_name}/{app_name}/messages
- Request Method : POST
- URL Params ： 无
- Request Headers :  {"Content-Type":"application/json","Authorization":"Bearer ${token}"}
- Response Body ： 详情参见示例返回值, 返回的json数据中会包含除上述属性之外的一些其他信息，均可以忽略。
- 可能的错误码： <br/>
404 （此用户或groupid不存在） <br/>401（未授权[无token,token错误,token过期]） <br/>5xx <br/> 详见：[REST接口错误码](http://www.easemob.com/docs/helps/errorcodes/) 
- Request Body ： 

<pre class="hll"><code class="language-java">
{
    "target_type" : "users", // users 给用户发消息, chatgroups 给群发消息
    "target" : ["u1", "u2", "u3"], // 注意这里需要用数组,数组长度建议不大于20, 即使只有一个用户,   
                                   // 也要用数组 ['u1'], 给用户发送时数组元素是用户名,给群组发送时  
                                   // 数组元素是groupid
    "msg" : {
        "type" : "txt",
        "msg" : "hello from rest" //消息内容，参考[聊天记录](http://www.easemob.com/docs/rest/chatmessage/)里的bodies内容
        },
    "from" : "jma2", //表示这个消息是谁发出来的, 可以没有这个属性, 那么就会显示是admin, 如果有的话, 则会显示是这个用户发出的    
    "ext" : { //扩展属性, 由app自己定义.可以没有这个字段，但是如果有，值不能是“ext:null“这种形式，否则出错
        "attr1" : "v1",
        "attr2" : "v2"
    }    
}
</code></pre>

#### curl示例

<pre class="hll"><code class="language-java">
curl -X POST -i -H "Authorization: Bearer YWMtxc6K0L1aEeKf9LWFzT9xEAAAAT7MNR_9OcNq-GwPsKwj_TruuxZfFSC2eIQ" "https://a1.easemob.com/easemob-demo/chatdemoui/messages" -d '{"target_type" : "users","target" : ["stliu1", "jma3", "stliu", "jma4"],"msg" : {"type" : "txt","msg" : "hello from rest"},"from" : "jma2", "ext" : {"attr1" : "v1","attr2" : "v2"} }'
</code></pre>

#### Response 示例：

<pre class="hll"><code class="language-java">
{
    "action": "post",
    "application": "4d7e4ba0-dc4a-11e3-90d5-e1ffbaacdaf5",
    "params": {},
    "uri": "https://a1.easemob.com/easemob-demo/chatdemoui",
    "entities": [],
    "data": {
        "stliu1": "success",
        "jma3": "success",
        "stliu": "success",
        "jma4": "success"
    },
    "timestamp": 1404932446668,
    "duration": 110,
    "organization": "easemob-demo",
    "applicationName": "chatdemoui"
}
</code></pre>


## 发送图片消息 {#sendimgmsg}

> 给一个或者多个用户, 或者一个或者多个群组发送消息, 并且通过可选的 _from_ 字段让接收方看到发送方是不同的人,同时, 支持扩展字段, 通过 _ext_ 属性, app可以发送自己专属的消息结构.
> 
> **接口限流说明: 同一个IP每秒最多可调用30次, 超过的部分会返回503错误, 所以在调用程序中, 如果碰到了这样的错误, 需要稍微暂停一下并且重试。如果该限流控制不满足需求，请联系商务经理开放更高的权限。**

- Path : /{org_name}/{app_name}/messages
- Request Method : POST
- URL Params ： 无
- Request Headers :  {"Content-Type":"application/json","Authorization":"Bearer ${token}"}
- Response Body ： 详情参见示例返回值, 返回的json数据中会包含除上述属性之外的一些其他信息，均可以忽略。
- 可能的错误码：<br/>
404 （此用户或groupid不存在）  <br/>401（未授权[无token,token错误,token过期]） <br/>5xx <br/> 详见：[REST接口错误码](http://www.easemob.com/docs/helps/errorcodes/) 
- Request Body ： 

<pre class="hll"><code class="language-java">
{
    "target_type" : "users",   //users 给用户发消息, chatgroups 给群发消息
    "target" : ["u1", "u2", "u3"],// 注意这里需要用数组,数组长度建议不大于20, 即使只有一个用户,   
                                  // 也要用数组 ['u1'], 给用户发送时数组元素是用户名,给群组发送时  
                                  // 数组元素是groupid
    "msg" : {  //消息内容
        "type" : "img",   // 消息类型
	    "url": "https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/55f12940-64af-11e4-8a5b-ff2336f03252",  //成功上传文件返回的uuid
	    "filename": "24849.jpg", // 指定一个文件名
	    "secret": "VfEpSmSvEeS7yU8dwa9rAQc-DIL2HhmpujTNfSTsrDt6eNb_", // 成功上传文件后返回的secret
	    "size" : {
          "width" : 480,
          "height" : 720
      }
     },
    "from" : "jma2", //表示这个消息是谁发出来的, 可以没有这个属性, 那么就会显示是admin, 如果有的话, 则会显示是这个用户发出的    
    "ext" : { //扩展属性, 由app自己定义.可以没有这个字段，但是如果有，值不能是“ext:null“这种形式，否则出错
        "attr1" : "v1",
        "attr2" : "v2"
    }    
}
</code></pre>

#### curl示例

<pre class="hll"><code class="language-java">
curl -X POST -i 'https://a1.easemob.com/easemob-demo/chatdemoui/messages'   -H 'Authorization: Bearer YWMtsFVigGSuEeSTc7k5183Z5QAAAUqzeFx_9IjRch-ZxNbIlBIvx_4GWvzheSU'  -d '{"target_type":"users","target":["l1k4vpllxp"],"from":"jma2","msg":{"type":"img","filename":"24849.jpg","secret":"VfEpSmSvEeS7yU8dwa9rAQc-DIL2HhmpujTNfSTsrDt6eNb_","url":"https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/55f12940-64af-11e4-8a5b-ff2336f03252"},"size":{"width":480,"height":720}}
</code></pre>

#### Response 示例：

<pre class="hll"><code class="language-java">
{
  "action" : "post",
  "application" : "4d7e4ba0-dc4a-11e3-90d5-e1ffbaacdaf5",
  "uri" : "https://a1.easemob.com/easemob-demo/chatdemoui",
  "entities" : [ ],
  "data" : {
   	 "l1k4vpllxp" : "success"
  },
  "timestamp" : 1415166497129,
  "duration" : 12,
  "organization" : "easemob-demo",
  "applicationName" : "chatdemoui"
}
</code></pre>


##  发送语音消息  {#sendvoicemsg}

> 发送语音文件，需要先上传语音文件，然后再发送此消息。（url中的uuid和secret可以从上传后的response获取）
> 
> **接口限流说明: 同一个IP每秒最多可调用30次, 超过的部分会返回503错误, 所以在调用程序中, 如果碰到了这样的错误, 需要稍微暂停一下并且重试。如果该限流控制不满足需求，请联系商务经理开放更高的权限。**

- Path : /{org_name}/{app_name}/messages
- Request Method : POST
- URL Params ： 无
- Request Headers :  {"Content-Type":"application/json","Authorization":"Bearer ${token}"}
- Response Body ： 详情参见示例返回值, 返回的json数据中会包含除上述属性之外的一些其他信息，均可以忽略。
- 可能的错误码：<br/>
404 （此用户或groupid不存在）<br/>401（未授权[无token,token错误,token过期]） <br/>5xx <br/> 详见：[REST接口错误码](http://www.easemob.com/docs/helps/errorcodes/) 

- Request Body ：


<pre class="hll"><code class="language-java">
{
	"target_type" : "users",  //users 给用户发消息, chatgroups 给群发消息
	"target" : ["testd", "testb", "testc"],// 注意这里需要用数组,数组长度建议不大于20, 即使只有一个  
                                           // 用户或者群组, 也要用数组形式 ['u1'], 给用户发送  
                                           // 此数组元素是用户名,给群组发送时数组元素是groupid
	"msg" : {   //消息内容
		"type": "audio",  // 消息类型
		"url": "https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/1dfc7f50-55c6-11e4-8a07-7d75b8fb3d42",  //成功上传文件返回的uuid
		"filename": "messages.amr", // 指定一个文件名
		"length": 10,
		"secret": "Hfx_WlXGEeSdDW-SuX2EaZcXDC7ZEig3OgKZye9IzKOwoCjM" // 成功上传文件后返回的secret
	},
	"from" : "testa" ,  //表示这个消息是谁发出来的, 可以没有这个属性, 那么就会显示是admin, 如果有的话, 则会显示是这个用户发出的
	"ext" : { //扩展属性, 由app自己定义.可以没有这个字段，但是如果有，值不能是“ext:null“这种形式，否则出错
       	 	"attr1" : "v1",
        	"attr2" : "v2"
    	}	 
}
</code></pre>

#### curl示例

<pre class="hll"><code class="language-java">
curl -X POST -H "Authorization: Bearer YWMtxc6K0L1aEeKf9LWFzT9xEAAAAT7MNR_9OcNq-GwPsKwj_TruuxZfFSC2eIQ" "https://a1.easemob.com/easemob-demo/chatdemoui/messages" -d '{"target_type" : "users","target" : ["testd", "testb", "testc"],"msg" : {"type": "audio","url": "https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/1dfc7f50-55c6-11e4-8a07-7d75b8fb3d42","filename": "messages.amr","length": 10,"secret": "Hfx_WlXGEeSdDW-SuX2EaZcXDC7ZEig3OgKZye9IzKOwoCjM"},"from" : "testa" }'
</code></pre>

#### Response 示例：

<pre class="hll"><code class="language-java">
{
  "action" : "post",
  "application" : "4d7e4ba0-dc4a-11e3-90d5-e1ffbaacdaf5",
  "uri" : "https://a1.easemob.com/easemob-demo/chatdemoui",
  "entities" : [ ],
  "data" : {
    "testd" : "success",
    "testb" : "success",
    "testc" : "success"
  },
  "timestamp" : 1415166234863,
  "duration" : 5,
  "organization" : "easemob-demo",
  "applicationName" : "chatdemoui"
}
</code></pre>

## 发送视频消息  {#sendvideomsg}

> 发送视频消息，需要先上传视频文件和视频缩略图文件，然后再发送此消息。（url中的uuid和secret可以从上传后的response获取）
> 
> **接口限流说明: 同一个IP每秒最多可调用30次, 超过的部分会返回503错误, 所以在调用程序中, 如果碰到了这样的错误, 需要稍微暂停一下并且重试。如果该限流控制不满足需求，请联系商务经理开放更高的权限。**

- Path : /{org_name}/{app_name}/messages
- Request Method : POST
- URL Params ： 无
- Request Headers :  {"Content-Type":"application/json","Authorization":"Bearer ${token}"}
- Response Body ： 详情参见示例返回值, 返回的json数据中会包含除上述属性之外的一些其他信息，均可以忽略。
- 可能的错误码：<br/>
404 （此用户或groupid不存在）<br/>401（未授权[无token,token错误,token过期]） <br/>5xx <br/> 详见：[REST接口错误码](http://www.easemob.com/docs/helps/errorcodes/) 

- Request Body ：

<pre class="hll"><code class="language-java">
{
    "target_type": "users", //users 给用户发消息, chatgroups 给群发消息
    "target": [
        "ceshib"// 注意这里需要用数组,数组长度建议不大于20, 即使只有一个，// 用户或者群组, 也要用数组形式 ['u1'], 给用户发送
    ], // 此数组元素是用户名,给群组发送时数组元素是groupid
    "from": "ceshia",
    "msg": { //消息内容
        "type": "video",// 消息类型
        "filename": "1418105136313.mp4",// 视频文件名称
        "thumb": "https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/67279b20-7f69-11e4-8eee-21d3334b3a97",//成功上传视频缩略图返回的uuid
        "length": 10,//视频播放长度
        "secret": "VfEpSmSvEeS7yU8dwa9rAQc-DIL2HhmpujTNfSTsrDt6eNb_",// 成功上传视频文件后返回的secret
        "file_length": 58103,//视频文件大小
        "thumb_secret": "ZyebKn9pEeSSfY03ROk7ND24zUf74s7HpPN1oMV-1JxN2O2I",// 成功上传视频缩略图后返回的secret
        "url": "https://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/671dfe30-7f69-11e4-ba67-8fef0d502f46"//成功上传视频文件返回的uuid
    }
}

</code></pre>

#### curl示例

<pre class="hll"><code class="language-java">

curl -X POST -i 'https://a1.easemob.com/easemob-demo/chatdemoui/messages' -H 'Authorization: Bearer YWMtxc6K0L1aEeKf9LWFzT9xEAAAAT7MNR_9OcNq-GwPsKwj_TruuxZfFSC2eIQ'  -d '{"target_type":"users","target":["testd","testb","testc"],"from":"testa","msg":{"type":"video","filename" : "1418105136313.mp4","thumb" : "http://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/67279b20-7f69-11e4-8eee-21d3334b3a97","length" : 0,"secret":"VfEpSmSvEeS7yU8dwa9rAQc-DIL2HhmpujTNfSTsrDt6eNb_","file_length" : 58103,"thumb_secret" : "ZyebKn9pEeSSfY03ROk7ND24zUf74s7HpPN1oMV-1JxN2O2I","url" : "http://a1.easemob.com/easemob-demo/chatdemoui/chatfiles/671dfe30-7f69-11e4-ba67-8fef0d502f46"}}'
</code></pre>

#### Response 示例：

<pre class="hll"><code class="language-java">
{
  "action" : "post",
  "application" : "4d7e4ba0-dc4a-11e3-90d5-e1ffbaacdaf5",
  "uri" : "https://a1.easemob.com/easemob-demo/chatdemoui",
  "entities" : [ ],
  "data" : {
    "testd" : "success",
    "testb" : "success",
    "testc" : "success"
  },
  "timestamp" : 1415166234863,
  "duration" : 5,
  "organization" : "easemob-demo",
  "applicationName" : "chatdemoui"
}
</code></pre>

## 发送透传消息  {#sendpayloadmsg}

>透传消息：不会在客户端提示（铃声，震动，通知栏等），但可以在客户端监听到的消息推送，具体功能可以根据自身自定义

> **接口限流说明: 同一个IP每秒最多可调用30次, 超过的部分会返回503错误, 所以在调用程序中, 如果碰到了这样的错误, 需要稍微暂停一下并且重试。如果该限流控制不满足需求，请联系商务经理开放更高的权限。**

- Path : /{org_name}/{app_name}/messages
- Request Method : POST
- URL Params ： 无
- Request Headers :  {"Content-Type":"application/json","Authorization":"Bearer ${token}"}
- Response Body ： 详情参见示例返回值, 返回的json数据中会包含除上述属性之外的一些其他信息，均可以忽略。
- 可能的错误码：<br/>
404 （此用户或groupid不存在） <br/>401（未授权[无token,token错误,token过期]） <br/>5xx <br/> 详见：[REST接口错误码](http://www.easemob.com/docs/helps/errorcodes/) 
- Request Body ：

<pre class="hll"><code class="language-java">
{
	"target_type":"users",     // users 给用户发消息,  chatgroups 给群发消息
	"target":["testb","testc"], // 注意这里需要用数组,数组长度建议不大于20, 即使只有  
                                // 一个用户u1或者群组, 也要用数组形式 ['u1'], 给用户发  
                                // 送时数组元素是用户名,给群组发送时数组元素是groupid
	"msg":{  //消息内容
		"type":"cmd",  // 消息类型
		"action":"action1"
	},
	"from":"testa",  //表示这个消息是谁发出来的, 可以没有这个属性, 那么就会显示是admin, 如果有的话, 则会显示是这个用户发出的
	"ext":{   //扩展属性, 由app自己定义.可以没有这个字段，但是如果有，值不能是“ext:null“这种形式，否则出错
		"attr1":"v1",
		"attr2":"v2"
	}
}
</code></pre>

#### curl示例

<pre class="hll"><code class="language-java">
curl -X POST -H "Authorization:Bearer YWMtxc6K0L1aEeKf9LWFzT9xEAAAAT7MNR_9OcNq-GwPsKwj_TruuxZfFSC2eIQ" -i "https://a1.easemob.com/easemob-demo/chatdemoui/messages" -d '{"target_type":"users","target":["testb","testc"],"msg":{"type":"cmd","action":"action1"},"from":"testa","ext":{"attr1":"v1","attr2":"v2"}}'
</code></pre>

#### Response 示例：

<pre class="hll"><code class="language-java">
{
  "action" : "post",
  "application" : "4d7e4ba0-dc4a-11e3-90d5-e1ffbaacdaf5",
  "uri" : "https://a1.easemob.com/easemob-demo/chatdemoui",
  "entities" : [ ],
  "data" : {
    "testb" : "success",
    "testc" : "success"
  },
  "timestamp" : 1415167842297,
  "duration" : 4,
  "organization" : "easemob-demo",
  "applicationName" : "chatdemoui"
}
</code></pre>
