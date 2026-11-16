# Fan Yundi 个人学术主页：Agent 工作指令

本文件是后续 agent 的唯一交接文档。不要假设能够读取此前的对话；开始工作前必须完整阅读本文件。用户通常用中文提出需求，但网站公开内容默认使用英文。

## 1. 项目固定信息

- 网站所有者：Fan Yundi。
- GitHub 用户：`Peau-Vae`。
- 正式网站：https://peau-vae.github.io/
- 源仓库：https://github.com/Peau-Vae/Peau-Vae.github.io
- 分支：`master`。
- GitHub Pages：legacy 原生构建，发布 `master` 分支根目录，不使用 GitHub Actions。
- 本地工作目录：`/mnt/agents/output/app`。该目录可能没有 `.git`，不要因此重新初始化网站或覆盖文件。
- 网站模板：Academic Pages，Jekyll + Liquid + Markdown + Sass。
- 网站语言：英文。用户给出的中文简介、游记说明或课程说明，需要忠实、自然地翻译成英文，不要擅自增加事实。
- 风格：简洁学术风。除非用户明确要求，不要 redesign，不要更换模板、配色、字体或导航结构。

## 2. 开始任何修改前必须做的事

1. 重新检查 `/mnt/agents/output/app`、用户上传目录和远端 `master`，不要依赖旧的文件列表或旧 commit。
2. 用户上传文件通常位于 `/mnt/agents/temp/`；项目共享文件可能位于 `/mnt/agents/upload/`。文件名可能含空格，命令中必须正确引用路径。
3. 远端仓库是部署事实来源。用户可能直接在 GitHub 网页上修改文件，尤其是 `_pages/about.md`。
4. 推送前若远端有新 commit，先 `fetch`，再 merge 或 rebase；保留用户远端修改，禁止强推覆盖。
5. 不要接收或索取 GitHub 密码，不要把 token、cookie、凭据或设备授权日志写进仓库、回复或本文件。

## 3. 当前网站状态，不要误判为故障

- 首页姓名：Fan Yundi。
- 首页引言：`Wir müssen wissen, wir werden wissen.`。
- 首页身份：year 1 MPhil student at IMS, CUHK。
- 左侧资料：Hong Kong；Hometown: Shanghai；IMS, CUHK；Email；GitHub；Zhihu。
- 公开邮箱：`ydfan@math.cuhk.edu.hk`。
- 知乎：https://www.zhihu.com/people/hao_hai_zi
- 头像：`images/profile.jpg`，应保持彩色。不要重新加入 `filter: grayscale(...)`。
- 名字下方的旧 bio 已按用户要求删除，不要自行补回。
- Publications、Activities、CV 当前只有页面标题，没有正文或条目。这是用户要求的“清空”，不是构建失败。
- Travel 现有四篇游记（原始 PDF 直接发布，未经降质，位于 `files/travel/`），后续添加内容时不要删除：

| 标题 | Markdown 条目 | PDF |
|---|---|---|
| Yuen Long: Shap Pat Heung and Pat Heung | `_portfolio/2024-12-20-yuen-long-shap-pat-heung.md` | `files/travel/yuen-long-shap-pat-heung-pat-heung-2024-12-20.pdf` |
| Yuen Long: Tai Tong and Tung Shing Lei | `_portfolio/2024-12-23-yuen-long-tai-tong.md` | `files/travel/yuen-long-tai-tong-tung-shing-lei-2024-12-23.pdf` |
| Tai Po: Tai Mei Tuk | `_portfolio/2024-12-25-tai-po-tai-mei-tuk.md` | `files/travel/tai-po-tai-mei-tuk-2024-12-25.pdf` |
| Tai Po: Lam Tsuen | `_portfolio/2025-01-25-tai-po-lam-tsuen.md` | `files/travel/tai-po-lam-tsuen-2025-01-25.pdf` |
| Fuzhou（一个帖子含三份 PDF：闽江夜色、石厝教堂前的卖柑人、乌山） | `_portfolio/2025-02-01-fuzhou.md` | `files/travel/fuzhou-minjiang-night-2025-02-01.pdf`、`files/travel/fuzhou-orange-seller-stone-church-2025-02-01.pdf`、`files/travel/fuzhou-wu-hill-2025-02-01.pdf` |
| Lai Chi Wo | `_portfolio/2025-02-23-lai-chi-wo.md` | `files/travel/lai-chi-wo-2025-02-23.pdf` |
| Kaiping: A Journey Out of Order | `_portfolio/2025-10-06-kaiping.md` | `files/travel/kaiping-2025-10-06.pdf`（约 65 MB，原始质量直接发布） |

Activities 现有两个讨论班帖子，PDF 位于 `files/activities/`，后续添加时不要删除：

| 标题 | Markdown 条目 | PDF |
|---|---|---|
| Heat Kernel and Dirac Operator Seminar | `_talks/2026-05-18-heat-kernel-dirac-operator-seminar.md` | `files/activities/heat-kernel-local-index-seminar-poster.pdf`、`heat-kernel-seminar-iii-clifford-module-dirac-operator.pdf`、`heat-kernel-seminar-vi-equivariant-local-index.pdf` |
| Spectral Sequence Seminar | `_talks/2026-08-01-spectral-sequence-seminar.md` | `files/activities/spectral-sequence-seminar-iii-morse-homology.pdf` |

Teaching 页面当前内容：2026 Spring, TA of MMAT5350 Coding Theory。
- 首页 Explore 链接仍然保留，指向上述页面和 Notes。

顶部导航固定为五项：

| 导航 | 页面文件 | 内容来源 |
|---|---|---|
| Notes | `_pages/year-archive.html` | `_posts/` |
| Publications | `_pages/publications.html` | `_publications/` |
| Travel | `_pages/portfolio.html` | `_portfolio/` |
| Activities | `_pages/talks.html` | `_talks/` |
| Teaching | `_pages/teaching.md` | 直接编辑该页面（普通文字页面，不用帖文模式） |
| CV | `_pages/cv.md` | 直接编辑该页面 |

当前 Notes 有六份 PDF。后续添加内容时不要删除它们：

| 标题 | Markdown 条目 | PDF |
|---|---|---|
| Geometric Quantization | `_posts/2026-06-17-geometric-quantization.md` | `files/notes/geometric-quantization.pdf` |
| MATH4080 Modules and Group Representation | `_posts/2026-05-03-math4080-modules-and-group-representation.md` | `files/notes/math4080-modules-and-group-representation.pdf` |
| MATH5051 Abstract Algebra I: Commutative Algebra Notes | `_posts/2026-02-11-math5051-commutative-algebra-notes.md` | `files/notes/math5051-commutative-algebra-notes.pdf` |
| Complex Morse Theory | `_posts/2025-06-16-complex-morse-theory.md` | `files/notes/complex-morse-theory.pdf` |
| Morse Theory, by Milnor | `_posts/2024-11-15-morse-theory-by-milnor.md` | `files/notes/morse-theory-by-milnor.pdf` |
| Generalization of Optional 7 in MATH3030 Homework 2 | `_posts/2024-11-15-math3030-homework-reflections.md` | `files/notes/math3030-homework-2-optional-7.pdf` |

每次增删内容后，如本表已过时，应同步更新本文件。

## 4. 添加普通 PDF 笔记的标准流程

1. 检查 PDF 是否真实存在、能否解析、页数和文件大小：

   ```bash
   pdfinfo "输入文件.pdf"
   ls -lh "输入文件.pdf"
   ```

2. 如用户没有指定标题，先读 PDF 首页，优先采用文件原有标题或课程信息；不要编造标题、日期、教师、学校或项目背景。
3. 日期优先采用用户明确给出的日期；没有时可用 PDF 的可靠创作日期。不要虚构月份或日期。
4. 将原 PDF 复制到 `files/notes/`，文件名用小写 ASCII 和连字符，例如：

   ```text
   files/notes/math5051-commutative-algebra-notes.pdf
   ```

5. 在 `_posts/` 新建对应 Markdown，文件名格式为 `YYYY-MM-DD-short-title.md`。
6. 条目应包含：英文标题、日期、英文简介、列表中的 PDF 链接、详情页中的阅读或下载链接。
7. 简介较长时可使用 YAML block scalar，保留编号列表。模板如下：

   ```markdown
   ---
   title: "English Title"
   date: 2026-01-31
   excerpt: |-
     First English paragraph.

     The main topics were:

     1. First topic.
     2. Second topic.

     Closing paragraph. [PDF](/files/notes/example.pdf).
   ---

   First English paragraph.

   The main topics were:

   1. First topic.
   2. Second topic.

   Closing paragraph.

   [Read or download the PDF](/files/notes/example.pdf).
   ```

8. 数学记号保留原义。Hilbert's Nullstellensatz、Krull/Chevalley/Samuel dimension、PID、G-module 等术语不要误译或随意改写。
9. 人名以 PDF 首页或用户明确写法为准；现有课程笔记使用 `Prof. Jiu Kang Yu`。
10. 构建后检查 Notes 列表、编号列表、详情页和所有 PDF 链接，不能只检查 Markdown 源文件。

## 5. 图片与 PDF 画质红线

用户明确要求：可以优化图片或 PDF，但不得损害画质。

1. 原始上传文件必须保持不变；优化时另存为新文件，不能覆盖唯一原件。
2. 禁止为了减小体积而执行以下操作：
   - 降低图片分辨率、DPI 或像素尺寸；
   - 降低 JPEG quality，或有损重压缩图片；
   - 转灰度、去色、降低色深；
   - 模糊、锐化、加水印或改变图片内容；
   - 删除图片、页面、字体或公式；
   - 将整页重新栅格化为低分辨率图片。
3. 不要直接套用 Ghostscript 的 `/screen`、`/ebook` 等预设，也不要运行会自动 downsample 的“PDF 压缩”命令。
4. 网页缩略图可以单独生成，但原始 PDF 和原始图片必须保留；缩略图不能替代原文件下载。
5. PNG 只允许 `optipng`、`zopflipng` 等无损优化，优化后必须确认解码像素完全一致；不要使用有损的 `pngquant`。
6. JPEG 只允许 `jpegtran -optimize -copy all` 这类不重编码像素的无损优化；不得通过降低 quality 来缩小文件，EXIF 和版权元数据也应保留。
7. 若只能依靠有损压缩才能满足体积要求，不要擅自降质。改用第 6 节的大文件发布方案。

## 6. PDF 太大时的处理顺序

GitHub 限制可能调整，遇到大文件时应先核对官方最新文档。当前已知规则：普通 Git 文件超过 50 MiB 会警告，超过 100 MiB 会被拒绝；GitHub Pages 发布站点上限为 1 GB，构建超时为 10 分钟。

按以下顺序处理：

### A. 先测量，不要猜测

```bash
ls -lh "document.pdf"
pdfinfo "document.pdf"
pdfimages -list "document.pdf"
du -sh /mnt/agents/output/app/files
```

`pdfimages -list` 只用于分析，不要为了压缩而提取并重写图片。

### B. 体积合适时直接上传原文件

- 几十 MB 的 PDF 带图片并不必然失败。
- 只要单文件、仓库和 Pages 均在限制内，可以直接提交原始 PDF。
- 文件较大主要影响上传、构建和访客下载速度，不等于内容有问题。

### C. 先尝试可验证的无损优化

只允许无损压缩 PDF 内部流，例如 `qpdf` 的流压缩和 object streams：

```bash
qpdf "input.pdf" \
  --stream-data=compress \
  --recompress-flate \
  --compression-level=9 \
  --object-streams=generate \
  "output.optimized.pdf"
qpdf --check "output.optimized.pdf"
```

无损优化后必须同时满足：

1. `qpdf --check` 通过；
2. 页数、页面尺寸、文字、公式、图片数量与原件一致；
3. 用同一渲染器和同一 DPI 渲染优化前后的全部页面，逐页进行像素级比较，结果必须一致；若有差异，丢弃优化版本；
4. 优化文件确实更小，否则删除优化版本，继续使用原件；
5. 不要把 `qpdf --linearize` 当作缩小体积的手段；它只改善网络分段读取，不改变画质。

如果无损优化效果很小，这是正常现象，尤其是 PDF 内已经包含 JPEG/JPX 图片时。不得转而使用有损压缩。

### D. 单文件超过普通 Git 限制时，保留原文件并改用 GitHub Release

1. 不要把超限文件强行加入 Git，不要反复尝试绕过限制。
2. 不要把 Git LFS 当作 GitHub Pages 的直接发布方案；LFS pointer 不是访客可阅读的 PDF。
3. 将未经降质的原始 PDF 上传为 GitHub Release asset，再在笔记或游记页面链接该 asset。
4. 每个文件名必须唯一，不要使用 `--clobber` 覆盖旧资料。
5. Release 单 asset 也有大小上限，操作前核对 GitHub 最新限制。

示例流程：

```bash
gh release create "large-files" \
  -t "Original documents" \
  -n "Original-quality files for the academic website." \
  --repo Peau-Vae/Peau-Vae.github.io

gh release upload "large-files" \
  "document.pdf#Original PDF" \
  --repo Peau-Vae/Peau-Vae.github.io
```

如果 `large-files` Release 已存在，只执行 `gh release upload`，不要重复创建。网页中的链接形如：

```markdown
[Read or download the original PDF](https://github.com/Peau-Vae/Peau-Vae.github.io/releases/download/large-files/document.pdf)
```

发布前必须检查最终链接能下载到完整文件，且文件大小与原件一致。

### E. 超过 Release 限制或不适合 Release 时

1. 向用户说明实际文件大小和命中的具体限制，不要笼统声称“发布失败”。
2. 可建议使用用户认可的外部对象存储或云盘，并在网站放原文件链接。
3. 若用户同意按章节或页码拆分，可用 `qpdf`/`pikepdf` 按页拆分，不重渲染、不重压缩图片；每份拆分文件仍需验证。
4. 未经用户同意，不要拆书、删页或改变阅读顺序。

## 7. 其他内容类型的更新方式

- 游记：放入 `_portfolio/`，页面 URL 为 `/travel/...`。照片放在 `images/` 或合适的静态目录，正文使用相对路径引用。
- 论文：放入 `_publications/`，不要编造期刊、arXiv、DOI 或发表状态。
- 活动：放入 `_talks/`，页面 URL 为 `/activities/...`。
- CV：直接编辑 `_pages/cv.md`；当前为空是刻意的，收到真实经历后再添加。
- 首页和左侧资料：分别编辑 `_pages/about.md`、`_config.yml` 和 `_includes/author-profile.html`。
- 不要恢复已删除的 sample 文章、示例论文、示例游记、示例活动或模板 CV。

## 8. 本地构建规则

1. 修改后必须运行完整构建：

   ```bash
   cd /mnt/agents/output/app
   npm run build
   ```

2. 构建产物在 `dist/`，必须生成 `dist/index.html`。
3. 如果缺少 npm 依赖，先运行 `npm install`。
4. 如果缺少 Jekyll，可安装此前使用过的 Debian 包：

   ```bash
   apt-get update
   apt-get install -y jekyll \
     ruby-jekyll-gist ruby-jekyll-paginate \
     ruby-jekyll-sitemap ruby-jekyll-redirect-from \
     ruby-jekyll-include-cache
   ```

5. `assets/css/main.css` 是由 `assets/css/main.scss` 生成并提交的；修改样式源文件后必须重新构建并提交生成后的 CSS。
6. `assets/js/main.min.js` 也必须存在于仓库中，因为 Pages 原生构建不会替我们执行 npm 编译。
7. `_config_preview.yml` 只用于本地预览；GitHub Pages 使用 `_config.yml`。
8. 根目录 `index.html` 是本地预览生成的入口，已被 Git 和 Jekyll 排除，不要把它当作源文件编辑。
9. 不要通过削弱或替换 build script 来绕过构建错误；应修复真正的依赖、源文件或配置问题。
10. `AGENTS.md` 已加入 Jekyll exclude，只保留在仓库，不应作为公开网页发布。

## 9. 本地验收清单

每次内容更新至少检查：

- `npm run build` 成功；
- 新标题和英文简介与用户提供的信息一致；
- 长简介中的编号列表实际渲染为列表；
- PDF 链接返回 HTTP 200；
- 直接存放在 Pages 的 PDF 返回 `Content-Type: application/pdf`；
- PDF 的 `Content-Length` 与本地文件大小一致；
- Publications、Activities、CV 仍保持用户要求的空白状态，Travel 保留现有四篇游记，除非本轮明确要求增删；
- 桌面约 1440px 和手机约 375px 均无横向溢出；
- 浏览器控制台无错误；
- 头像保持彩色且能正常加载。

可使用本地静态服务器检查：

```bash
cd /mnt/agents/output/app/dist
python3 -m http.server 4000
```

网络不稳定时，完整下载 PDF 可能超时；可再用 HEAD 请求核对状态、类型和文件大小，但不能因此跳过线上链接检查。

## 10. GitHub 授权与安全

1. 先运行：

   ```bash
   gh auth status
   ```

2. 未登录时，使用 GitHub 官方 device authorization，让用户自己在浏览器确认。不要索要密码或 token。
3. 授权进程必须持续等待用户确认，不要设置会自动终止并刷新验证码的短 timeout。
4. 若网络握手失败，可重试获取 device code；给出新验证码后，旧验证码作废时不要继续轮询旧进程。
5. 登录成功后运行：

   ```bash
   gh auth setup-git
   ```

6. 当前授权通常只有 `repo` 等 scope，没有 `workflow`。不要上传 `.github/workflows`，也不要为此索取更大权限；继续使用 Pages legacy 原生构建。
7. 日志和回复中不得显示访问 token。设备 code 可以临时提供给用户用于授权，但不要写入仓库。

## 11. 部署流程

1. 优先使用新鲜 clone，或在已有工作 clone 中先获取远端：

   ```bash
   git -c http.version=HTTP/1.1 clone \
     --branch master --single-branch \
     https://github.com/Peau-Vae/Peau-Vae.github.io.git \
     /tmp/homepage-deploy
   ```

2. 只复制本轮有意修改的源文件和静态文件，检查：

   ```bash
   git -C /tmp/homepage-deploy status --short
   git -C /tmp/homepage-deploy diff
   ```

3. 不要误提交 `node_modules`、`dist`、本地缓存、授权日志或临时截图。
4. 提交信息使用简短英文，例如：

   ```bash
   git add -A
   git commit -m "Add new mathematical notes"
   ```

5. 推送遇到 TLS 问题时可用 HTTP/1.1 重试：

   ```bash
   git -c http.version=HTTP/1.1 push origin master
   ```

6. 若 push 被拒绝，因为远端有用户的新修改：
   - 先 `git fetch origin master`；
   - 查看本地和远端差异；
   - 用 merge 或 rebase 集成；
   - 保留用户的远端修改；
   - 禁止 `git push --force`。
7. 推送后等待 Pages 构建，并确认 build 的 commit 就是本轮 commit：

   ```bash
   gh api repos/Peau-Vae/Peau-Vae.github.io/pages/builds/latest
   ```

8. 只有最新 build 状态为 `built` 后，才进行正式网站验收。构建为 `error` 时先读取错误并修复，不要声称已上线。

## 12. Kimi 预览版本

本地构建和验收通过后，可保存 Kimi 网站预览版本：

- `project_dir`：`/mnt/agents/output/app`
- `type`：`static`
- `artifact_type`：`landing_page`
- `default_view`：`desktop`
- `message`：简短中文标题，例如“新增三份课程学习笔记”

Kimi 预览版本与 GitHub Pages 正式部署是两套机制。保存预览版本不等于发布；正式网站是否更新必须以 GitHub push、Pages build 和线上验收为准。

## 13. 常见网络问题

- GitHub clone/push 偶发 TLS handshake 错误：使用 HTTP/1.1，有限次数重试。
- `gh auth login` 获取 device code 偶发超时或 EOF：持续重试，但一旦显示验证码，就让该进程继续等待用户确认。
- GitHub Pages 刚 push 后返回旧内容：先检查 latest build 的 commit 和状态，不要立即重复推送。
- 截图等待外部字体可能超时：这不自动等于网站失败，应分别检查正文、资源、控制台和实际链接。

## 14. 完成回复应报告什么

完成后用中文简洁报告：

1. 修改了哪些页面或新增了哪些文件；
2. 正式网站或 Notes 的链接；
3. 是否完成桌面、手机、链接和 Pages 构建检查；
4. 若使用 Release 或外部存储，明确说明原 PDF 未经降质，并给出下载入口；
5. 若有任何未完成或受阻事项，直接说明，不要把本地上传成功描述成已经上线。

## 15. 最重要的十条禁令

1. 不要索取密码或访问 token。
2. 不要强推覆盖用户在 GitHub 上的新修改。
3. 不要损害图片或 PDF 画质。
4. 不要把大文件有损压缩当成默认解决方案。
5. 不要恢复模板示例或空白页面的旧占位文字。
6. 不要把头像变回黑白。
7. 不要编造标题、日期、论文、活动、学历或研究经历。
8. 不要绕过失败的构建却仍声称完成。
9. 不要把 Kimi 预览说成 GitHub 正式发布。
10. 不要让本文件过时：改变网站结构、部署方式或大文件策略后，必须同步更新 `AGENTS.md`。
