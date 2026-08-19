# 感情日記

[English](README.md) | [한국어](README.ko.md) | [日本語](README.ja.md)

日々の感情を記録し、月ごとに振り返りながら編集できるReact・Vite製のWebアプリケーションです。

[公開アプリを開く](https://emotion-project-xi.vercel.app/)

![感情日記のホーム画面](image.png)

## 概要

感情日記は、実際のユーザーから聞いた「簡単に感情を残したい」という要望を、集中したCRUDプロダクトへ変換したプロジェクトです。各エントリーは日付、5段階の感情、自由記述で構成されます。データはブラウザの`localStorage`に保存されるため、アカウントやバックエンドは必要ありません。

## 主な機能

- 日付、感情、本文を含む日記の作成。
- 月単位での日記一覧表示。
- 新しい順・古い順の並び替え。
- 日記の詳細表示。
- 既存日記の編集と削除。
- ブラウザ`localStorage`による再読み込み後のデータ保持。
- 存在しないルート向けの404ページ。
- デスクトップ・モバイル対応レイアウト。

## 技術スタック

- React 18
- Vite 6
- React Router DOM 7
- Context APIと`useReducer`
- ブラウザ`localStorage`
- CSS

## プロジェクト構成

```text
src/
  components/       エディター、一覧、カード、ヘッダー、ボタン、感情UI
  hooks/            日記検索とページタイトル用hook
  pages/            ホーム、作成、編集、詳細、404
  util/             感情定数、画像マッピング、日付ユーティリティ
  App.jsx           ルーティングと全体状態
  main.jsx          アプリのエントリーポイント
```

## ローカル実行

```bash
git clone https://github.com/zxcc9867/Diary_App.git
cd Diary_App
npm install
npm run dev
```

`http://localhost:5173`を開きます。

## ビルドとプレビュー

```bash
npm run lint
npm run build
npm run preview
```

## データとプライバシー

日記データは現在のブラウザの`localStorage`にのみ保存されます。

- アカウント機能やクラウド同期はありません。
- ブラウザストレージを削除すると日記も削除されます。
- デバイスやブラウザ間で自動同期されません。
- 共有端末で機密性の高い記録に使用しないでください。

## 画面

### ホーム

<img src="image.png" width="800" alt="感情日記のホーム画面" />

### 編集

<img src="image-1.png" width="800" alt="感情日記の編集画面" />

## 今後の改善案

- 感情・キーワード検索。
- 月別感情統計。
- ダークモード。
- 任意のアカウント・クラウド同期。
- モバイルUXの改善。
