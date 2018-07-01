#IOST 测试网络连接教程

1. golang 基础环境安装

2. 获取 iost 代码，请确定是 0.05 测试版

3. cd 到代码根目录 执行 `make build`

4. `./build/iwallet account` 会在 `~/.ssh` 目录下生成 `id_secp` 对应为私钥 , `id_secp.pub` 对为位公钥

5. 修改 `iserver/iserver.yml` 配置文件

   ```yaml
   account:
     id: {替换为步骤3生成的公钥}
     pub-key: {替换为步骤3生成的公钥}
     sec-key: {替换为步骤3生成的私钥}
   net:
     log-path: iostlog
     node-table-path: netpath
     node-id:
     register-addr: 18.179.83.17:30304
     listen-addr: {替换为自己服务器的公网IP}
     target: base
     port: 30301
     rpc-port: 30303
     metrics-port:
   log:
     level: debug
     path: /tmp/iost/logs/ {日志路径，随意配置}
   vm:
     max-block-gas:
   ldb:
     path: /tmp/iost/data/ {区块数据存放路径}
   redis:
     addr: 127.0.0.1
     port: 6379
   
   ```

   

6. 去https://explorer.iost.io/#/applyIOST 领取 iost， 填写 刚才生成的地址（也就是那个公钥）可以领 10个

7. 发起交易或者部署合约