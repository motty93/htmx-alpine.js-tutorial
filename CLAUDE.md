# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 日本語でのやり取りについて

このプロジェクトでは、主に日本語でコミュニケーションを行います。コードコメント、ドキュメント、ユーザーとのやり取りは基本的に日本語で行ってください。ただし、コード自体（変数名、関数名など）は英語を使用します。

## プロジェクト概要

このプロジェクトは、HTMXとAlpine.jsを学習するためのチュートリアルプロジェクトです。現在はHTMXの基本的な機能を実装しており、今後Alpine.jsの統合を予定しています。

## 開発環境

### 開発サーバーの起動

```bash
# Bunを使用してローカルサーバーを起動
bunx serve

# ホットリロード付きで起動する場合
bun run --hot index.html
```

## 技術スタック

- **HTMX 2.0.5**: CDN経由で読み込み、動的なHTML操作を実現
- **Alpine.js**: プロジェクト名に含まれているが、まだ実装されていない
- **Bun**: 開発サーバーとランタイムとして使用

## プロジェクト構造

```
/
├── index.html    # メインのHTMLファイル（HTMXのデモ）
├── profile.html  # HTMXで動的に読み込まれるコンテンツ
└── README.md     # 最小限のドキュメント
```

## 現在の実装状況

### HTMX機能
- `hx-get`: profile.htmlの内容を取得
- `hx-swap="outerHTML"`: 要素自体を置き換え
- `hx-target`: レスポンスを挿入する対象要素を指定
- `hx-trigger="mouseover"`: マウスオーバーでリクエストを発火

## 開発時の注意点

1. **Alpine.jsの統合**: プロジェクト名に含まれているが、まだ実装されていないため、今後追加する必要がある
2. **日本語コンテンツ**: profile.htmlには日本語のテキストが含まれているため、文字エンコーディングに注意
3. **シンプルな構造**: ビルドプロセスやパッケージ管理は使用していない静的サイト

## 今後の開発方針

HTMXの基本的な機能は実装済みのため、次のステップとしては：
1. Alpine.jsをCDN経由で追加
2. HTMXとAlpine.jsの連携デモを実装
3. より実践的なサンプルの追加