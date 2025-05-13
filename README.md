<<<<<<< HEAD
# Project Title: Douyin Downloader

### Description
Douyin Downloader is a tool that allows you to download a variety of content from Douyin, including videos, music, live stream information, and albums. It supports downloading personal homepages, works, live streams, collections, and music collections. The downloader also supports watermark removal and batch downloads, making it a powerful tool for Douyin content retrieval.

Key Features:
- **Multiple content support**: Download videos, images, music, live streams, and more.
- **Support for various types of links**: Personal homepages, work collections, live streams, and music collections.
- **Watermark removal**: Download content without watermarks.
- **Batch downloading**: Download multiple links simultaneously using multi-threaded parallel downloading.
- **Flexible configuration**: Support for command-line parameters and configuration files.
- **Incremental updates**: Download new content from homepages with filtering by time range.
- **Data persistence**: Store data in a database for future updates.

---

### Table of Contents
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

### Installation

#### Prerequisites
Ensure that you have Python 3.x installed on your system. You will also need to have `pip` installed for managing dependencies.

#### Steps to Install
1. Clone the repository to your local machine:
git clone https://github.com/yourusername/douyin-downloader.git


2. Navigate to the project directory:
cd douyin-downloader


3. Install the Python dependencies:
pip install -r requirements.txt


编辑

4. Copy the example configuration file:
cp config.example.yml config.yml



### Configuration

1. **Edit the `config.yml` file** to set up the following:
- **Download links**: The links to the Douyin content you wish to download.
- **Download path**: The local directory where content will be saved.
- **Cookie information**: Retrieve this from the browser's developer tools (necessary for accessing content behind authentication).
- **Other download options**: Customize the download behavior such as file types, download limits, and more.


### Usage

#### Option 1: Using the configuration file (Recommended)
Simply run the Python script with the following command:
python DouYinCommand.py


This method will use the settings defined in the `config.yml` file.

#### Option 2: Using command-line arguments
You can also specify download options directly from the command line:
python DouYinCommand.py -C True -l "Douyin Share Link" -p "Download Path"


- `-C True` enables watermark removal.
- `-l` specifies the Douyin share link you want to download.
- `-p` specifies the download path.


### Screenshots

Include some relevant screenshots of the tool in action, if applicable.



Description of what is shown in the screenshot


### Contributing

We welcome contributions to improve the project! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.


### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


### Additional Notes
- Make sure to provide your own Douyin cookie information to ensure the downloader works properly with content that may require authentication.
- This project is designed to be used for personal use only, respecting the terms and conditions of the content provider.
=======
# DouYin Downloader

<a href="https://trendshift.io/repositories/13156" target="_blank"><img src="https://trendshift.io/api/badge/repositories/13156" alt="jiji262%2Fdouyin-downloader | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

DouYin Downloader 是一个用于批量下载抖音内容的工具。基于抖音 API 实现，支持命令行参数或 YAML 配置文件方式运行，可满足大部分抖音内容的下载需求。

## ✨ 特性

- **多种内容支持**
  - 视频、图集、音乐、直播信息下载
  - 支持个人主页、作品分享、直播、合集、音乐集合等多种链接
  - 支持去水印下载
  
- **批量下载能力**
  - 多线程并发下载
  - 支持多链接批量下载
  - 自动跳过已下载内容
  
- **灵活配置**
  - 支持命令行参数和配置文件两种方式
  - 可自定义下载路径、线程数等
  - 支持下载数量限制
  
- **增量更新**
  - 支持主页作品增量更新
  - 支持数据持久化到数据库
  - 可根据时间范围过滤

## 🚀 快速开始

### 安装

1. 安装 Python 依赖：
```bash
pip install -r requirements.txt
```

2. 复制配置文件：
```bash
cp config.example.yml config.yml
```

### 配置

编辑 `config.yml` 文件，设置：
- 下载链接
- 保存路径
- Cookie 信息（从浏览器开发者工具获取）
- 其他下载选项

### 运行

**方式一：使用配置文件（推荐）**
```bash
python DouYinCommand.py
```

**方式二：使用命令行**
```bash
python DouYinCommand.py -C True -l "抖音分享链接" -p "下载路径"
```

## 使用交流群

![fuye](img/fuye.png)

## 使用截图

![DouYinCommand1](img/DouYinCommand1.png)
![DouYinCommand2](img/DouYinCommand2.png)
![DouYinCommand download](img/DouYinCommanddownload.jpg)
![DouYinCommand download detail](img/DouYinCommanddownloaddetail.jpg)

## 📝 支持的链接类型

- 作品分享链接：`https://v.douyin.com/xxx/`
- 个人主页：`https://www.douyin.com/user/xxx`
- 单个视频：`https://www.douyin.com/video/xxx`
- 图集：`https://www.douyin.com/note/xxx`
- 合集：`https://www.douyin.com/collection/xxx`
- 音乐原声：`https://www.douyin.com/music/xxx`
- 直播：`https://live.douyin.com/xxx`

## 🛠️ 高级用法

### 命令行参数

基础参数：
```
-C, --cmd            使用命令行模式
-l, --link          下载链接
-p, --path          保存路径
-t, --thread        线程数（默认5）
```

下载选项：
```
-m, --music         下载音乐（默认True）
-c, --cover         下载封面（默认True）
-a, --avatar        下载头像（默认True）
-j, --json          保存JSON数据（默认True）
```

更多参数说明请使用 `-h` 查看帮助信息。

### 示例命令

1. 下载单个视频：
```bash
python DouYinCommand.py -C True -l "https://v.douyin.com/xxx/"
```

2. 下载主页作品：
```bash
python DouYinCommand.py -C True -l "https://v.douyin.com/xxx/" -M post
```

3. 批量下载：
```bash
python DouYinCommand.py -C True -l "链接1" -l "链接2" -p "./downloads"
```

更多示例请参考[使用示例文档](docs/examples.md)。

## 📋 注意事项

1. 本项目仅供学习交流使用
2. 使用前请确保已安装所需依赖
3. Cookie 信息需要自行获取
4. 建议适当调整线程数，避免请求过于频繁

## 🤝 贡献

欢迎提交 Issue 和 Pull Request。

## 📜 许可证

本项目采用 [MIT](LICENSE) 许可证。

## 🙏 鸣谢

- [TikTokDownload](https://github.com/Johnserf-Seed/TikTokDownload)
- 本项目使用了 ChatGPT 辅助开发，如有问题请提 Issue

## 📊 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=jiji262/douyin-downloader&type=Date)](https://star-history.com/#jiji262/douyin-downloader&Date)




# License

[MIT](https://opensource.org/licenses/MIT) 

>>>>>>> 65556cb0ede369ddb110d03f6bbc2cd41e7cecf6
