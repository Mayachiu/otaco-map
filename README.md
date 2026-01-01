# OTACO Map - 太田市デジタル金券 加盟店マップ

太田市のデジタル金券「OTACO」が使える804店舗をインタラクティブなマップで表示するWebアプリケーションです。

![OTACO Map Preview](https://via.placeholder.com/800x400?text=OTACO+Map+Preview)

## 機能

- 🗺️ **インタラクティブマップ**: Leafletを使用した滑らかなマップ操作
- 🔍 **店舗検索**: 店舗名・町名で素早く検索
- 🏷️ **カテゴリフィルター**: 飲食・物販・体験・観光・宿泊で絞り込み
- 💳 **カード対応フィルター**: 磁気・定額カード対応店のみ表示
- 📱 **レスポンシブデザイン**: スマートフォン・タブレット対応
- 📍 **クラスター表示**: 多数の店舗を見やすくグループ化

## 技術スタック

- **Backend**: Node.js + Express
- **Frontend**: Vanilla JavaScript + Leaflet.js
- **Styling**: カスタムCSS（日本風デザイン）
- **Map**: OpenStreetMap (CartoDB Voyager tiles)

## ローカル開発

```bash
# 依存関係をインストール
npm install

# サーバーを起動
npm start

# ブラウザで開く
open http://localhost:3000
```

## Renderへのデプロイ

### 1. GitHubにリポジトリを作成

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/otaco-map.git
git push -u origin main
```

### 2. Renderでデプロイ

1. [Render](https://render.com) にログイン
2. **New** → **Web Service** をクリック
3. GitHubリポジトリを接続
4. 以下の設定で作成:
   - **Name**: `otaco-map`
   - **Environment**: `Node`
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Instance Type**: Free

5. **Create Web Service** をクリック

デプロイ完了後、`https://otaco-map.onrender.com` でアクセス可能になります。

## データについて

店舗データは太田市公式の「太田市デジタル金券等加盟店一覧（令和７年１２月１日現在）」PDFから抽出しています。

- **総店舗数**: 804店舗
- **カテゴリ**: 飲食、物販、体験（生活関連サービス等）、観光、宿泊
- **カード対応**: ○印の店舗はchiicaアプリ・磁気・定額カードが利用可能

## ライセンス

MIT License

## 謝辞

- 地図データ: © OpenStreetMap contributors © CARTO
- 店舗データ: 太田市
