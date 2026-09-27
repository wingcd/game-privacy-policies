# game-privacy-policies

各游戏的隐私政策 / 用户协议静态站点，通过 GitHub Pages 访问。

- 站点首页：https://wingcd.github.io/game-privacy-policies/
- 每个游戏一个文件夹，互不影响；文件夹里放 `index.html`，访问地址即 `https://wingcd.github.io/game-privacy-policies/<文件夹名>/`

## 目录结构

```
├── index.html                 # 站点首页（游戏列表，需手动加条目）
├── .nojekyll                  # 让 Pages 按原样输出文件
├── template/                  # 新游戏协议模板（基于《用户隐私保护指引设置.docx》）
├── 消个毛线/                   # 《消个毛线》隐私政策（中英双语，SUD 提交用）
│   ├── index.html
│   └── README.md              # 该协议的说明 / 待办（英文名占位等）
└── 用户隐私保护指引设置.docx     # 原始参考文档
```

## 新增一个游戏的协议

1. 复制 `template/` 或某个现成游戏的文件夹，重命名为游戏名（中文英文均可；如平台后台不接受中文 URL，用拼音或英文命名）。
2. 编辑其中的 `index.html`：替换游戏名、日期、邮箱、第三方 SDK 信息等占位。
3. 打开根目录 `index.html`，在卡片列表最上面加一段：

   ```html
   <a class="card" href="./游戏文件夹名/">
     <div>
       <div class="name">游戏名</div>
       <div class="desc">隐私政策 · 中英双语</div>
     </div>
     <div class="arrow">›</div>
   </a>
   ```

4. 提交推送：

   ```bash
   git add -A && git commit -m "add <游戏名> privacy policy" && git push
   ```

5. 等约一分钟 Pages 生效，在线地址为 `https://wingcd.github.io/game-privacy-policies/<文件夹名>/`。
