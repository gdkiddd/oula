<img width="703" alt="image" src="https://github.com/user-attachments/assets/68b35ff8-2062-4715-ab3f-f146fd72f452">## [怪盗] ALEO oula高性能锄头 ubuntu+hiveos部署教程

### 📺怪盗oula锄头视频教程： 
https://www.youtube.com/watch?v=K4PSg9bZ6i0

## 一、 注册 oula 账户

用以下链接注册, 领先30%+算力
https://pool.oula.com/signUp?referralCode=yhQbsd

注册账户后，https://pool.oula.com/user/miner 在后台绑定自己aleo钱包地址，需要两步验证。
<img src="https://github.com/gdkiddd/gdkiddd.github.io/blob/main/oula/001.png" width="800" alt="001"/>

这里可以快速生成自己的 aleo 钱包地址：https://aleo.tools/account

也可以用 https://www.leo.app

## 二、Ubuntu系统，快速启动锄头:
https://github.com/oula-miner/Aleo-miner/releases 直接下载aleo-pool-prover,

下载后，pool模式的启动方法：
```
chmod +x aleo-pool-prover
```
```
./aleo-pool-prover --account gdkiddd --pool wss://aleo.oula.com:3777 --worker-name Miner01
```
（这里gdkiddd换成你oula的账户名）

具体方法看这里：
https://github.com/oula-miner/Aleo-miner
  
  
## 三、HIVEOS飞行表部署:

文字教程：
1️⃣ 先到 https://the.hiveos.farm/wallets 添加钱包,输入aleo查找，pool模式的话，地址填入oula的账户名：
<img src="https://github.com/oula-miner/Aleo-miner/blob/master/HiveOS/101.png" width="800" alt="101"/>

添加飞行表，选ALEO和刚才创建的钱包， 挖K软件选custom，然后点旁边的“设定挖K软件配置”
<img src="https://github.com/oula-miner/Aleo-miner/blob/master/HiveOS/102.png"  width="800"  alt="102"/>

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
https://hiveon.com?ref=2743196891

然后下载 hiveos GPU镜像，用 etcher刻录到优盘
https://hiveon.com/zh/install/

开机后从优盘启动系统，启动后会自动运行飞行表，自动下载oula程序并启动， 过一会看到算力值就成功了。
<img src="https://github.com/gdkiddd/gdkiddd.github.io/blob/main/oula/002.png" width="800" alt="002"/>

注意： 如果启动后提示 github 程序下载失败， 可能是你没有翻墙，可在这里找到备用锄头链接， 去更新飞行表中的安装链接：

http://80.251.210.232/oula-miner/
