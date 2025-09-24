# gemholm — Single-Page Paper/Project (Jekyll)

一页式论文/项目展示模板：Hero 轮播、Abstract / Background / Approach / Results / Societal Impact 分区，轻量灯箱与手写体（Patrick Hand + 中文）。

## Quick Start
```bash
# 需要 Ruby + Bundler
bundle install
bundle exec jekyll serve --livereload

```

Edit Content

站点信息：_config.yml（title / description / links.*）

首页结构：index.html

分区文案：_includes/sections/{abstract,background,approach,results,impact}.md

轮播：_data/hero.yml（图片放 assets/images/hero/）


结果区：


卡片模式：配置 items 列表

颜色/排版：assets/css/styles.scss（二级标题大小见末尾 .section h2.hand-title）


Credits / 致谢

Demo references: Ashish Vaswani et al., Attention Is All You Need, NeurIPS 2017.
We link to the original paper only; any reproduced tables/figures follow the permission note in the PDF (attribution required; journalistic or scholarly use). All rights remain with the original authors/organizations.