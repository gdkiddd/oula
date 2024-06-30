[怪盗] zklion hiveos部署教程


怪盗ALEO高性能锄头：

## 一、 注册 zklion 账户

用以下链接注册, 领先30%+算力
https://pool.zklion.com/signUp?referralCode=yhQbsd

注册账户后，https://pool.zklion.com/user/miner 在后台绑定自己aleo钱包地址，需要两步验证。


## 二、ubuntu下，快速启动锄头:
https://github.com/zklion-miner/Aleo-miner/releases 直接下载aleo-pool-prover,

下载后，pool模式的启动方法：
```
chmod +x aleo-pool-prover
./aleo-pool-prover --account gdkiddd --pool wss://aleo.zklion.com:3777 --worker-name myMiner
```
（这里gdkiddd换成你zklion的账户名）

具体方法看这里：
https://github.com/zklion-miner/Aleo-miner

 
## 三、HIVEOS锄头部署教程:

📺怪盗全视频解析： https://www.youtube.com/watch?v=K4PSg9bZ6i0

文字教程：
1️⃣ 先到 https://the.hiveos.farm/wallets 添加钱包,输入aleo查找，pool模式的话，地址填入zklion的账户名：
<img width="600" height="500" src="https://github.com/zklion-miner/Aleo-miner/blob/master/HiveOS/101.png" alt="101"/>

添加飞行表，选ALEO和刚才创建的钱包， 挖K软件选custom，然后点旁边的“设定挖K软件配置”
<img src="https://github.com/zklion-miner/Aleo-miner/blob/master/HiveOS/102.png" alt="102"/>

CUSTOM配置中，
名称：zklion-miner 

安装链接： github中的zklion_miner.tar.gz程序链接, 

钱包模板：%WAL%

矿地址：pool 模式: wss://aleo.zklion.com:3777 solo模式：wss://aleo.zklion.com:3666

密码：不填

其他配置参数：pool模式的话不填，solo模式的话填：solo

<img width="600" height="600" src="https://github.com/zklion-miner/Aleo-miner/blob/master/HiveOS/103.png" alt="103"/>
<img width="600" height="600" src="https://github.com/zklion-miner/Aleo-miner/blob/master/HiveOS/104.png" alt="104"/>

输入飞行表名称后， 创建飞行表后，就算成功了。
<img src="https://github.com/zklion-miner/Aleo-miner/blob/master/HiveOS/105.png" alt="105"/>


## 四、启动 hiveos飞行表
下载 hiveos GPU镜像，写入优盘，
https://hiveon.com/zh/install/
然后从优盘启动系统，启动后会自动运行飞行表，自动下载zklion程序并启动， 过一会看到算力值就成功了。
