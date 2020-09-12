# visdom-static

解决使用 visdom 时因静态文件下载失败导致启动白屏的问题。

## 使用

- 使用 pip 安装 visdom：`pip install visdom`
- 克隆或下载本仓库
- 将仓库的 `visdom` 文件夹下的文件覆盖到 `<your_python_path>/Lib/site-packages/visdom`

## 主要修改内容

- 补齐了 `static` 目录下所需的 JS、CSS等文件
- 注释掉 `server.py` 中 download_scripts_and_run 函数对 download_scripts 的调用，阻止再次下载静态文件

## 版本

在 visdom 0.1.8.5、0.1.8.9 下均正常工作