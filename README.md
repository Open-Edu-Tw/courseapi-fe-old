# CourseAPI 前端

![Licensed under GPL-3.0-or-later](https://img.shields.io/github/license/Open-Edu-Tw/courseapi-fe)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/xojs/xo)

> 由於仍在早期開發階段，目前的內容較為零散。

## Tech Stack

這個專案使用了以下 Tech Stacks。
部分比較特別的 Tech Stack 會附上文件說明寫法：

- TypeScript
- React
- Tailwind CSS
- Ladle (Storybook)
  - [《建立 CourseAPI 組件的 Story》](./docs/make-component-story.md)
- Nx (for monorepo)
  - [Nx CLI 的使用教學（英文）](https://nx.dev/using-nx/nx-cli)
  - 原則上 nx 的命令都要以 `pnpm` 開頭，比如 `pnpm nx build types`。

## 專案架構

- apps (App 區，包括各種前端微服務及 mock 後端)
- libs（放置組件及工具的地方）
  - components（CourseAPI 的組件）
  - icons（CourseAPI 用到的圖示）
  - types（CourseAPI 用到的工具類型）

## 開始開發 CourseAPI

您可以選擇在 Gitpod 直接使用定義好的環境，無設定開始開發 CourseAPI；
您亦可可以根據下方的說明，在本機環境配置 CourseAPI 的開發環境。

### 在 Gitpod 開啟這個專案

點一下下方的按鈕即可直接開啟。這個 Gitpod 內含 VS Code、開發常用的 extensions，
以及預先配置好且已經安裝依賴的 Node.js 及 PNPM 環境：

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Open-Edu-Tw/courseapi-fe)

### 在本機環境開始開發

**TL;DR:** 安裝 Node.js v16 版本，配置 corepack (`corepack enable`) 然後安裝依賴 (`pnpm install`)。

目前開發使用的 Node.js 版本為 `v16.15.0`，但應該 `v16` 全系列都可以進行開發。
您可以使用 [`nvm`](https://github.com/nvm-sh/nvm) 等工具安裝 Node v16：

```bash
nvm install 16
nvm use 16
```

> 如果是 Windows 的話，直接到 [Node.js 的官網](https://nodejs.org/en/) 下載 v16 安裝也行。

接下來，請 **fork** 後 clone 這個 repo。您可以點選 GitHub 專案首頁的 “Code” 按鈕，
找到這個專案的 clone 連結。fork 和 clone 部分不多贅述，可參考網路文章進行操作。

接著，您會需要安裝依賴管理工具。我們使用 `corepack` 管理依賴管理工具的版本。
首先，進到專案的根目錄，然後輸入：

```bash
# 一定要進到專案的根目錄！
corepack enable
```

啟用 `corepack`，接著即可開始安裝依賴（本專案使用 PNPM 管理）：

```bash
pnpm i
```

使用 VS Code 或其他文字編輯器或 IDE，即可開始貢獻及開發本專案。
此外，VS Code 會建議 **推薦安裝的延伸模組**，方便您進行程式編寫。

### 配置 Ladle (Storybook)

Ladle 可以讓您清楚看到組件實際顯示的模樣。輸入以下命令即可啟動 Ladle：

```bash
pnpm nx ladle (專案名稱)
```

假如想要看 `icons` 的組件，請輸入：

```bash
pnpm nx ladle icons
```
