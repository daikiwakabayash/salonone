# CLAUDE.md — Salon+ LP プロジェクト指示

このファイルは Claude Code がプロジェクトを理解するための指示書です。

## プロジェクト概要
サロン・整体院向け経営プラットフォーム「Salon+」のランディングページ（1ページ完結）。
`index.html` に HTML / CSS / JavaScript をすべて内包し、画像のみ `assets/` から相対パスで参照する構成です。ビルド工程やフレームワークはありません。素の HTML を直接編集します。

## 編集時のルール

### カラーは必ず CSS 変数を使う
`index.html` の `<style>` 内 `:root` にブランドカラーを定義済み。色を足す・変える時はハードコードせず変数を参照／追加すること。
- `--green:#003B36`（メイン深緑）
- `--gold:#D8BE84`（サブ・シャンパンゴールド）
- `--bg:#F4F9F7`（背景）

### トーン＆マナー
高級ホテル／金融系SaaS的な落ち着き。深緑×ゴールド、広い余白、Fraunces（欧文セリフ）＋Zen Kaku Gothic New（和文）。新しい要素も必ずこのトーンに合わせる。

### ブランド表記
- 名称は必ず「Salon+」（旧称：SalonOne / Salon Base は使わない）。
- ロゴ：`assets/mark-plus.svg`（マークのみ）／`assets/logo-salonplus.svg`（マーク+ワードマーク）
- コンセプト：これ一つで、サロン経営のすべてを。
- メッセージ：One Platform. One Management. ／ 経営を、ひとつに。 ／ 経営に、＋を。

### 個人情報・ダミーデータ
UIモック内の氏名・連絡先はすべてダミー（山田太郎・佐藤花子・090-XXXX-XXXX 等）。
実在の個人情報は絶対に入れないこと。店舗名は「渋谷院」等の架空名を使用。

## セクション構成（index.html 内の順序）
1. ナビ（固定ヘッダー／モバイルはハンバーガー）
2. ヒーロー（`.hero`）
3. 連携バッジ帯（`.trust`）
4. コンセプト（`#concept`）
5. Before / After（`.problem`）
6. 全機能タブ（`#features`／JSでタブ切替）
7. Product Tour（`#showcase`／実画面の交互レイアウト）
8. More Screens ギャラリー（`#screens`）
9. 強み6つ（`#strengths`）
10. AIサジェスト（`.ai`）
11. 6月限定オファー（`#offer`／カウントダウンJSあり）
12. FAQ（`.faq`／アコーディオンJSあり）
13. 最終CTA（`.final`）
14. フッター（`footer`）
15. モバイル追従CTA（`.mobile-cta`）

## JavaScript（index.html 末尾）
- ナビのスクロール追従（`.scrolled` 切替）
- ハンバーガーメニュー開閉
- 機能タブ切替（`#featTabs`）
- FAQアコーディオン
- オファーのカウントダウン（2026-06-30 締切。期限を変える場合はこの `target` を編集）

## よくある依頼と対応箇所
- 価格・締切の変更 → `#offer` セクション＋JSの `target` 日付
- 機能の追加 → `#features` の該当パネル（`data-p="0〜5"`）にカードを追加
- 新しいUI画面の追加 → `assets/` に画像を置き、`#showcase` か `#screens` に追加
- 文言・コピー変更 → 各セクションのテキストを直接編集

## 確認方法
```bash
python3 -m http.server 8000   # http://localhost:8000
```
