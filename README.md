# Bilibili Subtitle Comment Danmaku Extractor Export & AI Summarizer

这是一个用于 B 站视频页的油猴脚本，支持：

- 字幕提取、搜索、复制、导出
- 弹幕拉取、导出、AI 总结
- 评论拉取、导出、AI 总结
- 视频字幕内容 AI 总结
- 自定义 1/2/3 三个 AI 任务
- 可配置默认导航页、手动/自动触发、提示词、LLM 参数、流式输出
- 提供 LLM 连通测试按钮

## 导航页

脚本弹窗内置导航栏：

- 字幕
- 视频总结
- 弹幕总结
- 评论总结
- 自定义1
- 自定义2
- 自定义3
- 设置

## 功能说明

### 1. 字幕页

- 自动拉取字幕轨道并支持切换
- 支持关键词过滤
- 支持复制：
  - 纯文本
  - 时间轴
  - SRT
- 支持导出：
  - TXT
  - SRT
  - VTT
  - JSON

### 2. 弹幕总结页

- 支持手动拉取弹幕
- 支持导出弹幕 TXT
- 支持 AI 总结（手动或自动）

### 3. 评论总结页

- 支持手动拉取评论
- 支持导出评论 TXT
- 支持 AI 总结（手动或自动）

### 4. 视频总结页

- 基于字幕内容进行 AI 总结
- 支持流式展示（按设置）

### 5. 自定义1/2/3

- 每个任务都有独立提示词
- 可分别设置为手动触发或自动触发
- 输入会自动组合当前视频可用的字幕、弹幕、评论材料

## 设置页

设置页可配置：

- 默认打开导航页
- LLM 参数
  - API URL
  - API Key
  - 模型名
  - System Prompt
  - temperature
  - top_p
  - max_tokens
  - 超时
  - 是否流式输出
- 任务触发模式
  - 视频总结 / 弹幕总结 / 评论总结 / 自定义1/2/3
  - 每个任务支持手动或自动
- 数据规模限制
  - 字幕最大行数
  - 弹幕最大行数
  - 评论最大条数
  - 评论抓取页数
- 提示词模板
  - 视频总结提示词
  - 弹幕总结提示词
  - 评论总结提示词
  - 自定义1/2/3提示词

并提供：

- 保存设置
- 恢复默认
- LLM 连通测试

## 安装方式

### 方式一：直接安装（推荐）

打开以下地址，Tampermonkey 会弹出安装页：

`https://raw.githubusercontent.com/constansino/bilibili-subtitle-comment-danmaku-extractor-export-ai-summary/main/bilibili-subtitle-comment-danmaku-extractor-export-ai-summary.user.js`

### 方式二：手动导入

1. 打开 Tampermonkey 管理面板
2. 新建脚本
3. 粘贴 `bilibili-subtitle-comment-danmaku-extractor-export-ai-summary.user.js` 内容
4. 保存并启用

## 使用流程建议

1. 打开任意 B 站视频页
2. 点右下角「视频助手」按钮
3. 先进入「设置」页填写 LLM URL / Key / 模型并做连通测试
4. 回到各总结页执行生成，或把任务切换到自动触发
5. 在字幕/弹幕/评论页按需导出文本

## 注意事项

- 评论接口可能受视频权限、接口风控、登录状态影响
- LLM 请求会消耗你的模型额度
- 自动触发会在每个新视频触发对应任务，请按实际成本配置

## 免责声明

本项目仅用于学习和效率提升，请遵守 B 站相关规则和当地法律法规。
