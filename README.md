# hw3前端部分

[![Docker](https://github.com/ds-hw-fuuzen/hw3-frontend/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/ds-hw-fuuzen/hw3-frontend/actions/workflows/docker-publish.yml)

[使用 VSCode + docker 开发](https://github.com/ds-hw-fuuzen/.github/blob/main/profile/README.md)

为了实现前后端对接，请在 VSCode 创建开发容器之前确保先创建好这样一个 docker bridge：

```shell shell
docker network create hw3_bridge
```

您可以通过 `docker network ls` 检查 `hw3_bridge` 是否存在。

这个网桥 `hw3_bridge` 名称已经硬编码在 `.devcontainer/docker-compose.yml` 中。

当需要对接的时候，请打开两个 VSCode 窗口，分别在开发容器中打开项目目录，分别运行程序即可。

:warning 注意！本仓库镜像基于 Debian 9，目前已不被 VSCode 支持，VSCode 会弹出相应的警告，但目前不影响开发。
