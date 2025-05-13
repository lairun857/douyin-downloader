## 负责README.md中的"How to Use"部分
<!-- by 秦登基 -->
Installation
Before you start using DouYin Downloader, ensure you have Python installed on your system. You can install the required dependencies using pip:
pip install -r requirements.txt

Command Line Usage
DouYin Downloader supports both command line parameters and YAML configuration files for flexible operation.

Basic Command Line Example
python douyin_downloader.py --url <douyin_link> --output <output_folder>

--url: The URL of the Douyin content you want to download (e.g., video, playlist, user profile).
--output: The directory where the downloaded files will be saved.

Advanced Options
| Parameter         | Description                                                                  |
| ----------------- | ---------------------------------------------------------------------------- |
| `--threads`       | Number of concurrent download threads (default: 5)                           |
| `--limit`         | Limit the number of items to download (default: no limit)                    |
| `--skip-existing` | Skip files that already exist in the output directory                        |
| `--no-watermark`  | Download content without watermarks (if supported)                           |
| `--time-range`    | Filter downloads by time range (format: `start_date:end_date` in YYYY-MM-DD) |

Example with advanced options:
python douyin_downloader.py --url https://douyin.com/example --output downloads --threads 10 --limit 20 --skip-existing --no-watermark --time-range 2023-01-01:2023-06-30

YAML Configuration File Usage
You can also use a YAML configuration file for more complex setups. Create a config.yaml file with the following structure:
url: "https://douyin.com/example"
output: "downloads"
threads: 10
limit: 20
skip_existing: true
no_watermark: true
time_range:
  start: "2023-01-01"
  end: "2023-06-30"

Run the downloader with the configuration file:
python douyin_downloader.py --config config.yaml

Incremental Updates
For user profiles or playlists, DouYin Downloader supports incremental updates. It will only download new content since the last run. To enable this feature, use the --incremental flag or set incremental: true in the YAML configuration.
Example:
python douyin_downloader.py --url https://douyin.com/user_profile --output downloads --incremental