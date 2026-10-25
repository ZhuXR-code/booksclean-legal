# booksclean-legal

「文包整理清理助手」（Booksclean）公开法律文件托管仓库，用于向 Apple App Store、华为应用市场等渠道提供**公网可访问**的隐私政策与用户协议链接。

源码仓库为私有（`novel_files_clean`），本仓库**只存放**对外公示的静态文件，不含任何源码、密钥或配置。

## 文件

| 文件 | 说明 |
|---|---|
| `index.html` | 入口页，汇总各法律条款链接 |
| `privacy_policy.html` | 隐私政策（网页版，商店填写用） |
| `privacy_policy.txt` | 隐私政策（纯文本版） |
| `terms_of_use.html` | 用户协议（网页版） |
| `terms_of_use.txt` | 用户协议（纯文本版） |
| `terms_of_use_en.txt` | Terms of Use（英文纯文本） |
| `.nojekyll` | 关闭 Jekyll 处理，保证文件原样发布 |

## 公开地址

GitHub Pages（已启用，Source = `master` / `(root)`）：

- 入口页：https://zhuxr-code.github.io/booksclean-legal/
- 隐私政策：https://zhuxr-code.github.io/booksclean-legal/privacy_policy.html
- 用户协议：https://zhuxr-code.github.io/booksclean-legal/terms_of_use.html

备用 CDN（仓库公开即可取，国内一般可访问）：

- https://fastly.jsdelivr.net/gh/ZhuXR-code/booksclean-legal@master/privacy_policy.txt

> `raw.githubusercontent.com` 域名在中国大陆常被连接重置，不建议作为商店填写地址。

## 更新方式

本目录由私有源码仓库中的同名文件同步而来，不要直接在这里改正文：

1. 在 `novel_files_clean` 根目录修改 `privacy_policy.html` / `privacy_policy.txt` 等文件并提交；
2. 执行仓库根目录的 `sync_legal_site.ps1` 完成同步；
3. 在 `legal_site` 目录内提交并推送到 `booksclean-legal` 仓库的 `master`；
4. GitHub Pages 约 1～2 分钟后自动生效。

> 注意：`booksclean-legal` 仓库必须保持 **public**，否则 GitHub Pages 与 raw 直链都会返回 404。
