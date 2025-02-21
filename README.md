# ZJU-ICAL-PY

> [!NOTE]
> 本项目是基于 [ZJU-ICAL 项目](https://github.com/cxz66666/zju-ical)的 Python 重构版本，更换了调用 API，目前**只支持本科生课程表**生成。本文档部分参考原项目的 README。
>
> 原项目按 LGPL-2.1 协议开源，本项目继承了原项目的协议。

将 ZJU 本科生课程表转换为 iCal 日历格式，方便地导入到 Windows/macOS/Linux/Android/Harmony OS/iOS/iPadOS/watchOS/Wear OS 上，支持：

 - 自动调休安排（由作者不定期维护）
 - 考试安排，包括考点教室、考试座位

> [!WARNING]
> 当前项目仍处于测试阶段，可能存在未知的问题，欢迎提交 Issue 或 Pull Request。

## 免责声明

**该项目仅供学习交流使用，作者不对产生结果正确性与时效性做实时保证，使用者需自行承担因程序逻辑错误或课程时间变动导致的后果。**

所有服务均在使用者的本地设备上运行，ZJUAM 登录密码加密传输，不会存在任何有关用户隐私的蓄意记录/收集行为。

## 开始使用

首先使用 `git` 将本项目克隆到本地，安装 3.8 及以上的 Python 环境，然后使用以下命令安装依赖库：

```sh
pip install -r requirements.txt
```

> [!CAUTION]
> 由于所有代码均在本地运行，请在使用前使用 `git pull` 确保代码是最新的，**尤其是调休安排发生了更新的时候**。

`zjuical.py` 即为主程序，使用以下命令运行：

```sh
python zjuical.py -u [username] -p [password]
```

其中 `[username]` 为浙江大学统一认证用户名，`[password]` 为统一认证密码，运行后即可在当前目录下生成 `zjuical.ics` 文件，导入到日历应用即可，更多的参数请使用 `python zjuical.py --help` 查看。

## 开发计划

 - [ ] 提供网页版订阅，自动推送更新
 - [ ] 支持研究生课程表（作者是本科生，欢迎研究生同学合作）
