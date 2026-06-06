# HP全体リニューアル PJ管理

> 最終更新: 2026-06-06
> 担当: 世戸口（コンテンツ・プレビュー） / 宮澤（WP実装）

---

## 📋 運用フロー

```
① プレビュー作成（世戸口 × Claude Code）
   - HP改修_seto_edit/ 配下のHTMLを編集
   - push → GitHub Pages（hp-preview）で宮澤さんが確認可能
       ↓
② 差分整理 → Issue コメント（世戸口）
   - 「プレビューのここが正。本番との差分はここ」を明記
   - hatena-pr の該当Issue にプレビューURL付きでコメント
       ↓
③ WP実装（宮澤）
   - プレビューを参考に homepage-wp テンプレートを更新
       ↓
④ 最終確認 & 本番push
```

---

## 📊 ページ別ステータス

### 事業部ページ（親ページ）

| # | ページ | プレビュー | 本番反映 | Issue | 次のアクション |
|---|--------|-----------|---------|-------|---------------|
| 1 | トップページ | ✅ 初版あり | 未着手 | [#22](https://github.com/HatenaBase/hatena-pr/issues/22) | 本番差分の洗い出し |
| 2 | 会計コンサルティング事業部 | ✅ 初版あり | 未着手 | [#23](https://github.com/HatenaBase/hatena-pr/issues/23) | 本番差分の洗い出し |
| 3 | 研修事業部 | ✅ 初版あり | 未着手 | [#24](https://github.com/HatenaBase/hatena-pr/issues/24) | リンク差し替え ← 今ここ |

### ソリューションLP

| # | LP名 | プレビュー | 本番反映 | Issue |
|---|------|-----------|---------|-------|
| 1 | 経理AX — BPO | ✅ 初版あり | 未着手 | [#13](https://github.com/HatenaBase/hatena-pr/issues/13) |
| 2 | 経理AX — Premium | ✅ 初版あり | 未着手 | [#18](https://github.com/HatenaBase/hatena-pr/issues/18) |
| 3 | 速習freee会計研修 | ✅ 初版あり | 未着手 | [#36](https://github.com/HatenaBase/hatena-pr/issues/36) |
| 4 | IPO支援 | ✅ 初版あり | 未着手 | [#16](https://github.com/HatenaBase/hatena-pr/issues/16) |
| 5 | 勘定奉行導入支援 | ✅ 初版あり | 未着手 | [#10](https://github.com/HatenaBase/hatena-pr/issues/10) |
| 6 | 研修候補者募集 | ✅ 初版あり | 未着手 | [#32](https://github.com/HatenaBase/hatena-pr/issues/32) |
| 7 | 研修派遣先募集 | ✅ 初版あり | 未着手 | [#33](https://github.com/HatenaBase/hatena-pr/issues/33) |
| 8 | Zencom | ✅ 初版あり | 未着手 | [#17](https://github.com/HatenaBase/hatena-pr/issues/17) |

---

## 📝 直近アクション

- [ ] 研修事業部ページのリンク差し替え（研修LP群への導線整備）
- [ ] 各ページの本番差分洗い出し → Issue コメント化
- [ ] 旧プレビューリポジトリ（training-preview / hatenabase-freee-training）のアーカイブ

---

## 🔗 リンク集

| 項目 | URL |
|------|-----|
| プレビュー一覧 | https://hatenabase.github.io/hp-preview/index.html |
| プレビューリポジトリ | https://github.com/HatenaBase/hp-preview |
| Epic Issue | https://github.com/HatenaBase/hatena-pr/issues/20 |
| 本番リポジトリ | https://github.com/HatenaBase/homepage-wp |
| 本プロジェクトフォルダ | `hatena-lp/HP改修_seto_edit/` |
