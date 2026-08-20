<p align="center">
  <a href="./README.md"><img src="https://img.shields.io/badge/简体中文-当前语言-2563eb?style=for-the-badge" alt="简体中文"></a>
  <a href="./README_EN.md"><img src="https://img.shields.io/badge/English-Switch-334155?style=for-the-badge" alt="English"></a>
</p>

# MarketAhead

MarketAhead 是一套面向 A股、港股市场与美股盘前时段的静态每日市场简报。它将每个交易日的研究笔记整理为可浏览的 HTML 仪表盘，并通过 JSON 数据提供日历归档。

在线站点：[https://market-ahead-open.vercel.app/](https://market-ahead-open.vercel.app/)

## 项目概览

- 在同一个静态页面展示 A股港股早报与美股盘前简报
- 通过日历浏览历史市场简报
- 每日归档数据存放于 `history/data/`
- 使用 `history/manifest.json` 提供归档导航元数据
- 无需后端，可部署到 GitHub Pages 或任意静态托管平台

## 仓库结构

- `index.html`：主仪表盘与最新简报
- `history/index.html`：历史日期视图
- `history/manifest.json`：可用简报日期列表
- `history/data/YYYY-MM-DD.json`：每日简报归档内容

## 本地查看

可以直接在浏览器中打开 `index.html`，也可以使用任意静态文件服务器运行本项目。

```sh
python3 -m http.server 8000
```

然后访问 `http://localhost:8000`。

## 更新流程

1. 在 `index.html` 中更新最新市场简报。
2. 新增或更新对应的 `history/data/YYYY-MM-DD.json` 归档记录。
3. 更新 `history/manifest.json`，使归档日历包含新日期。
4. 提交并发布静态文件。

## 免责声明

本项目仅用于市场研究与信息整理，不构成任何投资建议。
