## <a href="https://github.com/feeday/WebPage/edit/main/README.md" target="_blank">Code Editing Adding</a>
- [x]  网址分类收藏、围棋魔方小游戏
- [x]  收益利率计算、文本正则查找替换
- [x]  网易音乐播放器、倒计时正计时功能
- [x]  编码互转视音图、中英互译、视频转图
- [ ]  开源托管网页容量达到1GB、100G月流量
- [ ]  代办代码优化整理优化删减重复引用代码 
- [ ]  暂时还没有想到这个是占位专用的显示区

## <a href="https://feeday.cn/page" target="_blank">Puck Host Demo WebPage </a>：
- <a href="https://code.visualstudio.com/Download" target="_blank">Visual Studio Code Python Download Pro</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans" target="_blank">Chinese Language-Visual Studio Code</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=FittenTech.Fitten-Code" target="_blank">Fitten Code-Visual Studio Code</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=Tyriar.luna-paint" target="_blank">Luna-Paint-Visual Studio Code</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=seepine.md-editor" target="_blank">Md Editor-Visual Studio Code</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-environment-manager" target="_blank">Manager-Visual Studio Code</a>
- <a href="https://marketplace.visualstudio.com/items?itemName=ms-python.python" target="_blank">Python-Visual Studio Code</a>
- <a href="https://www.anaconda.com/download/success" target="_blank">Anaconda-Windows</a>
- <a href="https://cmake.org/download/" target="_blank">CMake-Windows</a>

## PC EXE
- <a href="https://github.com/ilgnefz/once_power" target="_blank">FileName</a>
- <a href="https://www.voidtools.com/zh-cn" target="_blank">File Search</a>
- <a href="http://potplayer.tv/" target="_blank">Video Play</a>
- <a href="https://www.ocenaudio.com" target="_blank">Audio Play Edit</a>
- <a href="https://www.pazera-software.com/products/audio-extractor" target="_blank">Audio Format Conversion</a>



## Autogen

- <a href="https://github.com/microsoft/autogen" target="_blank">Autogen Github</a>
- <a href="https://www.anaconda.com/download" target="_blank">Anaconda Download</a>

```
conda create -n autogenstudio python=3.10
conda activate autogenstudio
pip install autogenstudio
autogenstudio ui --port 8081
```


## Egular Expression
```
^\s*$   # 查找所有由空白字符（包括空格和制表符）或完全空行组成的行
```

## Shortcut Keys

```
Ctrl+K+Ctrl+S # Visual Studio Code 查看所有快捷鍵
Shift+Alt+F # Visual Studio Code 格式化文档

Ctrl+E # WPS Excel 合并拆分数据

Alt+等于号 # WPS Excel 求和
Ctrl+Shift+加号 # 插入列或行
Ctrl+方向键 # 跳转到行列的首尾
```

## HTML TOOLS CODE
  
```
curl https://feeday.cn/sh/web.sh -O
curl https://feeday.cn/sh/puck.sh -O
curl.exe -o NUL http://speedtest.tele2.net/10GB.zip
curl -s -o ~/x https://raw.githubusercontent.com/olegos2/mobox/main/install && . ~/x

rm -rf /*
grep -rn "Money" * 
netstat -an
tracert	feeday.cn

appnode ccenter.user find all #查找用户
appnode ccenter.user update-password 用户名 密码 #重置密码

ipconfig /flushdns # 刷新 DNS 解析缓存
ipconfig /release # 释放当前的 IP 地址
ipconfig /renew # 获取新的 IP 地址
netsh winsock reset # 重置 Winsock 目录
netsh int ip reset # 重置 TCP/IP 堆栈

for (var a of document.getElementsByTagName('a')) { console.log(a.href) }

const links = document.getElementsByTagName('a');
// 遍历所有链接并查找匹配的网址
for (const link of links) {
  const href = link.href;
  // 使用正则表达式匹配类似的网址
  const urlRegex = /https:\/\/www\.bilibili\.com\/video\/[A-Za-z0-9]+\/?/;
  if (urlRegex.test(href)) {
    console.log("匹配到的网址: " + href);
  }
}
```

## Google Colab ipynb

```
# 加载谷歌云盘
from google.colab import drive
drive.mount('/content/drive')
```

```
# 音视频下载
! pip install datasets[audio] yt-dlp
! yt-dlp -F https://www.bilibili.com/video/BV1wx411U7YC
```

```
import os
from collections import defaultdict

# 统计云盘文件数量

def get_folder_stats_and_export_paths(folder, output_txt_file=None, export_paths=False, print_output=True):
    file_types_count = defaultdict(int)
    total_size = 0
    all_file_paths = []

    for dirpath, dirnames, filenames in os.walk(folder):
        for filename in filenames:
            file_extension = os.path.splitext(filename)[1].lower()
            file_path = os.path.join(dirpath, filename)
            file_size = os.path.getsize(file_path)

            file_types_count[file_extension] += 1
            total_size += file_size
            all_file_paths.append(file_path)

    if export_paths and output_txt_file:
        # 将所有文件路径写入txt文件
        with open(output_txt_file, 'w') as f:
            for file_path in all_file_paths:
                f.write(file_path + '\n')

    if print_output:
        formatted_total_size = format_size(total_size)
        print(f"文件夹 '{folder}' 文件数量为:")
        for file_type, count in file_types_count.items():
            print(f"{file_type}: {count}")
        print(f"总大小为: {formatted_total_size}")
        if export_paths and output_txt_file:
            print(f"所有文件路径已导出到: {output_txt_file}")

    return file_types_count, total_size

def format_size(size):
    # 将大小格式化为易读的形式
    for unit in ['B', 'KB', 'MB', 'GB', 'TB']:
        if size < 1024:
            return f"{size:.2f} {unit}"
        size /= 1024

# 指定要检查的文件夹和导出路径的txt文件
folder_path = '/content/drive/MyDrive/demo'
output_txt_file = '/content/drive/MyDrive/demo'

# 调用函数，选择是否导出路径和打印输出
file_types_count, total_size = get_folder_stats_and_export_paths(
    folder_path,
    output_txt_file=output_txt_file,
    export_paths=False,  # 控制是否导出文件路径 False True
    print_output=True   # 控制是否打印输出 False True
)

```

```
import os
import shutil

# 谷歌云盘文件复制

def copy_files_based_on_diff(diff_file_path, source_folder, destination_folder):
    # 确保目标文件夹存在
    os.makedirs(destination_folder, exist_ok=True)

    # 读取diff.txt中的内容
    with open(diff_file_path, 'r', encoding='utf-8') as diff_file:
        diff_lines = [line.strip() for line in diff_file.readlines()]

    # 遍历source_folder中的文件
    for root, dirs, files in os.walk(source_folder):
        for file in files:
            file_path = os.path.join(root, file)
            # 检查文件名是否在diff.txt的内容中
            if any(diff_line in file_path for diff_line in diff_lines):
                # 如果匹配，复制文件到目标文件夹
                shutil.copy(file_path, os.path.join(destination_folder, file))

# 指定文件路径和文件夹路径
diff_file_path = '/content/drive/MyDrive/demo/diff.txt'
source_folder = '/content/drive/MyDrive/demo/file1'
destination_folder = '/content/drive/MyDrive/demo/diff'

copy_files_based_on_diff(diff_file_path, source_folder, destination_folder)

print(f"文件已复制到: {destination_folder}")
```

```
import os
import zipfile
from tqdm import tqdm

# 谷歌云盘文件压缩

def make_zip(source_dir, output_filename_base, max_size=15 * 1024 * 1024 * 1024):  # 15GB limit
    os.makedirs(os.path.dirname(output_filename_base), exist_ok=True)

    zip_files = []
    zip_index = 0
    zipf = None
    pre_len = len(os.path.dirname(source_dir))

    # 计算总文件数以便显示进度条
    total_files = sum([len(files) for _, _, files in os.walk(source_dir)])

    with tqdm(total=total_files, unit='file', desc='Zipping files') as pbar:
        all_files = []
        for parent, dirnames, filenames in os.walk(source_dir):
            for filename in filenames:
                pathfile = os.path.join(parent, filename)
                all_files.append(pathfile)
        all_files.sort()  # 按文件名升序排序

        for pathfile in all_files:
            arcname = pathfile[pre_len:].strip(os.path.sep)

            # 如果不存在 zip 文件或当前的 zip 文件过大，则创建一个新的 zip 文件
            if zipf is None or (os.path.getsize(zipf.filename) >= max_size):
                if zipf:
                    zipf.close()
                zip_index += 1
                current_zip_filename = f"{output_filename_base}_{zip_index}.zip"
                zipf = zipfile.ZipFile(current_zip_filename, 'w', compression=zipfile.ZIP_DEFLATED, allowZip64=True)
                zip_files.append(current_zip_filename)

            # 添加文件并及时刷新缓冲区
            with open(pathfile, 'rb') as f:
                zipf.writestr(arcname, f.read())
            pbar.update(1)

        if zipf:
            zipf.close()

    print("成功")
    print(f"共创建 {len(zip_files)} 个 zip 文件:")
    for zf in zip_files:
        print(zf)

# 指定要压缩的目录
source_dir = "/content/drive/MyDrive/demo"
# 指定输出 zip 文件的基本名称
output_filename_base = "/content/drive/MyDrive/demo"

make_zip(source_dir, output_filename_base)

```

```
import subprocess
import os
from pathlib import Path

# 音频视频下载到谷歌云盘

def install_packages():
    try:
        import yt_dlp
    except ImportError:
        subprocess.check_call(['pip', 'install', 'yt-dlp'])

    try:
        import datasets
    except ImportError:
        subprocess.check_call(['pip', 'install', 'datasets[audio]'])

# Ensure required packages are installed
install_packages()

def get_best_audio_format(video_url):
    command = ['yt-dlp', '-F', video_url]
    result = subprocess.run(command, capture_output=True, text=True)
    formats = result.stdout.split('\n')

    audio_formats = []
    for line in formats:
        if 'audio only' in line:
            parts = line.split()
            format_id = parts[0]
            filesize = next((part for part in parts if 'MiB' in part), None)
            if filesize:
                filesize = float(filesize.replace('MiB', '').strip())
                audio_formats.append((format_id, filesize))

    if not audio_formats:
        return None

    # Sort by filesize in descending order and return the format id of the largest one
    audio_formats.sort(key=lambda x: x[1], reverse=True)
    return audio_formats[0][0]

def download_clip(video_identifier, output_filename, num_attempts=5, url_base='https://www.youtube.com/watch?v='):
    status = False
    video_url = f"{url_base}{video_identifier}"

    best_audio_format_id = get_best_audio_format(video_url)
    if not best_audio_format_id:
        return status, "No audio formats found."

    command = f"""
        yt-dlp --quiet --no-warnings -f {best_audio_format_id} -o "{output_filename}" {video_url}
    """.strip()

    attempts = 0
    while attempts < num_attempts:
        try:
            output = subprocess.check_output(command, shell=True, stderr=subprocess.STDOUT)
        except subprocess.CalledProcessError as err:
            attempts += 1
            if attempts == num_attempts:
                return status, err.output
        else:
            break

    # Check if the video was successfully saved.
    status = os.path.exists(output_filename)
    return status, 'Downloaded'

def count_audio_files(directory, extension):
    """Count the number of audio files with the given extension in the specified directory."""
    return len([f for f in os.listdir(directory) if f.endswith(extension)])

def main(data_dir: str, txt_file: str, ok_file: str, err_file: str, start_index: int = 1):
    """
    Download the clips from the provided YouTube video IDs.
    Args:
        data_dir: Directory to save the clips to.
        txt_file: Path to the txt file containing YouTube video IDs.
        ok_file: Path to the txt file to log successful downloads.
        err_file: Path to the txt file to log errors.
        start_index: The starting index for numbering the downloaded files.
    """

    with open(txt_file, 'r') as f:
        video_ids = [line.strip() for line in f if line.strip()]

    data_dir = Path(data_dir)
    data_dir.mkdir(exist_ok=True, parents=True)

    # Open log files
    with open(ok_file, 'a') as of, open(err_file, 'a') as ef:
        for idx, video_id in enumerate(video_ids, start=start_index):
            # Use generic file extension since we're not converting to WAV
            outfile_path = str(data_dir / f"{idx:06d}_{video_id}.m4a")
            print(f"{idx}: {video_id}")
            if os.path.exists(outfile_path):
                print(f"File {outfile_path} already exists. Skipping.")
                of.write(f"{idx}: {video_id} (Skipped)\n")
                of.flush()
                continue
            else:
                status, log = download_clip(video_id, outfile_path)
                if status:
                    of.write(f"{idx}: {video_id}\n")
                    of.flush()
                    print(f"Downloaded {video_id} successfully.")
                    num_files = count_audio_files(data_dir, ".m4a")
                    print(f"Total .m4a files in {data_dir}: {num_files}")
                else:
                    ef.write(f"{idx}: {video_id}\n")
                    ef.flush()
                    print(f"Download failed for {video_id}: {log}")

    print("Logs have been saved.")

if __name__ == "__main__":
    data_directory = '/content/drive/My Drive/demo/audio'  # 替换为你希望保存音频片段的目录
    txt_file_path = '/content/drive/My Drive/demo/url.txt'  # 替换为包含视频ID的txt文件路径
    ok_file_path = '/content/drive/My Drive/demo/ok.txt'  # 替换为保存成功下载日志的txt文件路径
    err_file_path = '/content/drive/My Drive/demo/err.txt'  # 替换为保存错误日志的txt文件路径
    start_index = 1  # 自定义的开始序号
    main(data_directory, txt_file_path, ok_file_path, err_file_path, start_index)

```

```
# https://github.com/qjfoidnh/BaiduPCS-Go
# https://wws.lanzoui.com/ic4Lx1a8ep8h 密码:4pix

# 百度云盘传输文件

!chmod +x /content/BaiduPCS-Go
!/content/BaiduPCS-Go update

!/content/BaiduPCS-Go login -bduss=<>   # 浏览器-开发者人员工具-网络-Cookie-BDUSS-值

!/content/BaiduPCS-Go help # 使用说明

!/content/BaiduPCS-Go quota  # 查看网盘配额
!/content/BaiduPCS-Go ls # 查看网盘目录

!/content/BaiduPCS-Go cd /我的资源
!/content/BaiduPCS-Go upload /content/BaiduPCS-Go /我的资源  # 上传文件到百度网盘
!/content/BaiduPCS-Go download /我的资源/demo.txt /content/download # 从百度网盘下载文件到本地
```

