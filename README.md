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

Additional Tips
Check Link Validity: Ensure that the Douyin links you provide are valid and publicly accessible.
Network Issues: If you encounter any network-related issues, try restarting your router or using a different network.
Cookie Information: Some features may require a valid cookie. Please refer to the Cookie Acquisition Method for details.
Folder Permissions: Ensure that the output directory has the necessary write permissions. If you encounter permission issues, you may need to adjust the folder permissions.
Cookie Acquisition Method
Open the Douyin web page (e.g., Douyin).
Press F12 to open the developer tools.
Switch to the "Network" tab.
Refresh the page and find a request in the list.
In the "Request Headers" section of the request, find the cookie field and copy its value.
Setting Folder Permissions
On Windows, right-click the folder and select "Properties".
Switch to the "Security" tab.
Ensure that the current user has "Write" permissions.