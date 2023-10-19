## 第三章 套接字编程
### 套接字地址结构
每个协议族都定义自己的套接字地址结构，这些结构的名字都以sockaddr_开头，以每个协议族的唯一后缀结尾。

1. sockaddr_in：IPv4套接字地址结构
![sockaddr_in](../notes/res/sockaddr_in_struct.png)
2. sockaddr: 通用套接字地址结构
![sockaddr](./res/sockaddr_struct.png)
3. sockaddr_in6:IPv6套接字地址结构
![sockaddr_in6](./res/sockaddr_in6.png)
