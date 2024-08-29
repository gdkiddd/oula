
## [怪盗] ALEO oula高性能锄头 ubuntu+hiveos部署教程v1.8

### 📺怪盗oula锄头视频教程（旧版，现已升级为oula品牌，但方法大同小异）： 
[https://www.youtube.com/watch?v=K4PSg9bZ6i0](https://www.youtube.com/watch?v=K4PSg9bZ6i0)


## 一、 注册 oula 账户

点击以下怪盗邀请链接注册 (收不到验证码的话, 可能在垃圾邮箱中)：
[https://oula.network/zh/register?invitation=SDDV6L](https://oula.network/zh/register?invitation=SDDV6L)

登录后台-子账户管理-添加一个子账户名,这个就是挖矿账户,之后会用到.

提现:（仅测试锄头的话可跳过）
登录后台-付款设置-绑定自己aleo钱包地址，要先开通谷歌验证。
快速生成自己的 aleo 钱包地址：[https://www.provable.tools/account](https://www.provable.tools/account)
也可以用LEO wallet(网页版和手机都有)： [https://www.leo.app](https://www.leo.app)



## 二、Ubuntu系统，快速启动锄头:
需要ubuntu22以上， cuda12.3以上的环境
可用以下代码查看：
```nvidia-smi```

下载锄头：
最新版本详见： [https://github.com/oula-network/aleo/releases](https://github.com/oula-network/aleo/releases)
以下为v1.8为例：
```
wget https://github.com/oula-network/aleo/releases/download/v1.8/oula-pool-prover
```
下载后，授权：
```
chmod +x oula-pool-prover
```
启动锄头
```
./oula-pool-prover --pool wss://aleo.oula.network:6666 --account kidcdf --worker-name worker01
```
（以上为测试账号， --account后的名字，换成你oula注册的子账户名）

具体方法看这里：
[https://oula-faq.gitbook.io/zh/kai-shi-wa-kuang/publish-your-docs](https://oula-faq.gitbook.io/zh/kai-shi-wa-kuang/publish-your-docs)




## 三、HIVEOS飞行表部署:
环境要求：hiveos-0.6-227-stable（Ubuntu 20.04）

1️⃣ 首先检查hiveos版本是否是基于Ubuntu 20.04、执行如下命令
```hostnamectl```

如果ubuntu版本正确,则升级显卡驱动(必须!)
```
nvidia-driver-update
```

2️⃣ 添加钱包:  [https://the.hiveos.farm/wallets](https://the.hiveos.farm/wallets) ，输入aleo查找：
<img width="598" alt="image" src="https://github.com/user-attachments/assets/de7f1a51-fb24-40fa-9447-8b030636a4be">

3️⃣ 添加飞行表：
复制下面代码，然后点击hiveos-飞行表-【添加自剪切板】，完成一键配置：
```
{"name":"oula_miner","isFavorite":true,"items":[{"coin":"ALEO","pool_ssl":false,"wal_id":10333513,"dpool_ssl":false,"miner":"custom","miner_alt":"oula_miner","miner_config":{"url":"wss://aleo.oula.network:6666","algo":"aleo","miner":"oula_miner","template":"%WAL%","install_url":"http://23.106.143.181/oula/oula_miner-v0.3.0.tar.gz"},"pool_geo":[]}]}
```
锄头下载链接为: [http://23.106.143.181/oula/oula_miner-v0.3.0.tar.gz](http://23.106.143.181/oula/oula_miner-v0.3.0.tar.gz)

输入飞行表名称后， 创建飞行表后，就算成功了。
<img width="1217" alt="image" src="https://github.com/user-attachments/assets/21144864-a31a-45dd-9b7d-fa77e945e3b5">




## 四、启动 hiveos飞行表
第一次用 HIVEOS 的， 用这个优惠链接注册账户：
[https://hiveon.com?ref=2743196891](https://hiveon.com?ref=2743196891)

然后下载 hiveos GPU镜像，用 etcher刻录到优盘
[https://hiveon.com/zh/install/](https://hiveon.com/zh/install/)

运行前先升级hiveos显卡驱动
```
nvidia-driver-update
```
开机后从优盘启动系统，启动后会自动运行飞行表，自动下载oula程序并启动，
如果启动后提示 github 程序下载失败， 可能是你没有翻墙。

启动后过10分钟左右， 等算力稳定，以下为启动运行成功后，显示算力的画面：
![telegram-cloud-photo-size-5-6194924926851466377-y](https://github.com/user-attachments/assets/758270a2-11d5-47b1-90d9-edddc5a0dc04)


