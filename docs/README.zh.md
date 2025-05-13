
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

注意事项
• 检查链接有效性：确保提供的抖音链接是有效的，并且内容是公开可访问的。如果链接无效或内容不可访问，工具可能无法正常工作。
• 网络问题：由于网络原因，某些链接可能无法成功解析。如果遇到问题，请检查链接的合法性，并确保网络连接正常。建议适当重试。
• Cookie 获取：某些功能可能需要有效的 Cookie 信息。请参考 获取 Cookie 的方法。
• 文件夹权限：确保输出目录具有写入权限。如果权限不足，工具可能无法保存下载的文件。
获取 Cookie 的方法
1. 打开抖音网页版（如 抖音）。
2. 按下 F12 键打开开发者工具。
3. 切换到“网络”（Network）标签页。
4. 刷新页面，然后在请求列表中找到一个请求。
5. 在请求的“请求头”（Request Headers）中找到 cookie 字段，复制其值。
设置文件夹权限
1. 在 Windows 系统中，右键点击文件夹，选择“属性”。
2. 切换到“安全”标签页。
3. 确保当前用户具有“写入”权限。

[MIT 许可证](https://opensource.org/licenses/MIT)