# 磐誠資訊有限公司 — 官方網站

## 部署到 GitHub + Vercel（步驟）

### 第一步：上傳到 GitHub

1. 登入 [github.com](https://github.com)，點右上角 **+** → **New repository**
2. Repository name 填：`panchen-website`（或你喜歡的名稱）
3. 選 **Public**，點 **Create repository**
4. 在你的電腦，把 `index.html` 和 `vercel.json` 放在同一個資料夾
5. 執行以下指令：

```bash
cd 你的資料夾路徑
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/你的帳號/panchen-website.git
git push -u origin main
```

### 第二步：連結 Vercel 自動部署

1. 前往 [vercel.com](https://vercel.com)，用 GitHub 帳號登入
2. 點 **Add New → Project**
3. 選剛剛建立的 `panchen-website` repository，點 **Import**
4. Framework Preset 選 **Other**（純 HTML 不需要框架）
5. 點 **Deploy**，約 30 秒完成

完成後 Vercel 會給你一個網址，例如：
`https://panchen-website.vercel.app`

### 之後更新網站

只需修改 `index.html` 後執行：

```bash
git add .
git commit -m "更新內容"
git push
```

Vercel 會自動重新部署，約 30 秒生效。

### 自訂網域（選用）

若你有購買網域（如 panchen-it.com.tw），在 Vercel 專案設定 → **Domains** → 加入你的網域即可。
