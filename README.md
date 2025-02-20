# React Router へようこそ！

React Routerを使用した本番環境対応のフルスタックReactアプリケーション構築用テンプレートです。

[![StackBlitzで開く](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/remix-run/react-router-templates/tree/main/default)

## 主な機能

- 🚀 サーバーサイドレンダリング
- ⚡️ ホットモジュールリプレイスメント（HMR）
- 📦 アセットのバンドルと最適化
- 🔄 データの読み込みと更新
- 🔒 TypeScript標準搭載
- 🎉 スタイリング用TailwindCSS
- 📖 [React Router ドキュメント](https://reactrouter.com/)

## はじめ方

### インストール

依存関係をインストールします：

```bash
npm install
```

### 開発

開発サーバーを起動します（HMR対応）：

```bash
npm run dev
```

アプリケーションは `http://localhost:5173` で利用可能になります。

## 本番用ビルド

本番環境用のビルドを作成：

```bash
npm run build
```

## デプロイ

### Dockerでのデプロイ

このテンプレートには、各パッケージマネージャー用に最適化された3つのDockerfileが含まれています：

- `Dockerfile` - npm用
- `Dockerfile.pnpm` - pnpm用
- `Dockerfile.bun` - bun用

Dockerでビルドして実行：

```bash
# npm の場合
docker build -t my-app .

# pnpm の場合
docker build -f Dockerfile.pnpm -t my-app .

# bun の場合
docker build -f Dockerfile.bun -t my-app .

# コンテナの実行
docker run -p 3000:3000 my-app
```

コンテナ化されたアプリケーションは、以下を含むDockerをサポートする任意のプラットフォームにデプロイ可能です：

- AWS ECS
- Google Cloud Run
- Azure Container Apps
- Digital Ocean App Platform
- Fly.io
- Railway

### 手動デプロイ

Node.jsアプリケーションのデプロイに慣れている場合、内蔵のアプリケーションサーバーは本番環境での使用に対応しています。

`npm run build` の出力をデプロイしてください：

```
├── package.json
├── package-lock.json (または pnpm-lock.yaml, bun.lockb)
├── build/
│   ├── client/    # 静的アセット
│   └── server/    # サーバーサイドコード
```

## スタイリング

このテンプレートには[Tailwind CSS](https://tailwindcss.com/)が初期設定済みで含まれています。お好みのCSSフレームワークを使用することも可能です。

---

React Routerで❤️を込めて作られています。
