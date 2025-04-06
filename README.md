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
