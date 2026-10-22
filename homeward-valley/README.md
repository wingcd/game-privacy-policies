# 《山谷归途》（Homeward Valley）

TapTap 平台提审材料：隐私政策页面。

## 文件说明

- `index.html` — 隐私政策页面（中英俄三语，单文件自包含），手机/桌面自适应，默认按浏览器语言显示，顶部可手动切换；支持 `?lang=zh` / `?lang=en` / `?lang=ru` 参数固定语言

## 在线地址

部署在本仓库的 GitHub Pages 上：

- https://wingcd.github.io/game-privacy-policies/homeward-valley/

平台后台需要填 URL 时直接用上面的地址。

## 基本信息

| 项 | 值 |
| --- | --- |
| 中文名 | 山谷归途（已确认，TapTap app_id 946111） |
| 英文名 | Homeward Valley（与游戏内英文标题一致） |
| 俄文名 | Домой в долину（与游戏内俄文标题一致） |
| 项目路径 | H:\game_dev\taptap_maker\山谷归途（TapTap Maker 工程，另可 build-sud.mjs 转 SUD） |
| 类型 | 休闲益智 · 栈排序解谜 |
| 开发主体 | 成都致样互动科技有限公司（TapTap 后台目前挂个人厂商 developer_id 447170，政策署名按公司主体） |
| 联系邮箱 | wingcd@foxmail.com |

## 与 sort-it-magic-water 政策的差异（按实际代码核对）

- **无昵称/头像收集**：游戏无排行榜/好友功能（scripts 中无 leaderboard、getUserInfo 调用），已删除"用户信息（昵称、头像）"条款，并在导言明示不收集；
- **无支付**：无内购/下单代码（金币仅游戏内产出，商店用金币购买道具），已删除"支付服务"条款；
- **新增云端存档**：`scripts/vs/save.lua` 为本地 + 平台云端双存档（clientCloud），政策第一节与第三方服务节均补入"云端存储"；
- **广告**：3 个激励视频位（撤销补满 `undo_refill`、体力补充 `energy_refill`、胜利翻倍 `win_double`），均走平台/宿主广告 SDK，政策按"激励视频"表述。

## 需要注意 / 后续要改的地方

| 位置 | 说明 |
| --- | --- |
| 日期 | 页面顶部「更新日期 / 生效日期」目前是 2026-10-22，政策改版时记得同步 |
| 邮箱 | 目前用 `wingcd@foxmail.com`，如换主体邮箱需全局替换 |
| 开发主体 | 已按用户确认署名"成都致样互动科技有限公司"；TapTap 后台仍挂个人厂商，若日后后台迁移为企业厂商需保持一致 |
