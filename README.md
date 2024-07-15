# gh-proxy

### 简介

github release、archive以及项目文件的加速项目，支持clone，有Cloudflare Workers无服务器版本以及Python版本

### 使用

直接在copy出来的url前加部署域名即可

也可以直接访问，在input输入

访问私有仓库可以通过

`git clone https://user:TOKEN@ghproxy.com/https://github.com/xxxx/xxxx` 

以下都是合法输入：

- 分支源码：https://github.com/github/spec-kit/archive/main.zip

- release源码：https://github.com/github/spec-kit/archive/refs/tags/v0.0.79.zip

- release文件：https://github.com/github/spec-kit/releases/download/v0.0.79/spec-kit-template-amp-ps-v0.0.79.zip

- 分支文件：https://github.com/github/spec-kit/blob/main/README.md

- commit文件：https://github.com/github/spec-kit/blob/598148ca67bce30095e0a3bd3d1791ef4235929e/README.md

- api接口：https://api.github.com/repos/github/spec-kit

- gist：https://gist.githubusercontent.com/aamiaa/204cd9d42013ded9faf646fae7f89fbb/raw/4912415839790240d49c1d2553e940f0c65f95d5/CompleteDiscordQuest.md

### 用 Docker 部署 Python 版本

```
docker run -d --name="gh-proxy-py" \
  -p 0.0.0.0:80:80 \
  --restart=always \
  zzcgwu/gh-proxy:latest
```

第一个80是你要暴露出去的端口

