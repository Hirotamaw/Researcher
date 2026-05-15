# Chain Lens — Blockchain & DeFi Intelligence

ブロックチェーン・DeFiプロジェクトをAIで即時調査できるリサーチツールです。

## 使い方

1. **Anthropic APIキー**を取得し、画面上部の入力欄に貼り付ける
   - [Anthropic Console](https://console.anthropic.com/) から取得可能
   - キーはブラウザの`localStorage`にのみ保存され、外部には送信されません

2. **カテゴリを選択**：Blockchain または DeFi

3. **プロジェクト名を入力**して「調査する」をクリック

## 出力項目

### Blockchain
- 正式名称 / ネイティブトークン / 運営体
- 時価総額 / コンセンサスアルゴリズム
- EVM互換性 / スマートコントラクト対応
- 概要 / 技術的特徴 / ユースケース
- 開発歴タイムライン / 今後のロードマップ
- 金融機関・取引所との連携実績
- エコシステム / 対応ウォレット / セキュリティインシデント

### DeFi
- 正式名称 / ガバナンストークン / 運営体
- TVL / カテゴリー / 累計取引量
- 対応チェーン / 概要 / 技術的特徴
- 開発歴タイムライン / 今後のロードマップ
- 金融機関・取引所との連携実績
- セキュリティ監査歴 / インシデント歴

## GitHub Pages デプロイ手順

1. このリポジトリをGitHubにpush
2. Settings → Pages → Branch: `main` / Folder: `/ (root)` を選択
3. 数分後に `https://<username>.github.io/<repo>/` でアクセス可能に

## 将来の拡張 (Phase 2)

- **Dune Analytics API**: オンチェーンデータのグラフ表示
- **CoinMarketCap API**: リアルタイム時価総額・価格チャート
- **DeFiLlama API**: リアルタイムTVL取得

## 注意事項

- 本ツールの情報はAI生成であり、投資判断には使用しないでください
- 時価総額・TVL等の数値は概算です。最新データはCoinMarketCap・DeFiLlama等でご確認ください
