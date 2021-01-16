# slackware-WSL

This project is a fork of [slackware-container](https://github.com/vbatts/slackware-container).

本项目是[slackware-container](https://github.com/vbatts/slackware-container)的一个fork分支。

My target is to build an minimun slackware distribution for [Windows Subsystem for Linux](https://docs.microsoft.com/zh-cn/windows/wsl/).

目标是构建一个在 [适用于 Windows 的 Linux 子系统 (WSL)](https://docs.microsoft.com/zh-cn/windows/wsl/) 上运行的 slackware 发行版。

this repo contains few scripts to build base filesystem of slackware for running in wsl environment.

这个仓库包含少量脚本用于构建于 WSL 运行所需的 slackware 基础文件系统。

## pre-requires

Currently this script only tested in my slackware64-14.2 VM.
So if there is any problem when running this script under another linux distribution,
try it under slackware64-14.2 or modify script by your self.

目前本脚本仅在 slackware64-14.2 虚拟机下测试过，如果你在其他Linux发行版运行脚本出现问题，请尝试在 Slackware64-14.2 下运行，或者自行修改脚本。

PS: it should be easy if you known a bit of shell scripting.

PS: 如果你懂点shell脚本的话应该不难。

## build

just make it.

> be aware, you need root privilege to mount special filesystem such as /proc and /sys.
>
> 注意，你需要 root 权限来挂载特殊文件系统如 /proc 和 /sys 。
>
> you *SHOULD* always read source code first before giving super user privilege to unknown script.
>
> 你 *应该* 在以超级管理员权限运行未知脚本前阅读脚本源码。

运行 make 命令。

```
sudo make VERSION=14.2
```

## TODOs

- [ ] merge get_paths.sh and mkimage-slackware.sh
- [ ] read, understand, and cleanup mkimage-slackware.sh
- [ ] maybe rewrite this script with python or put them all in a makefile? seems unnecessary but should be fun.

## Contributing

please hack on this and send feedback!

## License

Copyright (c) 2021, nnnewb <weakptr@outlook.com>
Copyright (c) 2013, Vincent Batts <vbatts@hashbangbash.com>
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
