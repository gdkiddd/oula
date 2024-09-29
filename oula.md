
## 一、 注册oula账户

点击以下链接注册 (收不到验证码, 可能在垃圾邮箱中)

[https://oula.network/zh/register?invitation=SDDV6L](https://oula.network/zh/register?invitation=SDDV6L)

大算力客户请私信怪盗V: gdkiddd, 进VIP服务群:

登录后台-子账户管理-添加一个子账户名,这个就是挖矿账户
![image](https://github.com/user-attachments/assets/5f1779c8-a7e3-4c8a-bae3-5f41ba87578d)

提现方式:
登录后台-付款设置-绑定自己aleo钱包地址，要先开通谷歌验证。

快速生成自己的 aleo 钱包地址：[https://www.provable.tools/account](https://www.provable.tools/account)

或者fox wallet： [https://foxwallet.com/download](https://foxwallet.com/download)

或LEO wallet： [https://www.leo.app](https://www.leo.app)

## 二、Ubuntu系统:
### 检查环境
（重要！ 需要ubuntu22.04及以上）
输⼊```hostnamectl```查看ubuntu版本号：

![image](https://github.com/user-attachments/assets/5ad08c15-3844-4fd7-b46c-35db1c332929)

验证显卡驱动，如果版本不是550以上，那就先卸载，再安装新驱动：
```
nvidia-smi
```

### 卸载现有N卡驱动
```
nvidia-uninstall -s -q
apt --purge remove nvidia*
apt autoremove
reboot
```

### NVIDIA新驱动安装
1、下载
```
wget https://us.download.nvidia.com/XFree86/Linux-x86_64/550.107.02/NVIDIA-Linux-x86_64-550.107.02.run
```

2、添加可执行权限
```
chmod +x NVIDIA-Linux-x86_64-550.107.02.run
```

3、执行安装
```
./NVIDIA-Linux-x86_64-550.107.02.run -s --dkms --no-opengl-files
```

### 下载锄头
最新版本：[https://github.com/oula-network/aleo/releases](https://github.com/oula-network/aleo/releases)
以下为举例,实际请更换为上面最新版本链接:
```
wget https://github.com/oula-network/aleo/releases/download/v1.12/oula-pool-prover
```
启动锄头：
```
chmod +x oula-pool-prover
./oula-pool-prover --pool wss://aleo.oula.network:6666 --account kidcdf --worker-name worker01
```
（以上kidcdf为测试账号， 可换成你oula注册的子账户名）
![image](https://github.com/user-attachments/assets/9d1aeb8b-0421-429e-be4f-cf4f70e73f66)

启动后,等待⼏分钟后，可在Oula后台查看到算⼒情况.

更多方法：
[https://oula-faq.gitbook.io/zh/kai-shi-wa-kuang/publish-your-docs](https://oula-faq.gitbook.io/zh/kai-shi-wa-kuang/publish-your-docs)

**********************************************************************************************************************************

## 三、HIVEOS部署流程:
第一次用 HIVEOS的，看这里安装镜像和启动系统:

[https://github.com/gdkiddd/oula/blob/main/hiveos_first.md](https://github.com/gdkiddd/oula/blob/main/hiveos_first.md)

环境要求：hiveos-0.6-227-stable（必须Ubuntu 20.04及以上！）

### 1️⃣ 检查hiveos版本是否是基于Ubuntu 20.04:
```
hostnamectl
```

如果ubuntu版本正确,则升级显卡驱动，必须先升级到550版本的显卡！
```
nvidia-driver-update
```
执行后会下载驱动，自动安装升级，需要一会，这里如果不成功卡住，重启后尝试多执行几次。


### 2️⃣ 添加钱包
[https://the.hiveos.farm/wallets](https://the.hiveos.farm/wallets) ，输入aleo查找：

钱包地址：填你oula的挖矿子账户名

<img width="594" alt="image" src="https://github.com/user-attachments/assets/23f579e7-8e91-48d6-a30d-5f3bc34b3cd1">


### 3️⃣ 添加飞行表：

一键配置代码,复制：
```
{"name":"oulapool",
"isFavorite":true,
"items":[{"coin":"ALEO","pool_ssl":false,"wal_id":10333513,"dpool_ssl":false,
"miner":"custom",
"miner_alt":"oulapool",
"miner_config":{"url":"wss://aleo.oula.network:6666",
"algo":"aleo",
"miner":"oulapool",
"template":"%WAL%.%WORKER_NAME%",
"install_url":"http://45.78.60.184/oula/oulapool-v1.12.tar.gz"},
"pool_geo":[]}]}
```
点击hiveos-飞行表-添加自【剪切板】，完成一键配置：

![image](https://github.com/user-attachments/assets/7cc98dfb-3236-4172-9dfc-2718713dda63)
输入飞行表名称， 创建飞行表后，就算成功了。


### 4️⃣ 启动 hiveos飞行表

开机后从优盘启动系统，启动后会自动运行飞行表，自动下载oula程序并启动，

启动后过10分钟左右， 等算力稳定，以下为启动运行成功后显示算力的画面：

![IMG_6201](https://github.com/user-attachments/assets/378c81ec-5bf4-4a41-87cc-fbf73f8fe0ed)

算力会根据主网高度不同而波动，差异较大，要跑数小时可能才能获得峰值算力，可在oula后台查看。

## Q&A答疑:
1. 支持N卡和A100,H100， 暂不支持A卡。

2. 只支持ubuntu和hiveos，不支持windows和wsl。

3. 尽量避免不同型号GPU混插，以免出错。

4. 机器最低配置：CPU4核，8G内存，否则可能无算力。
   
5. 📺怪盗oula锄头视频教程（旧版的，新版本即将推出！）：
   
[https://www.youtube.com/watch?v=K4PSg9bZ6i0](https://www.youtube.com/watch?v=K4PSg9bZ6i0)

6.其他资讯： 
Aleo资讯: [https://fil8.top](https://fil8.top), 或关注公众号:怪盗KIDDD, 回复: aleo

咨询怪盗:  [https://t.me/gdkiddd](https://t.me/gdkiddd)

AleoAsic: [https://aleoasic.com](https://aleoasic.com)
