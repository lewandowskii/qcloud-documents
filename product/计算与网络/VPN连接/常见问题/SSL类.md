  
[](id:01)
### 创建 SSL 服务端过程中，本端网段、对端网段怎么填写？
- 本端网段：客户移动端访问的云上的网段，即您 VPN 网关所属于子网的网段，例如子网：10.0.0.0/18，此处可以填10.0.0.0/24、10.0.0.0/26、10.0.0.0/28、10.0.0.0/30等子集网段。
- 对端网段：分配给用户移动端用于云上 VPN 进行通信的网段，该网段请勿与腾讯侧 VPC CIDR 冲突。
  
[](id:02)
### SSL 连接不通原因
1. 公网不通，请检查公网连通性。
2. 公网 IP 是否检查，特别是跨境公网 IP，跨境公网 IP 禁止直接访问云上资源，一经发现将被封禁。
3. 子网路由未配。
  
[](id:03)
### SSL VPN 是否支持访问多 VPC？
暂不支持。
  
[](id:04)
### SSL 连接数可以修改吗？
目前暂时不支持，预计2023年支持，在创建前请提前规划 SSL 连接数。
  
[](id:05)
### SSL VPN 需要使用固定公网 IP 吗？
SSL VPN 连接不需要用户本地有固定的公网 IP 地址，支持 Windows/MAC/Linux 客户端、手机端使用 OpenVPN 连接到云上私有网络内部的实例。
  
[](id:06)
### SSL VPN 可以切换为 IPSec 吗？
不支持，IPSec VPN 和 SSL VPN 是两种不同形态的 VPN，不能互相切换。
  
[](id:07)
### 支持多个客户端使用同一份证书吗？
不支持，每个客户端只能使用一个 SSL 客户端配置证书。
  
[](id:08)
### SSL 连接数上限是多少？
SSL 连接数和网关的带宽有关，[5,100]Mbps最大支持100个 SSL 连接数，[200,500]Mbps最大支持500个 SSL 连接， 1000Mbps最大支持1000个 SSL 连接数。
