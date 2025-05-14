## 安装说明
<!-- by 邓凯 -->

### 系统要求
- Python 3.7 及以上版本
- 支持平台：Windows、macOS、Linux

### 安装步骤

1. **克隆项目仓库**  
   使用 Git 克隆代码到本地并进入项目目录：
   ```bash
   git clone https://github.com/yourname/douyin-downloader.git
   cd douyin-downloader

pip install -r requirements.txt

# 依赖冲突或权限问题

# 创建虚拟环境
python -m venv venv

# 激活虚拟环境
# macOS/Linux
source venv/bin/activate

# Windows
venv\Scripts\activate

# 再次安装依赖
pip install -r requirements.txt

# 问题二：安装缓慢或网络连接失败
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

# Git 克隆失败
git clone https://github.com.cnpmjs.org/yourname/douyin-downloader.git


<---- by 邓凯 ---->

# 配置文件准备

copy config.example.yml config.yml 

# Windows

# 方式一：使用配置文件（推荐）

python DouYinCommand.py

# 方式二：使用命令行参数（适合脚本调用）

python DouYinCommand.py -C True -l "https://v.douyin.com/xxxxxx/" -p "downloads/"