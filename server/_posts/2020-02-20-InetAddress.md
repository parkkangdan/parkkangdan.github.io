---
layout: post
title: InetAddress
author: author1
noindex: true
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

