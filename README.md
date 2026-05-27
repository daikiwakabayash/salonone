# SalonOne ランディングページ

> 経営を、ひとつに。 — これ一つで、サロン経営のすべてを。

サロン・整体院向けオールインワン経営プラットフォーム「SalonOne」のランディングページです。

## 構成

```
salononline-project/
├── index.html        … LP本体（HTML/CSS/JS すべて内包・1ファイル）
├── assets/           … 画像ファイル
│   ├── logo.png      … SalonOne 縦組みロゴ（フッター用）
│   ├── mark.png      … 円形 S1 マーク（ナビ・サイドバー用）
│   ├── dashboard.jpg … 予約管理ダッシュボード
│   ├── map.jpg       … 商圏分析マップ
│   └── ui_m1〜m9.jpg … 各機能のUIモック画像
├── README.md
└── CLAUDE.md         … Claude Code 向けのプロジェクト指示
```

### UIモック画像の対応表
| ファイル | 内容 |
|---|---|
| ui_m1.jpg | スタッフ別売上 / 日報 |
| ui_m2.jpg | 新規・継続サマリー（セラピスト別） |
| ui_m3.jpg | 媒体別ROAS・広告分析 |
| ui_m4.jpg | AIマーケティング分析 |
| ui_m5.jpg | 電子カルテ・顧客台帳 |
| ui_m6.jpg | LINEチャット |
| ui_m7.jpg | 給与計算・業務委託費 |
| ui_m8.jpg | 福利厚生マスタ |
| ui_m9.jpg | 強制リンク管理・流入分析 |

## ローカルで確認する

```bash
# 任意のローカルサーバで開く（画像が相対パス参照のため file:// より推奨）
python3 -m http.server 8000
# → http://localhost:8000 をブラウザで開く
```

## ブランドガイド

| 項目 | 値 |
|---|---|
| ブランド名 | SalonOne |
| コンセプト | これ一つで、サロン経営のすべてを。 |
| メッセージ | One Platform. One Management. ／ 経営を、ひとつに。 |
| メインカラー（深緑） | `#003B36`（他に `#0A4A43` `#0B2F2B` `#02322d`） |
| サブカラー（ゴールド） | `#D8BE84`（他に `#C9A86A` `#E3D3AF`） |
| 背景 | `#F4F9F7` ／ `#FBF8F1` |
| 見出しフォント | Fraunces（欧文セリフ）／ Zen Kaku Gothic New（和文） |

すべてのカラーは `index.html` の `:root` CSS変数で一元管理しています。
