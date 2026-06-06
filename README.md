# はてなベース HP全体リニューアル

## 概要

`hatenabase.jp` のトップページ・各事業部ページ・ソリューションLPを全面改修するプロジェクト。
ローカルでプレビューを作成し、宮澤さんに差分ベースでWP実装を依頼する。

- **Epic Issue**: [hatena-pr#20](https://github.com/HatenaBase/hatena-pr/issues/20)
- **プレビュー一覧**: [GitHub Pages](https://hatenabase.github.io/hp-preview/index.html)
- **プレビューリポジトリ**: [hp-preview](https://github.com/HatenaBase/hp-preview)
- **本番リポジトリ**: [homepage-wp](https://github.com/HatenaBase/homepage-wp)

### 宮澤さん確認用リンク

| ページ | プレビュー | 本番URL | Issue |
|---|---|---|---|
| トップページ | [プレビュー](https://hatenabase.github.io/hp-preview/top-preview.html) | `hatenabase.jp/` | [#22](https://github.com/HatenaBase/hatena-pr/issues/22) |
| 会計コンサルティング事業部 | [プレビュー](https://hatenabase.github.io/hp-preview/accounting-preview.html) | `hatenabase.jp/accounting/` | [#23](https://github.com/HatenaBase/hatena-pr/issues/23) |
| 研修事業部 | [プレビュー](https://hatenabase.github.io/hp-preview/training-preview.html) | `hatenabase.jp/training/` | [#24](https://github.com/HatenaBase/hatena-pr/issues/24) |

### ソリューションLP

| LP | プレビュー | Issue |
|---|---|---|
| 経理AX — BPO | [プレビュー](https://hatenabase.github.io/hp-preview/lp/ax-bpo/) | [#13](https://github.com/HatenaBase/hatena-pr/issues/13) |
| 経理AX — Premium | [プレビュー](https://hatenabase.github.io/hp-preview/lp/ax-premium/) | [#18](https://github.com/HatenaBase/hatena-pr/issues/18) |
| 速習freee会計研修 | [プレビュー](https://hatenabase.github.io/hp-preview/lp/freee-training/) | [#36](https://github.com/HatenaBase/hatena-pr/issues/36) |
| IPO支援 | [プレビュー](https://hatenabase.github.io/hp-preview/lp/ipo/) | [#16](https://github.com/HatenaBase/hatena-pr/issues/16) |
| 勘定奉行導入支援 | [プレビュー](https://hatenabase.github.io/hp-preview/lp/kaikei-bugyou/) | [#10](https://github.com/HatenaBase/hatena-pr/issues/10) |
| 研修候補者募集 | [プレビュー](https://hatenabase.github.io/hp-preview/lp/training-candidate/) | [#32](https://github.com/HatenaBase/hatena-pr/issues/32) |
| 研修派遣先募集 | [プレビュー](https://hatenabase.github.io/hp-preview/lp/training-dispatch/) | [#33](https://github.com/HatenaBase/hatena-pr/issues/33) |
| Zencom | [プレビュー](https://hatenabase.github.io/hp-preview/lp/zencom/) | [#17](https://github.com/HatenaBase/hatena-pr/issues/17) |

---

## 役割分担

| 担当 | GitHub | 役割 |
|------|--------|------|
| 世戸口 | @seto0615 | コンテンツ方針策定 → プレビュー作成 → 最終レビュー |
| 宮澤 | @kojikojikojikoji | WordPress実装 → デモ環境反映 → 本番push |

---

## 進め方

```
① プレビュー作成（世戸口 × Claude Code）
   - 本フォルダの *-preview.html を編集
   - push → GitHub Pages で確認
       ↓
② 差分整理 → Issue作成（世戸口）
   - プレビューと本番の差分を特定
   - hatena-pr の該当Issueにコメント（プレビューURL + 差分説明）
       ↓
③ WP実装（宮澤）
   - プレビューを参考に homepage-wp のテンプレートを更新
   - ステージング環境で実機確認
       ↓
④ 最終確認 & 本番push（世戸口確認 → 宮澤push）
```

> **詳細なステータス管理は [PJ管理.md](./PJ管理.md) を参照。**

---

## ディレクトリ構造

```
HP改修_seto_edit/
├── README.md                    ← 本ファイル（プロジェクト概要）
├── PJ管理.md                   ← ステータス・アクション管理
├── index.html                   ← プレビュー一覧ページ
├── top-preview.html             ← トップページ プレビュー
├── accounting-preview.html      ← 会計事業部 プレビュー
├── training-preview.html        ← 研修事業部 プレビュー
├── css/                         ← 共通CSS
├── images/                      ← 共通画像素材
├── lp/                          ← ソリューションLP
│   ├── ax-bpo/
│   ├── ax-premium/
│   ├── freee-training/
│   ├── ipo/
│   ├── kaikei-bugyou/
│   ├── training-candidate/
│   ├── training-dispatch/
│   └── zencom/
├── pages/                       ← コンテンツ仕様書（MD）
└── ref/                         ← 参照資料（本番ソース等）
```

---

## 関連リポジトリ（統合元）

以下のリポジトリは本プロジェクトに統合済み。今後は `hp-preview` に一本化する。

| 旧リポジトリ | 内容 | 状態 |
|---|---|---|
| [training-preview](https://github.com/HatenaBase/training-preview) | クラウド会計アカデミーLP | → `hp-preview` に統合 |
| [hatenabase-freee-training](https://github.com/HatenaBase/hatenabase-freee-training) | 速習freee会計研修LP | → `hp-preview` に統合 |
