# TANAKA UO 公式サイト

WordPress と SWELL を使用して TANAKA UO のHPを作成する。

---

## Codex へ｜ここから読む

**実装の正は `docs/codex-implementation-brief.md`（v2.0）である。** これ以外の文書と食い違った場合は、必ずこちらを優先する。

| 順 | 読むもの | 内容 |
|---|---|---|
| 1 | [`docs/codex-implementation-brief.md`](docs/codex-implementation-brief.md) | **トップページの実装指示。まずこれを全文読む。** §0 破棄／§1 禁止事項12項目／書体／配色／ページ構成／確定原稿／素材／検証 |
| 2 | [`docs/codex-brief-hamayaki.md`](docs/codex-brief-hamayaki.md) | 浜焼きページの実装指示 |
| 3 | [`docs/codex-brief-products.md`](docs/codex-brief-products.md) | 商品・メニューページの実装指示。価格を持たない設計 |
| 4 | [`docs/seo-and-weekly-operations.md`](docs/seo-and-weekly-operations.md) | 構造化データ、title と description、内部リンク、週次運用 |
| 5 | [`docs/open-questions.md`](docs/open-questions.md) | **確認事項の統合と決着。未確定項目の扱いはここが正。** 各指示書の確認事項節より優先する |
| 6 | [`docs/wordpress-swell-migration.md`](docs/wordpress-swell-migration.md) | SWELL への移植手順 |
| 7 | [`docs/hp-requirements-checklist.md`](docs/hp-requirements-checklist.md) | 掲載項目の棚卸し。書体・配色は定義していない（1に委譲） |

### 着手前に必ず確認すること

- **§0 の「旧仕様の破棄」を読む。** 金茶 `#B0894E`、明朝の全面使用、写真に重ねる縦書きコピー、薄暮ダークのヒーロー、ロゴのプレート画像、見出しごとの小英字ラベル。これらは過去の指示書に書かれているが**すべて破棄されている**
- **名刺から採るのは、ワードマーク「TANAKA UO」の書体と、住所・連絡先の表記だけ。** 名刺の世界観（地色・文字色・補助色・欧文 Georgia）は移植しない
- **§1 の禁止事項12項目を守る。** 特に 11（一海および畑地優二に一切触れない）と 12（法人名に言及しない）は絶対
- 数字と英字は欧文フォントが受け持つ。和文の全角字形で出してはならない
- **未確定の項目を回答待ちにしない。** `docs/open-questions.md` §3 に全件の扱いが定めてある。**「確認中」「準備中」と書かず、欄ごと出さない**

### 着手を止める項目は無い

確認事項48件を統合し、28件を決着させ、残り23件にも「確定するまでの扱い」を定めた。
公開の直前にだけ、Googleビジネスプロフィールとの一致とドメインの向き先の2件を確認する。

**営業時間は確定している。** 店頭は金・土・日の 8:00-15:00。月曜から木曜は仕入れと加工にあて、店頭には立たない。
予約でのご注文は受ける。**「定休日」という語を使わない**（`docs/open-questions.md` §2-3-1）。

### 素材

| 場所 | 中身 |
|---|---|
| `site/media/ariake.mp4` | 有明海の映像。H.264、9.5MB |
| `site/images/` | 写真7点。用途と実寸は指示書 §5 の表を参照 |

写真は1枚につき1ページ。使い回さない。`mise.jpg` と `nodoguro.jpg` は浜焼きページの持ち分。

### 納品

`index.html` 単体。外部依存なし、Web フォントの読み込みなし。画像と映像は相対パス。
WordPress + SWELL への移植を前提とするため、フレームワークを挟まない素の HTML と CSS で書く。
実装後、指示書 §8 の検証項目を機械的に照合してから返すこと。

---

## 履歴（実装の参照先にしない）

`site-a/` `site-b/` `site-c/` は初期の3案。金茶・明朝・縦書きを含む旧路線であり、**現行仕様ではない**。検討の記録として残している。
