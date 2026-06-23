# 神様のメモ帳 公式サイト Docker デプロイ手順

> **管理**: deploy/  
> **更新**: 2026-06-23

---

## 日本語

### 起動

```bash
cd deploy
docker compose up -d
# → http://localhost:8080
```

### 停止

```bash
cd deploy
docker compose down
```

### イメージ情報

- イメージ名: `kamimemo-archive:latest`
- ベース: `nginx:alpine`
- ディスク容量: 約 67MB (展開時)
- 公開ポート: 8080 → コンテナ内 80

### 別マシンへの移行

```bash
# エクスポート
docker save kamimemo-archive:latest | gzip > kamimemo-archive.tar.gz

# インポート先で
gunzip -c kamimemo-archive.tar.gz | docker load
cd deploy && docker compose up -d
```

---

## 中文

### 启动

```bash
cd deploy
docker compose up -d
# → http://localhost:8080
```

### 停止

```bash
cd deploy
docker compose down
```

### 镜像信息

- 镜像名: `kamimemo-archive:latest`
- 基础: `nginx:alpine`
- 磁盘: 约 67MB (展开)
- 端口: 8080 → 容器内 80

### 迁移到其他机器

```bash
# 导出
docker save kamimemo-archive:latest | gzip > kamimemo-archive.tar.gz

# 目标机器导入
gunzip -c kamimemo-archive.tar.gz | docker load
cd deploy && docker compose up -d
```

---

## English

### Start

```bash
cd deploy
docker compose up -d
# → http://localhost:8080
```

### Stop

```bash
cd deploy
docker compose down
```

### Image Info

- Image: `kamimemo-archive:latest`
- Base: `nginx:alpine`
- Size: ~67MB (unpacked)
- Port: 8080 → container 80

### Migration

```bash
# Export
docker save kamimemo-archive:latest | gzip > kamimemo-archive.tar.gz

# Import on target machine
gunzip -c kamimemo-archive.tar.gz | docker load
cd deploy && docker compose up -d
```

---

## 備考 / Notes

- サイトは完全オフライン対応。起動にインターネット接続は不要。
- 全コンテンツの著作権は原作者・権利者に帰属。
