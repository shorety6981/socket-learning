# socket函数
### linux系统
#### <sys/socket.h> 头文件中 socket() 函数来创建套接字       
`int socket(int af, int type, int protocol);`       

1) af 为地址族（Address Family）--- IP 地址类型        
常用的有 AF_INET 和 AF_INET6。            
AF 是“Address Family”的简写，INET是“Inetnet”的简写。          
AF_INET 表示 IPv4 地址，例如 127.0.0.1；AF_INET6 表示 IPv6 地址，例如 1030::C9B4:FF12:48AA:1A2B。         
大家需要记住127.0.0.1，它是一个特殊IP地址，表示本机地址       

2) type 为数据传输方式/套接字类型         
常用的有 SOCK_STREAM（TCP/流格式套接字/面向连接的套接字）和 SOCK_DGRAM（UDP/数据报套接字/无连接的套接字）         

3) protocol 表示传输协议
常用的有 IPPROTO_TCP 和 IPPTOTO_UDP，分别表示 TCP 传输协议和 UDP 传输协议   
#### 创建TCP套接字
`int sock = socket(AF_INET, SOCK_STREAM, 0); `


### windows系统
#### <sys/socket.h> 头文件中 socket() 函数来创建套接字
windows的返回值类型不同，是一个SOCKET 类型的句柄，linux中把socket看做文件，但windows不这么看      
 `SOCKET socket(int af, int type, int protocol);`
#### 创建TCP套接字
`SOCKET sock = socket(AF_INET, SOCK_STREAM, 0); `
