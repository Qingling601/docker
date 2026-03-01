🚀 Ubuntu 系统 Docker 极简安装指南

🛠️ 独家提供：闲鱼店铺【qingling】
💡 适用系统：Ubuntu 18.04 / 20.04 / 22.04 / 24.04

亲爱的开发者，您好！感谢支持**【qingling】**店铺。
要运行咱们的 ROS 专属环境，您的物理机只需具备一个基础软件：Docker。
为了帮您避开国内网络下载慢、经常报错的坑，本教程为您提供了国内专线一键安装方案，只需 3 分钟即可配置完毕！
🟢 第一步：一键安装 Docker 与 Compose 插件

打开您 Ubuntu 电脑的终端（快捷键：Ctrl + Alt + T），复制并执行以下两条命令。
这会自动从阿里云的国内服务器为您下载并安装最新版的 Docker 引擎：
Bash

# 1. 下载官方自动化安装脚本
curl -fsSL https://get.docker.com -o get-docker.sh

# 2. 运行脚本，并指定使用 Aliyun 国内镜像源加速
sudo sh get-docker.sh --mirror Aliyun

(注意：执行第二步时需要输入您电脑的开机密码，输入时屏幕不会显示字符，输完直接回车即可。安装过程大约需要 1~2 分钟，请耐心等待直到重新出现输入提示符。)
🟢 第二步：配置免 sudo 权限（⭐ 极其重要）

默认情况下，每次运行 Docker 命令都需要加 sudo，这不仅麻烦，还会导致我们后续挂载代码时出现权限冲突。
请依次在终端执行以下命令，将当前用户加入 Docker 最高权限组：
Bash

# 1. 创建 docker 用户组（如果已存在会提示已存在，不影响）
sudo groupadd docker

# 2. 将当前登录的用户加入 docker 组
sudo usermod -aG docker $USER

# 3. 刷新权限，使其立刻生效
newgrp docker

🟢 第三步：验证安装是否成功

让我们来测试一下 Docker 是否已经完美运行！在终端中直接输入以下命令（注意不要加 sudo）：
Bash

docker compose version

🎉 成功标志：
如果您能看到类似 Docker Compose version v2.x.x 的输出，说明大功告成！

接下来，您就可以直接打开我发给您的**《ROS Noetic 专属开发环境使用手册》**，开始导入 noetic_docker_v1.0.tar 镜像，享受【qingling】为您打造的丝滑 ROS 体验了！

👨‍💻 技术支持：
如果在安装过程中遇到任何系统底层报错，请随时截图并联系闲鱼店铺【qingling】，我们将为您提供技术指导。祝您科研与开发顺利！
