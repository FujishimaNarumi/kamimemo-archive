# 镜像差异报告

> 生成日期: 2026-06-23
> 工具: wget 1.25.0 vs HTTrack 3.49.2

## 1. 总览

| 指标 | wget | HTTrack |
|------|------|---------|
| 总文件数 | 502 | 523* |
| 总大小 | 6.8 MB | 7.9 MB |
| HTML 文件 | 60 | 84* |
| 运行时间 | ~10min | ~8min38s |
| 错误 | 0 | 21 (404) |

\* HTTrack 计数包含 hts-cache 文件和外部域名文件(animate.co.jp)

## 2. 差异分析

wget 多捕获的文件（部分）:
- news/hp0001/index00160000.html 等更多新闻文章
- 更多 core_sys CSS 子文件

HTTrack 额外捕获:
- hts-cache/ 日志文件
- 外部 animate.co.jp 链接页面（非本站内容）
- 部分来自 PHP 分页的页面

## 3. 关键发现

- **字符集**: UTF-8
- **外部引用**: Twitter (platform.twitter.com), Google AJAX (jquery.com), animate.co.jp
- **缺失资源**: 21 张角色按钮图片返回 404 (bt_chara12.jpg ~ bt_chara16.jpg 等)
- **流媒体**: 4 个 .asx 引用指向 WB 服务器（可能已离线）
- **动态内容**: Character 页面使用 PHP 分页 (index.php?No=8&page=N)

## 4. 结论

wget 在覆盖率上略优（捕获了更多新闻文章和 CSS 变体）。
HTTrack 更好处理了外部链接和外链页面。
两者结合可达到最大覆盖率。
建议以 wget 镜像为主要基础，补充 HTTrack 额外捕获的资源。
