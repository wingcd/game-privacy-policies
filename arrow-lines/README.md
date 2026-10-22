# 《箭头连线》（Arrow Lines）

SUD（OpenPaaS）海外平台提审材料：隐私政策页面。

## 文件说明

- `index.html` — 隐私政策页面（中英俄三语，单文件自包含），手机/桌面自适应，默认按浏览器语言显示，顶部可手动切换；支持 `?lang=zh` / `?lang=en` / `?lang=ru` 参数固定语言

## 在线地址

部署在本仓库的 GitHub Pages 上：

- https://wingcd.github.io/game-privacy-policies/arrow-lines/

平台后台需要填 URL 时直接用上面的地址（俄语区可用 `?lang=ru` 后缀）。

## 基本信息

| 项 | 值 |
| --- | --- |
| 中文名 | 箭头连线（已确认正式名） |
| 英文名 | Arrow Lines（商店全名 Arrow Lines: Connect Puzzle） |
| 俄文名 | Стрелки и линии（商店全名 Стрелки и линии: головоломка） |
| 项目路径 | H:\game_dev\arrow_line\arrow_line（Cocos Creator 3.8 工程） |
| 平台 | SUD（OpenPaaS）小游戏，构建配置 buildconfigs/openpass |
| 类型 | 休闲益智 · 箭头消除连线 |
| 开发主体 | 成都致样互动科技有限公司 |
| 联系邮箱 | wingcd@foxmail.com |

## 政策内容与实际代码核对（2026-10-22）

- **平台账号标识**：宿主应用登录换取用户 ID（`zysdk/user.ts` login 流程）；
- **昵称/头像**：排行榜展示用到 `userController.nickName / avatarUrl`（`RankWindow.ts`），政策含"用户信息（昵称、头像）"条款，仅限排行榜展示目的；
- **云端存档**：游戏进度走 `/user/saveData` 同步游戏服务器（本地 + 云端双存档），政策含"云端数据"条款；
- **广告**：激励视频（`AdManager.ts`，EAdType.Video），政策按"激励视频广告（补充道具、获取额外奖励等场景）"表述；
- **支付**：SUD 道具直购（`zysdk/sud.ts` `/sud/order/*`，服务端签名发货），政策含"支付服务"条款（平台支付，仅接收交易结果）；
- **行为统计**：heartbeat / counter 匿名统计，政策含"行为数据"条款。

## 需要注意 / 后续要改的地方

| 位置 | 说明 |
| --- | --- |
| 日期 | 页面顶部「更新日期 / 生效日期」目前是 2026-10-22，政策改版时记得同步 |
| 邮箱 | 目前用 `wingcd@foxmail.com`，如换主体邮箱需全局替换 |
| 俄语 | 政策已含俄语版；游戏本体俄语支持上线前需按 `docs/游戏多语言名称与描述.md` 落地清单补齐 |
