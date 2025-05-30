# 术语表

<!-- by 王瀚龙 -->

## 专业术语

### 抖音API相关
- **aweme**: 抖音作品的基本单位，可以是视频、图集或直播
- **sec_uid**: 用户唯一标识符，用于API请求
- **X-Bogus**: 抖音API的加密参数，用于请求验证
- **ttwid**: 抖音API必需的cookie参数
- **odin_tt**: 用于用户喜欢列表API的验证参数

### 下载相关
- **play_addr**: 视频播放地址字段
- **bit_rate**: 视频码率信息，包含不同清晰度的下载链接
- **uri**: 资源唯一标识符，用于构建下载链接
- **flv_pull_url**: 直播流媒体拉流地址

### 作品类型
- **awemeType=0**: 视频作品
- **awemeType=1**: 图集作品
- **awemeType=2**: 直播内容

## AI 使用术语

### 数据处理
- **数据清洗(Data Cleaning)**: 去除无效或错误数据的过程
- **特征提取(Feature Extraction)**: 从原始数据中提取有用信息
- **数据增强(Data Augmentation)**: 通过变换增加数据多样性

### 模型相关
- **XGBoost**: 用于推荐系统的梯度提升算法
- **CNN**: 卷积神经网络，用于图像处理
- **RNN**: 循环神经网络，用于序列数据处理

### 评估指标
- **准确率(Accuracy)**: 模型预测正确的比例
- **召回率(Recall)**: 正样本被正确识别的比例
- **F1分数(F1 Score)**: 精确率和召回率的调和平均

### API (Application Programming Interface)
- **定义**：应用程序编程接口，是一组规则和定义，允许不同的软件程序之间进行交互。
- **详细解释**：API定义了软件组件之间如何相互协作，包括数据的请求和响应格式。
- **示例**：在Web开发中，一个网站可以通过API从第三方服务获取数据，如天气信息或用户数据。

### Bug
- **定义**：软件中的错误或缺陷，导致程序无法正常运行或产生意外结果。
- **详细解释**：Bug可能由代码错误、逻辑问题或外部环境因素引起。
- **示例**：一个常见的Bug是在用户输入非法数据时，程序没有正确处理而导致崩溃。

### CI/CD (Continuous Integration / Continuous Deployment)
- **定义**：持续集成和持续部署，是一种软件开发实践，用于自动化软件的构建、测试和部署过程。
- **详细解释**：CI/CD通过自动化工具和流程，确保代码的持续集成和快速部署，提高开发效率和软件质量。
- **示例**：使用Jenkins等工具可以实现代码的自动构建和部署，每次代码提交后都会自动运行测试并部署到生产环境。

### Database (数据库)
- **定义**：用于存储和管理数据的系统。
- **详细解释**：数据库可以是关系型数据库（如MySQL、PostgreSQL）或非关系型数据库（如MongoDB、Redis）。
- **示例**：一个电商网站的用户信息和订单数据通常存储在数据库中，方便快速查询和更新。

### Endpoint
- **定义**：在API中，用于接收请求并返回响应的特定URL路径。
- **详细解释**：Endpoint定义了API的入口点，客户端通过Endpoint与服务器进行交互。
- **示例**：`/api/users`是一个用户信息的Endpoint，客户端可以通过这个路径获取或更新用户数据。

- **抖音平台（TikTok Platform）**：指由字节跳动公司开发的短视频社交平台，用户可以在平台上创作、分享和观看各种短视频内容。
- **视频链接（Video Link）**：用于标识抖音平台上特定视频的唯一网址，通过该链接可以直接访问对应的视频页面。
- **下载地址（Download URL）**：经过处理后，能够直接用于下载抖音视频的链接，与原始视频链接不同，它指向视频文件的实际存储位置。
- **解析（Parsing）**：在抖音下载器中，指对抖音视频链接进行分析和处理的过程，目的是获取视频的下载地址及其他相关信息。
- **水印（Watermark）**：通常是为了标识视频的来源和版权，在视频上添加的文字、图案或其他标识。抖音视频可能会带有抖音平台的水印。
- **无水印下载（Watermark-Free Download）**：指下载的抖音视频不包含抖音平台的水印，使视频看起来更加整洁。
- **缓存（Cache）**：下载器在运行过程中，为了提高效率，可能会将一些数据（如视频信息、解析结果等）临时存储在本地设备上，这些临时存储的数据称为缓存。
- **并发下载（Concurrent Download）**：指同时进行多个视频下载任务，可以提高下载效率，但可能会对网络带宽和服务器性能产生一定影响。
- **用户代理（User-Agent）**：在 HTTP 请求中，用于标识客户端（如浏览器或下载器）的软件信息。抖音下载器在请求视频数据时，需要设置合适的用户代理，以模拟正常的浏览器访问行为。