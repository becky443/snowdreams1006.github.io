# nvm快速入门

> [Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm)

## 下载并配置

- 下载安装脚本并运行

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

- 刷新环境变量

```bash
source ~/.bash_profile
```

- 检测是否安装成功

```bash
command -v nvm
```

- 升级 nvm

```bash
(
  cd "$NVM_DIR"
  git fetch --tags origin
  git checkout `git describe --abbrev=0 --tags --match "v[0-9]*" $(git rev-list --tags --max-count=1)`
) && \. "$NVM_DIR/nvm.sh"
```

## 基本用法

- 下载最新版本

```bash
nvm install node
```

- 下载指定版本

```bash
nvm install 8
```

- 列出全部远程可用版本

``` bash
nvm ls-remote
```

> `nvm ls available`

- 使用最新版本

``` bash
nvm use node
```

- 使用指定版本

```bash
nvm use 8
```

- 列出已安装版本

```bash
nvm ls
```

## 参考资料

- [使用 nvm 管理不同版本的 node 与 npm](https://www.runoob.com/w3cnote/nvm-manager-node-versions.html)