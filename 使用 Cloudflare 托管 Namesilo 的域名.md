# 域名

1. 访问 [Namesilo](https://www.namesilo.com/) 挑选好记、便宜的域名
 - 注册登陆之后访问 `Domain` 挑选域名，一般来说 `.top` 域名会比较便宜
 - 除了观察首单价之外，还要看一下续费的金额
2. 可以使用支付宝付款
3. 付款完成后进入到我的-域名设置，将默认的指向全部移除

# Cloudflare
1. 注册完成后点击添加站点，选择下方免费服务
  - 最大的优势是可以大大缩短域名解析到固定 ip 的速度
2. 回到 `Namesilo` 添加 `Cloudflare` 配置
  - 轮胎 - 删除原有的名称服务器，添加 `Cloudflare` 的名称服务器

# 购买服务器
1. 通过 [hosteons](https://my.hosteons.com/cart.php) 购买一台 VPS
 - 选择 `Debain10` 的系统

# 域名映射
1. 通过 `Cloudflare` 域名映射到对应机器
 - 并 `ping` 通

# SSH 到对应机器
1. 部署 `XUI`
```bash
apt update -y          # Debian/Ubuntu 命令
apt install -y curl socat    #Debian/Ubuntu 命令
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh) #X-ui面板安装
```

# 申请泛域名
> 匹配 *.your.doamin

1. 输入 `x-ui`

![image](https://user-images.githubusercontent.com/48549103/211484784-9342ab0e-5280-455d-955b-fea71b2cc23e.png)
按照提示完成域名添加

2. 在 `xui` 面板设置中配置 `/root/*csr & key`
 - 配置成功后即可通过 `https` 协议访问域名

# 使用 cdn 加速
![image](https://user-images.githubusercontent.com/48549103/211514538-f287aa14-7e90-46c6-a31e-0c0c12b5f966.png)

软件 `Qv2ray` 导入

