# 神様のメモ帳 公式サイト 完全アーカイブ

> **管理者**: Fujishima Narumi  
> **作成日**: 2026-06-23  
> **更新日**: 2026-06-23  
> **元URL**: `https://wwws.warnerbros.co.jp/anime/kamimemo/`  
> **ハッシュ**: `SHA256SUMS` 参照

---

## 日本語

TVアニメ「神様のメモ帳」(Heaven's Memo Pad, 2011年7月-9月放送) の公式サイトを完全にローカルへミラーしたアーカイブです。  
サーバがいつ停止しても閲覧可能なよう、全ページ・全アセットを保存し、オフラインでも完全に動作する状態にしています。

### 収録内容

| ディレクトリ | 説明 | サイズ |
|---|---|---|
| `restored_site/` | 完全オフライン復元サイト（nginx で配信可） | 6.8MB / 509 files |
| `museum/` | 画像博物館（216枚、カテゴリ分類済み） | 2.3MB |
| `archive/raw_httrack/` | HTTrack による生ミラー | 7.9MB |
| `archive/raw_wget/` | wget --mirror による生ミラー | 6.8MB |
| `archive/content/` | セクション別に整理した HTML+JSON | 1.2MB |
| `reports/` | 解析レポート（サイトマップ、差分、復旧記録等） | 9 files |
| `deploy/` | Docker デプロイ設定 | 3 files |
| `kamimemo_official_archive.tar.zst` | 長期保存アーカイブ（Zstandard圧縮） | 9.5MB |

### 収録セクション一覧

- トップページ (`index.html`)
- Introduction / 作品紹介 (`contents/hp0003/`)
- Character / キャラクター (`contents/hp0004/`) — 全11ページ
- Staff & Cast / スタッフ・キャスト (`contents/hp0005/`)
- Story / ストーリー (`contents/hp0006/`) — 全12話 + 一覧
- Blu-ray & DVD / グッズ (`contents/hp0009/`)
- CD (`contents/hp0010/`)
- Book (`contents/hp0011/`)
- News / ニュース (`news/hp0001/`) — 32記事
- Web Radio / webラジオ (`radio/`)

### 動作確認

```bash
# オプションA: ブラウザで直接開く
open restored_site/index.html

# オプションB: Docker で起動（推奨）
cd deploy && docker compose up -d
open http://localhost:8080
```

### ファイル構成

```
kamimemo-archive/
├── archive/
│   ├── raw_httrack/       ← HTTrack 一次データ
│   ├── raw_wget/          ← wget 一次データ
│   ├── recovered_assets/  ← 後日発見・追加取得したアセット
│   └── content/           ← セクション別アーカイブ
├── restored_site/          ← 復元済みオフラインサイト
├── museum/                 ← 画像博物館
├── evidence/               ← 証拠保全
├── reports/                ← レポート類
├── deploy/                 ← Docker 設定
├── Dockerfile
├── SHA256SUMS
├── manifest.json
└── kamimemo_official_archive.tar.zst
```

---

## 中文

TV 动画《神的记事本》（Heaven's Memo Pad，2011年7月-9月播出）官方网站完整本地镜像档案。  
为防止官网下线后无法访问，已保存全部页面与资源，可完全离线运行。

### 内容收录

| 目录 | 说明 | 大小 |
|---|---|---|
| `restored_site/` | 完全离线版网站（可用 nginx 部署） | 6.8MB / 509 files |
| `museum/` | 图片博物馆（216张，已分类） | 2.3MB |
| `archive/raw_httrack/` | HTTrack 原始镜像 | 7.9MB |
| `archive/raw_wget/` | wget --mirror 原始镜像 | 6.8MB |
| `archive/content/` | 按栏目整理的 HTML+JSON | 1.2MB |
| `reports/` | 分析报告（站点地图、差异、恢复记录等） | 9 files |
| `deploy/` | Docker 部署配置 | 3 files |
| `kamimemo_official_archive.tar.zst` | 长期保存压缩包 | 9.5MB |

### 收录栏目

- 首页
- Introduction / 作品介绍
- Character / 角色（全11页）
- Staff & Cast / 制作人员
- Story / 故事（全12话 + 列表）
- Blu-ray & DVD / 商品
- CD
- Book
- News / 新闻（32条）
- Web Radio / 网络广播

### 使用方法

```bash
# 方式A: 直接浏览器打开
open restored_site/index.html

# 方式B: Docker 一键启动（推荐）
cd deploy && docker compose up -d
open http://localhost:8080
```

---

## English

Complete offline mirror of the TV anime "Heaven's Memo Pad" (Kamisama no Memochou, 2011) official website.  
All pages and assets have been preserved for offline browsing, independent of the original Warner Bros server.

### Contents

| Directory | Description | Size |
|---|---|---|
| `restored_site/` | Fully restored offline site | 6.8MB / 509 files |
| `museum/` | Image museum (216 images, categorized) | 2.3MB |
| `archive/raw_httrack/` | HTTrack raw mirror | 7.9MB |
| `archive/raw_wget/` | wget --mirror raw mirror | 6.8MB |
| `archive/content/` | Section-organized HTML+JSON | 1.2MB |
| `reports/` | Analysis reports (sitemap, diff, recovery) | 9 files |
| `deploy/` | Docker deployment config | 3 files |
| `kamimemo_official_archive.tar.zst` | Long-term preservation archive | 9.5MB |

### Sections

- Top Page
- Introduction
- Character (11 pages)
- Staff & Cast
- Story (12 episodes + listing)
- Blu-ray & DVD (Goods)
- CD
- Book
- News (32 articles)
- Web Radio

### Quick Start

```bash
# Option A: Open directly in browser
open restored_site/index.html

# Option B: Docker (recommended)
cd deploy && docker compose up -d
open http://localhost:8080
```

---

## 更新履歴 / Changelog

| 日付 | 内容 |
|---|---|
| 2026-06-23 | 初版作成。wget + HTTrack による全サイトミラー完了。オフライン復元・全レポート生成・Dockerデプロイ対応。 |

## ライセンス / License

本アーカイブはファンによる保存目的で作成されました。  
This archive is created by a fan for preservation purposes.  
所有内容的版权归原作者及版权方所有。
