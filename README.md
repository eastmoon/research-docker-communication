# research-docker-communication

理想情況上，系統的服務皆容器化，僅需考量使用 API 在服務間進行通訊；然而，實務過程中，無論從大泥巴的系統逐步分切的成容器服務，還是容器服務中存在不具有 API 的應用程式，這都會導致這些服務容器化後不再有適合的溝通方式。

基於上述考量，本項目將調查與研究容器與主機間的通訊方式。

## 系統結構

本項目僅考慮執行於 Linux 作業系統，因此會基於 VirtualBox 建立開發環境，並分享研究程式目錄。

```
repository
  └ app\
  └ conf\
  └ Vagrantfile
```

## 通訊方式

單一容器會基於以下專案讓外部對其系統進行溝通。

+ API
+ SSH
+ Sock

## 通訊對象

單一容器如何與其他服務進行溝通

+ docker with docker
+ docker with host

## 服務探勘與溝通

單一容器登記於服務探勘系統，並透過探勘系統互相溝通

+ Consul
+ 簡易版的服務探勘架構
	- domain socket
	- mosquitto

## 文獻

+ [How To Communicate Between Docker Containers Via “Hostname”?](https://www.geeksforgeeks.org/how-to-communicate-between-docker-containers-via-hostname/)
