# Chain Lens — Blockchain & DeFi Intelligence

ブロックチェーン・DeFiプロジェクトをAIで即時調査できるリサーチツールです。

## セットアップ手順

### Step 1 — リポジトリをGitHubに作成してpush

```bash
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

### Step 2 — GitHub SecretにAPIキーを登録

1. GitHubリポジトリの「**Settings**」タブを開く
2. 左メニュー「**Secrets and variables**」→「**Actions**」をクリック
3. 「**New repository secret**」をクリック
4. Name: `GEMINI_API_KEY`
5. Secret: 取得したGemini APIキー（`AIza...`）を貼り付け
6. 「**Add secret**」をクリック

### Step 3 — GitHub Pages の公開元を設定

1. 「**Settings**」→「**Pages**」を開く
2. Branch: `gh-pages` / フォルダ: `/ (root)` を選択
3. 「**Save**」をクリック

### Step 4 — mainブランチにpushするだけで自動デプロイ

以後、`src/index.html` を修正して `main` ブランチにpushすると
GitHub Actionsが自動でビルド＆デプロイします。

## ファイル構成

```
├── src/
│   └── index.html        ← 編集するファイル（キーは __GEMINI_API_KEY__ のまま）
├── .github/
│   └── workflows/
│       └── deploy.yml    ← 自動デプロイの設定（触らなくてOK）
└── README.md
```

## 仕組み

```
src/index.html（__GEMINI_API_KEY__ と書かれている）
        ↓ GitHub Actionsが自動実行
GitHub SecretのAPIキーに置き換え
        ↓
dist/index.html（キーが埋め込まれた完成版）
        ↓
gh-pagesブランチに公開
```

APIキーはGitHubのコード上に一切現れないため、パブリックリポジトリでも安全です。
