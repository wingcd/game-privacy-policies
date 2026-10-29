# 《小猪出圈》（Let the Piggies Out）

SUD（OpenPaaS）等平台提审材料：隐私政策页面。游戏为一指滑块解谜手游（点一点小动物、把它送出猪圈），支持中英俄三语。

> 命名说明：项目原名"挪一挪猪"为他人游戏名，已于 2026-10-28 弃用并定稿为「小猪出圈 / Let the Piggies Out / Свинки на волю!」，详见游戏项目内 `creator/doc/游戏名与多语言介绍文案.md`。本政策使用定稿名。

## 文件说明

- `index.html` — 隐私政策页面（中英俄三语，单文件自包含），手机/桌面自适应，默认按浏览器语言显示，顶部可手动切换；支持 `?lang=zh` / `?lang=en` / `?lang=ru` 参数固定语言

## 在线地址

部署在本仓库的 GitHub Pages 上：

- https://wingcd.github.io/game-privacy-policies/piggies-out/

平台后台需要填 URL 时直接用上面的地址（俄语区可用 `?lang=ru` 后缀）。

## 基本信息

| 项 | 值 |
| --- | --- |
| 中文名 | 小猪出圈 |
| 英文名 | Let the Piggies Out（全球统一短名 Piggies Out） |
| 俄文名 | Свинки на волю! |
| 项目路径 | H:\game_dev\挪一挪猪\project（Cocos Creator 3.8 工程，项目名 thread-jam） |
| 平台 | SUD（OpenPaaS）小游戏，构建配置 buildconfigs/openpass（另有微信/抖音/快手/支付宝/TapTap/美团/Yalla/草木流川 等多渠道构建配置） |
| 类型 | 休闲益智 · 滑块解谜 |
| 上架文案 | 项目内 `creator/doc/游戏名与多语言介绍文案.md`（2026-10-28 定稿） |
| 开发主体 | 成都致样互动科技有限公司 |
| 联系邮箱 | wingcd@foxmail.com |

## 政策内容与实际代码核对（2026-10-28）

- **平台账号标识**：宿主应用登录换取用户 ID / OpenID（`zysdk/user.ts`、`zysdk/sud.ts` `/sud/login` code 换会话；草木流川 `cmlcsdk/login.ts` 返回 openid），政策表述为"平台用户标识（如用户 ID、OpenID）"；
- **昵称/头像**：排行榜展示用到 `nickName / avatarUrl`（`zysdk/leaderboard.ts`），政策含"用户信息（昵称、头像）"条款，仅限排行榜展示目的；
- **云端存档**：游戏进度走游戏服务器存档（本地 + 云端双存档，`framework/modules/base/BaseDAO.ts`，另有 `TapTapCloudSave.ts`），政策含"云端数据"条款；
- **广告**：激励视频 + 横幅 + 插屏（`game/ad/AdManager.ts`；原生 Android 走 AppLovin Max `MaxAdAndroidInterface.ts`），政策按"激励视频广告（补充道具、获取额外奖励等场景），部分平台下亦可能展示插屏或横幅广告"表述；
- **支付**：道具直购（`zysdk/order.ts` `/order/create`；SUD `zysdk/sud.ts` `/sud/order/*`；Yalla 渠道 `zysdk/yalla_pay.ts`），政策含"支付服务"条款（平台支付，仅接收交易结果）；
- **行为统计**：heartbeat / counter 匿名统计（`zysdk/heartbeat.ts`、`zysdk/counter.ts`、`StatisticController.ts`；草木流川埋点 `cmlcsdk`），政策含"行为数据"条款；
- **本地数据**：金币、道具、装扮、设置存本地（各 DAO），政策"本地数据"条款与之一致。

## 需要注意 / 后续要改的地方

| 位置 | 说明 |
| --- | --- |
| 日期 | 页面顶部「更新日期 / 生效日期」目前是 2026-10-28，政策改版时记得同步 |
| 邮箱 | 目前用 `wingcd@foxmail.com`，如换主体邮箱需全局替换 |
| 游戏名 | 名称取自 `creator/doc/游戏名与多语言介绍文案.md`（2026-10-28 定稿）；若后台注册名最终用短名 Piggies Out，页面标题文案无需改动（正文未依赖注册名） |
