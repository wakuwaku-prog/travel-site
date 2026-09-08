# 厦门 3 天 2 夜旅行网站（实例）

> 这是用 **travel-planner-kit** 通用模板跑出的厦门实例。
> 线上站：https://wakuwaku-prog.github.io/travel-site/
> 通用模板（无目的地数据，下一趟旅行直接用）：https://github.com/wakuwaku-prog/travel-planner-kit

## 本仓库内容
- `data/trips/trip-xiamen-2026-09-18.json` — 行程数据（19 POI / 4 餐厅 / 2 酒店 / 11 体验 / 105 来源）
- `data/research/` — 调研中间产物（小红书 79 篇、B站 16 视频种子、视频要点笔记、高德 POI 缓存）
- `guides/厦门-xiamen-攻略.md` — 攻略 v3 最终版
- `scripts/` — 本实例所用脚本（与模板一致：route_fill / export_routes / build_site 等）
- `site/` — 生成网站 + `site/export/*.kml/.gpx` 可导入高德/旅行软件

## 用法
站点是自动生成的：改 `data/trips/trip-xiamen-2026-09-18.json` → 重跑
`python scripts/amap/export_routes.py data/trips/trip-xiamen-2026-09-18.json` 与
`python scripts/build_site.py` → push 触发 GitHub Actions 自动发布。

> 注意：`.env`（高德 Key）不入库；重新 clone 后需自行配置。获取高德 Key 的官方教程（创建项目与 Key）：https://lbs.amap.com/api/mcp-server/create-project-and-key