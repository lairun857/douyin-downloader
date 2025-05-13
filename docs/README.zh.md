# DouYin 下载器

## 项目介绍
<!-- by 梁志灿 -->

## 安装说明
<!-- by 邓凯 -->

## 使用指南
### 功能一
<!-- by 甘润 -->


### 功能二
<!-- by 郭海生 -->

## 使用方法
<!-- by 秦登基 -->
## 负责README.zh.md中的"使用方法"部分
安装
在使用 DouYin Downloader 之前，请确保您的系统已安装 Python。您可以通过以下命令安装所需的依赖项：

命令行使用
DouYin Downloader 支持命令行参数和 YAML 配置文件两种方式运行。
基本命令行示例
python douyin_downloader.py --url <抖音链接> --output <输出文件夹>
--url: 您要下载的抖音内容的链接（例如视频、合集、用户主页）。
--output: 下载文件保存的目录。

高级选项
| 参数               | 描述                                                      |
| ----------------- | ----------------------------------------------------------|
| `--threads`       | 并发下载线程数（默认值：5）                                             |
| `--limit`         | 限制下载数量（默认值：无限制）                                          |
| `--skip-existing` | 跳过输出目录中已存在的文件                                              |
| `--no-watermark`  | 下载无水印内容（如果支持）                                              |
| `--time-range`    | 按时间范围过滤下载内容（格式：`开始日期:结束日期`，日期格式为 YYYY-MM-DD） |

高级选项示例：
python douyin_downloader.py --url https://douyin.com/example --output downloads --threads 10 --limit 20 --skip-existing --no-watermark --time-range 2023-01-01:2023-06-30

YAML 配置文件使用
您也可以通过 YAML 配置文件进行更复杂的设置。创建一个 config.yaml 文件，内容如下：
url: "https://douyin.com/example"
output: "downloads"
threads: 10
limit: 20
skip_existing: true
no_watermark: true
time_range:
  start: "2023-01-01"
  end: "2023-06-30"

  使用配置文件运行下载器：
  python douyin_downloader.py --config config.yaml

  增量更新
对于用户主页或合集，DouYin Downloader 支持增量更新功能。它只会下载自上次运行以来的新内容。要启用此功能，请在命令行中使用 --incremental 参数，或在 YAML 配置文件中设置 incremental: true。
示例：
python douyin_downloader.py --url https://douyin.com/user_profile --output downloads --incremental
## 贡献指南
<!-- by 冯浩 -->

[MIT 许可证](https://opensource.org/licenses/MIT)