---   
layout: server
author: author1  
title: [Server] InetAddress
date: 2020-02-20 17:14
description: description 내용  
---  

# 서버 IP확인
###### "java.net.InetAddress" 활용하기

import java.net.InetAddress;


```
public static String ServerIp() {
    try {
      ip = InetAddress.getLocalHost();
      Logger.info("Server IP = [" + ip.getHostAddress() + "]");
      return ip.getHostAddress();
    }
    catch (UnknownHostException e) {
    Logger.error("IP 확인 실패" + e.getLocalizedMessage());
      return "";
    }
  }
```

