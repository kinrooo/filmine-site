# filmine-site

Filmine 的公开页面(App Store Connect 提审必填的两个 URL)。

| ASC 字段 | 页面 |
|---|---|
| 隐私政策 URL | https://kinrooo.github.io/filmine-site/privacy.html |
| 支持 URL | https://kinrooo.github.io/filmine-site/support.html |

## ⚠️ 不要在这个仓库里直接改 HTML

本仓是**派生产物**。唯一事实源(SoT)是主仓 `kinrooo/ilive` 的 `docs/site/`:

- `docs/site/privacy.html`
- `docs/site/support.html`

`index.html` / `.nojekyll` / 本 README 由主仓的
`collab/tools/publish_site.sh` 生成。在这里直接改的任何内容,下一次 stage 都会被
覆盖。

## 改文案的正确流程

1. 在主仓改 `docs/site/*.html`(隐私政策须遵守主仓 `docs/site/README.md`
   的三副本纪律:App 内 `PrivacyView.swift` / 本页 / ASC App Privacy 问卷)
2. 在主仓跑 `./collab/tools/publish_site.sh`(stage 模式)
3. 回到本仓 `git add -A && git commit && git push`,Pages 自动重新发布
