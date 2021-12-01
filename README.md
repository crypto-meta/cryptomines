# @cryptox/mines

[Crypto Meta](https://github.com/crypto-meta) 团队为 [cryptomines](https://play.cryptomines.app/) 倾心打造的安全、稳定、高效的自动化脚本。

## 特性

1. 批量买工人盲盒
2. 一键开所有工人盲盒
3. 一键销毁所有算力小于等于 60 的工人（算力可自定义）
4. 批量买飞船盲盒
5. 一键开所有飞船盲盒
6. 一键销毁所有星级小于等于 2 的飞船（星级可自定义）
7. 无人值守：买盲盒、开盲盒、销毁低算力工人或低星级飞船自动一键自动完成
8. 账号多开：轻松管理多个账号，账号再多也不会乱了

## 安装

```sh
npm install -g @cryptox/mines
```

## 命令

### 打印版本

```sh
mines -V
```

### 帮助信息

```sh
mines -h
```

### 账号相关

- 登录：`mines login`
- 登出：`mines logout`
- 查看账号信息：`mines whoami`

### 工人（worker）相关

- 买工人：`mines worker buy`
  - 带参数使用：`mines worker buy --openGas=4000001 --openGasPrice=6200000001 --burnGasPrice=6000000001 --power=60 --only=false`
- 开工人盲盒：`mines worker open`
  - 带参数使用：`mines worker open --openGas=4000001 --openGasPrice=6200000001 --burnGasPrice=6000000001 --power=60 --only=false`
- 销毁工人：`mines worker burn`
  - 带参数使用：`mines worker burn --burnGasPrice=6000000001 --power=60`
- 工人统计：`mines worker list`

> 注意：参数什么意思都可以带上 `-h` 查看

> 注意：`--only` 参数默认为 `false`，设为 `true` 则只执行单步任务

### 飞船（spaceship）相关

- 买飞船：`mines ship buy`
  - 带参数使用：`mines ship buy --openGas=4000001 --openGasPrice=6200000001 --burnGasPrice=6000000001 --star=2 --only=false`
- 开飞船盲盒：`mines ship open`
  - 带参数使用：`mines ship open --openGas=4000001 --openGasPrice=6200000001 --burnGasPrice=6000000001 --star=2 --only=false`
- 销毁飞船：`mines ship burn`
  - 带参数使用：`mines ship burn --burnGasPrice=6000000001 --star=2`
- 飞船统计：`mines ship list`

> 注意：`--only` 参数默认为 `false`，设为 `true` 则只执行单步任务，比如只执行购买，不自动执行后续拆和销毁的任务

## 兼容性

脚本同时兼容 Windows、macOS 和 Linux 操作系统，满足多种场景使用。比如放在服务器上跑定时任务。
