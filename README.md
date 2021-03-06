# いめーじめーかー for 年賀状

## サービス概要
年賀状のコンテンツを作りたい。ただフォーマット通りでは味気ないなって考える人のために
Web上で画像が編集できるサービスを作りました。

## URL
https://rpg-image-editor.firebaseapp.com/

# 機能一覧
## 画像編集
- 画像アップロード機能
- 作成した画像のダウンロード
- 画像の切り取り
- 画像の反転、回転
- 図形の挿入、描画
- アイコン(アップロード可)、テキストの挿入
- 背景のマスク機能
- フィルタ機能(モノクロ、セピアなど)

# 使用技術
## 言語、フレームワーク
- HTML/CSS/JavaScript
- Vue.js 2.5.10

## 主要ライブラリなど
- Buefy(UIコンポーネント)
　URL:https://buefy.org/
- tui-image-editor(画像編集機能)
　URL:https://ui.toast.com/tui-image-editor/
- Firebase Hosting

## 既知の課題
- レスポンシブ対応
- デフォルト画像の用意

# 環境構築
## Project setup
```
yarn install
```

### 開発環境の起動
```
yarn run serve
```

### 本番環境のセットアップ
```
yarn run build
```

### テスト実行
```
yarn run test
```
