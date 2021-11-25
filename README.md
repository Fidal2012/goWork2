# bxd_errgroup_http

>基于 errgroup 实现一个 http server 的启动和关闭 ，以及 linux signal 信号的注册和处理，要保证能够一个退出，全部注销退出。

>启动程序
```
go run main.go

curl http://localhost:19990/ping
返回:
hello golang http! request: &{Method:GET URL:/ping Proto:HTTP/1.1 ProtoMajor:1 ProtoMinor:1 Header:map[Accept:[*/*] User-Agent:[curl/7.64.1]] Body:{} GetBody:<nil> ContentLength:0 TransferEncoding:[] Close:false Host:localhost:19990 Form:map[] PostForm:map[] MultipartForm:<nil> Trailer:map[] RemoteAddr:127.0.0.1:53129 RequestURI:/ping TLS:<nil> Cancel:<nil> Response:<nil> ctx:0xc00007c140}

然后ctrl+c
errgroup exit...
shutting down server...
errgroup exiting: get os signal: interrupt
```
