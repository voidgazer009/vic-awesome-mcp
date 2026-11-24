# Vic Awesome MCP · 全网精品 MCP 精选

> 每天从全网挑 3 个最优质的 MCP Server，亲测、打分、写清楚怎么用。每个都能用一行命令从本仓库直接装进你的 AI 客户端。
>
> Hand-picked best MCP servers from across the web, 3 a day. Each one is tested, scored and installable into your AI client with one line, straight from this repo.

**By Vic** · 收录标准见 [SELECTION_STANDARD.md](SELECTION_STANDARD.md) · 机器可读目录 [catalog.json](catalog.json)

## 一行安装 · Install in one line

```bash
# 看全部
curl -fsSL https://raw.githubusercontent.com/voidgazer009/vic-awesome-mcp/main/install.py | python3 - list

# 装进 Cursor（换成 claude-desktop / claude-code / vscode / codex 都行）
curl -fsSL https://raw.githubusercontent.com/voidgazer009/vic-awesome-mcp/main/install.py | python3 - playwright --client cursor --write
```

只需要 Python 3.9+，不装任何依赖。不加 `--write` 只打印配置；加了会先备份原配置（.bak）再合并。密钥永远不写进文件，只引用环境变量。

## 精选目录 · Catalog

| MCP | 一句话 | 适合哪条线 | 鉴权 | Vic 评分 | 收录 |
|---|---|---|---|---|---|
| [Mapbox MCP Server](servers/mapbox.md) | 查路线、算距离、给多个送货点排最优顺序 | 物流 · 外贸 | Token / OAuth | 86 | 2026-11-18 |
| [Filesystem MCP Server](servers/filesystem.md) | 让 AI 读你指定文件夹里的单据和素材（默认只读） | 外贸 · 物流 · 一人公司 · 自媒体 | 免密钥 | 90 | 2026-11-15 |
| [Memory MCP Server](servers/memory.md) | 给 AI 一本跨对话的记事本，记住客户和习惯 | 外贸 · 物流 · 一人公司 · 自媒体 | 免密钥 | 88 | 2026-11-15 |
| [Stripe MCP Server](servers/stripe.md) | 查收款、客户、发票、余额（关键动作需你批准） | 外贸 · 一人公司 | OAuth / Token | 86 | 2026-11-15 |
| [Time MCP Server](servers/time.md) | 让 AI 准确知道现在几点、跨时区换算 | 外贸 · 物流 · 一人公司 · 自媒体 | 免密钥 | 90 | 2026-11-14 |
| [Exa MCP Server](servers/exa.md) | AI 专用搜索：找客户、找选题、查行业新闻 | 外贸 · 物流 · 一人公司 · 自媒体 | 免密钥（Key 可选） | 89 | 2026-11-14 |
| [Apify MCP Server](servers/apify.md) | 调用几千个现成爬虫：地图、社媒、电商数据 | 外贸 · 物流 · 一人公司 · 自媒体 | OAuth / Token | 89 | 2026-11-14 |
| [Playwright MCP](servers/playwright.md) | 让 AI 打开网页、点击、填表、抓数据 | 外贸 · 物流 · 一人公司 · 自媒体 | 免密钥 | 92 | 2026-11-13 |
| [GitHub MCP Server](servers/github.md) | 让 AI 管理 GitHub 仓库、Issue、PR（默认只读） | 一人公司 | OAuth / Token | 92 | 2026-11-13 |
| [Context7](servers/context7.md) | 写代码前先查最新官方文档 | 一人公司 | 免密钥（Key 可选） | 89 | 2026-11-13 |

## 怎么选出来的 · How they are picked

1. **硬门槛**：开源许可证明确、30 天内有更新、亲测能用、无已知严重漏洞、不和已收录的重复。
2. **100 分制**：维护方、活跃度、社区认可、对外贸 / 物流 / 一人公司 / 自媒体的用处、上手难度、安全与权限、文档、许可证。**≥ 85 分才收录**。
3. **安全默认值**：能只读的默认只读（如 GitHub），浏览器默认隔离模式（如 Playwright）。要更多权限时显式加参数。

## 每张卡片里有什么 · What each card has

为什么收录 · Vic 的四条业务线用法 · 主要工具 · 一行安装 · 各客户端手动配置 · 注意事项与风险 · 评分明细

## 维护 · Maintenance

- 每天新增 3 个，记录在 [CHANGELOG.md](CHANGELOG.md)。
- `python3 tools/validate.py --live --smoke` 检查目录、评分、安装配置，并实际连接免密钥的 MCP。
- 每周复查一次，归档或停更的会下架。

## 也看看 · See also

Vic 自己写的 MCP Server：[vic-mcp-servers](https://github.com/voidgazer009/vic-mcp-servers)


## 公共数据 API（Apify）

- [Public Records MCP](https://github.com/GeminiGeorge22/publicrecords-mcp/blob/main/README.zh-CN.md) - 18 个托管在 Apify 上的公共数据 MCP 服务器：美国联邦合同与资助（SAM.gov、Grants.gov、USAspending）、欧盟 TED 与英国招标、市议会会议、Ashby/Greenhouse/Lever/SmartRecruiters 职位、公司社交账号、Google 广告透明度、Etsy 销量、体育赔率、Spotify 播放量.

## License

本仓库的文字、目录和脚本采用 MIT 许可。各 MCP Server 归原作者所有，遵循各自许可证。
