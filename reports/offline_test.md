# オフラインテスト報告書 / Offline Test Report

> 作成日: 2026-06-23  
> 確認者: automated

## テスト対象 / Test Targets

| セクション | パス | ステータス |
|---|---|---|
| トップページ / Top | `index.html` | ✓ (509 files, 6.8MB) |
| News / ニュース | `news/hp0001/` | ✓ (29 articles) |
| Character / キャラクター | `contents/hp0004/` | ✓ (11 pages) |
| Story / ストーリー | `contents/hp0006/` | ✓ (13 pages) |
| Goods / グッズ | `contents/hp0009/` | ✓ (1 page) |
| Web Radio / webラジオ | `radio/` | ✓ (1 page) |
| Introduction | `contents/hp0003/` | ✓ (1 page) |
| Staff & Cast | `contents/hp0005/` | ✓ (1 page) |

## 検証結果 / Results

- 全ページの内部リンクは相対パスで構成されており、オフラインでも正常動作
- 外部依存 (Twitter, Google jQuery, animate.co.jp) は除去済み
- 全 CSS, JS, 画像ファイルはローカルに保持
- Docker 起動確認: nginx:alpine 上で HTTP 200 を確認
- アーカイブ整合性: `SHA256SUMS` で全ファイル検証可能
