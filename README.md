[README.md](https://github.com/user-attachments/files/28682787/README.md)
# Kaeya Literature Radar

这是一个面向经济学、金融学和管理学文献泛读的 GitHub Pages 网页。

当前版本已经改成数据驱动结构：网页负责展示，文献数据放在 JSON 文件里。后续 Codex 自动化只需要每天更新 JSON，GitHub Pages 会自动发布最新网页。

## 文件结构

```text
web/index.html
web/data/latest.json
web/data/runs.json
web/data/archive/2026-06-07.json
config/interests.json
.github/workflows/pages.yml
```

## 数据更新方式

网页默认读取：

```text
web/data/latest.json
```

如果这个文件暂时读取失败，网页会退回到 HTML 内置的示例数据，避免页面空白。

每天自动化应该更新：

```text
web/data/latest.json
web/data/archive/YYYY-MM-DD.json
web/data/runs.json
```

## GitHub Pages

GitHub Pages 地址：

```text
https://kaeya0227.github.io/kaeya/
```

仓库设置应为：

```text
Settings -> Pages -> Source -> GitHub Actions
```

## Codex 自动化目标

每天上午 9 点，Codex 自动化应：

1. 检索 NBER、SSRN、arXiv、英文期刊、中文期刊等来源。
2. 筛选约 20 篇经济学、金融学、管理学相关论文。
3. 生成中文文献卡片，包括研究问题、背景动机、创新之处、机制、数据方法、主要发现、相关性和精读优先级。
4. 不编造论文、作者、链接、摘要或结论。
5. 只更新 `web/data/*.json`。

## 版权提示

如果后续加入凯亚主题，公开网页建议优先使用抽象冰元素、冰神之眼风格、深蓝银白色系和自制/授权图片，不直接使用未授权角色立绘。
