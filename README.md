
# linx-x

## mcp-server

### 概述

基于云存储构建的音乐网盘 MCP Server，为用户提供智能化的音乐文件管理体验。

### 工具

1. 音乐文件列表 `online_music_list`
    - 描述: 获取音乐文件列表，可以使用`prefix`根据路径过滤，返回音乐文件的key（名称，路径，还可以用于获取下载url）列表
    - 参数:
      - `max_keys` (optional) 最大返回的文件对象数量，默认为100，最大为500
      - `prefix` (optional) 音乐文件名前缀过滤。只返回路径以此前缀开头的音乐文件
      - `start_after` (optional) 分页起始位置。从指定的音乐文件名之后开始列出，用于实现分页浏览
    - 输出: 音乐文件列表，包含`Bucket`, `Key`, `Size`等信息

