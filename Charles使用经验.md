# Charles

Charles是一种Mac平台比较好用的抓包工具，对包内容进行了自动解析，方便直观的查看请求及响应内容。同时包含包大小、响应时间等信息，是一个很好的测试流量及响应时长的工具。

#### 手机上抓包
    1.Mac机启动网络分享，开启热点；
    2.设置手机连接Ma机c热点，配置手动代理，服务器IP填写Mac机IP，端口8888；
    3.Charles上Proxy勾选Mac OS X Proxy；
    4.现在打开任意消耗流量的app就可以抓包了，主要Mac机上选择allow。
      
#### 两种视图
    Structure：按域名归类排序。
    Sequence：按时间排序。
    
#### 常用的视窗
    Overview：这里有URL、协议类型、IP地址、时间、速度及流量大小等信息。
    Request：在Headers栏可以直观的看到请求内容。
    Response：响应内容，一般也只看Headers。
    Summary、Chart、Notes比较少关注。

#### 抓HTTPS包
    我们需要两个证书
    1.SSL证书，Charlesproxy.com/getsl上下载；
    2.对应的应用证书，需要利用浏览器导出https证书，然后放到服务器上，建立web service，手机访问ip/xxx.crt获取。
