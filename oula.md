
## [怪盗] ALEO oula高性能锄头 ubuntu+hiveos部署教程

### 📺怪盗oula锄头视频教程（旧版，现已升级为oula品牌，但方法大同小异）： 
[https://www.youtube.com/watch?v=K4PSg9bZ6i0](https://www.youtube.com/watch?v=K4PSg9bZ6i0)

## 一、 注册 oula 账户

用以下内部邀请链接注册, 领先30%+算力：
[https://oula.network/zh/register?invitation=SDDV6L](https://oula.network/zh/register?invitation=SDDV6L)

注册账户后， 在后台绑定自己aleo钱包地址，需要两步验证。（为了之后提现用，测试可跳过）

这里可以快速生成自己的 aleo 钱包地址：[https://aleo.tools/account](https://aleo.tools/account)

也可以用LEO wallet： [https://www.leo.app](https://www.leo.app)

## 二、Ubuntu系统，快速启动锄头:
需要ubuntu22以上， cuda12.3以上的环境
可用以下代码查看：
```nvidia-smi```
下载锄头：
[http://23.106.143.181/oula/oula_miner-v0.1.0.tar.gz](http://23.106.143.181/oula/oula_miner-v0.1.0.tar.gz)

下载后，授权：
```
chmod +x oula-pool-prover
```
启动锄头
```
./oula-pool-prover --pool wss://aleo.oula.network:6666 --account gdkiddd --worker-name worker01
```
（这里gdkiddd可换成你oula的账户名）

具体方法看这里：
https://github.com/oula-miner/Aleo-miner
  
  
## 三、HIVEOS飞行表部署:

文字教程：
1️⃣ 先到 https://the.hiveos.farm/wallets 添加钱包,输入aleo查找，pool模式的话，地址填入oula的账户名：
<img width="703" alt="image" src="https://github.com/user-attachments/assets/68b35ff8-2062-4715-ab3f-f146fd72f452">

添加飞行表，现复制下面代码，然后点击【添加自剪切板】
飞行表一键配置：
```
{"name":"oula_miner","isFavorite":true,"items":[{"coin":"ALEO","pool_ssl":false,"wal_id":10333513,"dpool_ssl":false,"miner":"custom","miner_alt":"oula_miner","miner_config":{"url":"wss://aleo.oula.network:6666","algo":"aleo","miner":"oula_miner","template":"%WAL%","install_url":"http://23.106.143.181/oula/oula_miner-v0.1.0.tar.gz"},"pool_geo":[]}]}
```
其他配置参数：solo模式的话填solo，pool不填

<img src="https://github.com/oula-miner/Aleo-miner/blob/master/HiveOS/103.png" width="800" alt="103"/>
<img src="https://github.com/oula-miner/Aleo-miner/blob/master/HiveOS/104.png" width="800" alt="104"/>

输入飞行表名称后， 创建飞行表后，就算成功了。
<img src="https://github.com/oula-miner/Aleo-miner/blob/master/HiveOS/105.png" width="800" alt="105"/>

  
## 四、启动 hiveos飞行表
第一次用 HIVEOS 的， 用这个优惠链接注册账户：
[https://hiveon.com?ref=2743196891](https://hiveon.com?ref=2743196891)

然后下载 hiveos GPU镜像，用 etcher刻录到优盘
[https://hiveon.com/zh/install/](https://hiveon.com/zh/install/)

运行前先升级hiveos显卡驱动
```
nvidia-driver-update
```
开机后从优盘启动系统，启动后会自动运行飞行表，自动下载oula程序并启动， 过一会看到算力值就成功了。
<img src="https://github.com/gdkiddd/gdkiddd.github.io/blob/main/oula/002.png" width="800" alt="002"/>
如果启动后提示 github 程序下载失败， 可能是你没有翻墙。

