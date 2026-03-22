# Gakkai Typesetter — 学会誌組版ツール

ブラウザだけで動く、学会誌向けの簡易組版ツールです。Word原稿（.docx）をドラッグ＆ドロップするだけで、二段組の学会誌レイアウトに変換してプレビューできます。

A browser-based typesetting tool for Japanese academic journals. Drop a Word (.docx) manuscript and instantly preview it in a two-column journal layout.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## デモ / Demo

`gakkai-typesetter.html` をダウンロードしてブラウザで開くだけで動きます。サーバー不要。

Just download `gakkai-typesetter.html` and open it in your browser. No server required.

## 特徴 / Features

- **Word直接読込** — .docxファイルをドラッグ＆ドロップまたはクリックで選択
- **二段組レイアウト** — 学会誌標準の二段組でプレビュー
- **構造自動検出** — タイトル、著者名、要旨、キーワード、見出し、参考文献を自動認識
- **直接編集** — プレビュー画面上でテキストをクリックして直接修正可能
- **書式ツールバー** — 太字、イタリック、下線、上付き・下付き文字に対応
- **誌面設定** — 学会誌名、巻号、発行年、記事区分、著作権表示をカスタマイズ
- **PDF出力** — ブラウザの印刷機能でPDF保存
- **完全クライアントサイド** — すべての処理がブラウザ内で完結。原稿データはサーバーに送信されません
- **単一HTMLファイル** — インストール不要。ファイル1つで動作

## 使い方 / Usage

1. `gakkai-typesetter.html` をブラウザで開く
2. 「誌面設定」に学会誌名・巻号・発行年などを入力
3. Word原稿（.docx）をドロップエリアにドラッグ＆ドロップ
4. プレビューが表示される。テキストをクリックして編集可能
5. 「PDF出力」ボタンでPDF保存

## Word原稿の書き方のコツ

本ツールはWordの構造情報を元にレイアウトを生成します。以下の書き方をすると認識精度が上がります。

- **タイトル** → Wordの「見出し1」スタイルを使用、または太字で記述
- **著者名** → タイトル直後に短い行として記述
- **要旨** → 「要旨」「Abstract」で始まる段落
- **キーワード** → 「キーワード：」「Keywords:」で始まる行
- **節見出し** → Wordの「見出し2」「見出し3」スタイルを使用
- **参考文献** → 「参考文献」「References」という見出しの後に記述

## 技術仕様 / Technical Details

- 単一HTMLファイル（外部依存はCDN経由で読み込み）
- [mammoth.js](https://github.com/mwilliamson/mammoth.js) — Word文書の解析
- [Noto Serif JP](https://fonts.google.com/noto/specimen/Noto+Serif+JP) — Google Fonts経由の明朝体フォント
- 動作にはインターネット接続が必要（CDN読み込みのため）

## 動作環境 / Requirements

- モダンブラウザ（Chrome、Firefox、Edge、Safari）
- インターネット接続（初回のライブラリ・フォント読み込み時）

## 制限事項 / Limitations

- 現時点ではプロトタイプです。以下の機能は未実装です：
  - Excel図表（.xlsx）の取り込み
  - 複数論文の合本・通しページ番号
  - 目次・奥付の自動生成
  - J-STAGE用メタデータXML出力
  - 脚注の処理
  - 画像の埋め込み表示
- Word原稿の書き方によっては、タイトルや著者名の自動検出が正しく動作しない場合があります（プレビュー画面で直接編集して修正できます）

## ロードマップ / Roadmap

- [ ] Excel図表の読み込みと自動配置
- [ ] 複数論文の一括処理と合本PDF生成
- [ ] 目次・奥付の自動生成
- [ ] J-STAGE登載用XMLの出力
- [ ] 脚注・注の自動処理
- [ ] 画像の表示対応
- [ ] オフライン対応（ライブラリの同梱版）

## ライセンス / License

MIT License

## 貢献 / Contributing

Issue・Pull Requestを歓迎します。

Issues and pull requests are welcome.
