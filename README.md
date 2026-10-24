<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=30&pause=1200&color=F26B3A&center=true&vCenter=true&random=false&width=760&lines=Hi%2C+I%27m+Jay+%F0%9F%91%8B;Write+C%2C+ship+with+Python+%F0%9F%90%8D;%E6%8A%8A%E6%83%B3%E6%B3%95%E5%86%99%E6%88%90%E8%83%BD%E8%B7%91%E7%9A%84%E4%B8%9C%E8%A5%BF+%E2%9C%A8;Keep+Learning+%F0%9F%93%9A" alt="Typing SVG" />

**计算机科学与技术 · 从命令行小工具写到带后台的整站**

<a href="https://github.com/sheephearttidy">
  <img src="https://img.shields.io/badge/GitHub-sheephearttidy-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
</a>
<img src="https://img.shields.io/badge/Focus-C%20%7C%20Python%20%7C%20Web-orange?style=for-the-badge" alt="Focus" />
<img src="https://komarev.com/ghpvc/?username=sheephearttidy&label=Profile%20Views&color=F74700&style=flat-square" alt="Profile views" />

</div>

---

## 👋 关于我

在读计算机科学与技术。喜欢把脑子里的想法做成真的能跑起来的东西：从一个命令行小工具，到一个有登录、有后台、有统计、能上线的完整站点。

比起刷完一整套教程，我更相信「先写出来，再修好它」——所以我这些仓库里的版本号都长得离谱，每一次 `vX.Y.Z` 背后都是一次真实的踩坑和修复。

> 「双非不是终点，持续学习才是。」

| | |
|---|---|
| 🔭 正在做 | [`mysite`](https://github.com/sheephearttidy/mysite)（Flask + SQLite 个人站后台） · [`CBuild`](https://github.com/sheephearttidy/CBuild)（自举的 C/C++ 构建工具） |
| 🌱 正在学 | 算法与数据结构、C++ / Java 补课、AI Agent 工作流 |
| 💬 可以聊 | C 语言基础、Flask 轻量后台、Nginx 部署、Linux 日常运维 |
| 🧭 原则 | 能离线就离线，能零依赖就零依赖，改完要能验证 |

---

## 🚀 精选项目

| 项目 | 是什么 | 技术栈 |
|:--|:--|:--|
| [**mysite**](https://github.com/sheephearttidy/mysite) | 贴纸风学生个人主页 + 后台管理系统。前台 7 个页面手写 HTML/CSS/JS 零框架，后台 Flask + SQLite 在线改内容 | `Python` `Flask` `SQLite` `JavaScript` `Nginx` |
| [**CBuild**](https://github.com/sheephearttidy/CBuild) | 零配置 C/C++ 构建工具，一条 `cbuild build` 替代 CMake/Makefile 样板，并且**用它自己构建自己** | `C11` `CMake` `POSIX/Win32` |
| [**HowMuchGIUse**](https://github.com/sheephearttidy/HowMuchGIUse) | 轻量网络流量监控：实时速率、日/月/小时统计、多网卡，数据全存本地 SQLite，不联网不上传 | `Python` `psutil` `SQLite` |
| [**MiniGrade**](https://github.com/sheephearttidy/MiniGrade) | 命令行学生成绩管理器，为吃透 C 语言核心知识点（指针、函数指针、union、位域、可变参数）而写的练习项目 | `C` `Makefile` |

<details>
<summary><b>几个我觉得值得一提的细节</b></summary>

<br />

**mysite** —— 一个「越写越像产品」的练手站，41 次提交迭代到 `v2.5.1`：

- 前台纯手搓，零框架零依赖；后台可在线编辑技能树、项目墙、时间线、公告、留言板，改内容不用碰代码
- 安全上是认真做的：图形验证码（纯标准库 SVG 生成、一次性、答案哈希存储）、TOTP 两步验证（RFC 6238 手写实现）、CSP nonce、登录限速与 IP 封锁、敏感操作审计留痕
- 自建访问统计 + 「来访地图」：IP 只用于解析城市，**只存城市不存 IP**，SVG 世界地图上钉贴纸星星
- PWA、深色模式、节日特效，GitHub Actions 做前端一致性检查（导航一致、资源存在、`?v=` 哈希与文件 sha256 对得上）

**CBuild** —— 写它是为了不再写 `CMakeLists.txt`：

- 一份 `scaffold.toml` 管完项目配置，编译器自动探测（`gcc` → `clang` → `cc`）
- 增量编译是真的增量：用 `gcc -MMD` 生成头文件依赖，改一个公共头只重编真正包含它的翻译单元
- 并行编译（`-j N`，Windows 用 `CreateProcess`、Unix 用 `fork`+`exec`）
- 所有公开函数返回语义化错误码而不是 `-1`；`#ifdef _WIN32` 只出现在一个文件里
- **自举**：CMake 只在第一次编译出 `cbuild` 时用一次，之后 `cbuild build` 编译它自己的源码

</details>

---

## 🛠 技术栈

**主力**（都有上面这些公开项目为证）

<p>
  <img alt="C" src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white" />
  <img alt="C++" src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css&logoColor=white" />
  <img alt="Bash" src="https://img.shields.io/badge/Shell-4EAA25?style=flat-square&logo=gnubash&logoColor=white" />
</p>

**Web 与后端**

<p>
  <img alt="Flask" src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" />
  <img alt="gunicorn" src="https://img.shields.io/badge/gunicorn-499848?style=flat-square&logo=gunicorn&logoColor=white" />
  <img alt="Nginx" src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" />
</p>

**工具与部署**

<p>
  <img alt="Linux" src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
  <img alt="CMake" src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" />
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
</p>

**还在路上**：Java · MySQL · Redis · Docker · Node.js —— 在学，暂时还没有能拿出来看的公开项目。

---

## 🌱 现在与以后

- 把 `mysite` 的测试和部署流程再收一收，让它从「能跑」变成「敢改」
- 给 `CBuild` 补上库目标类型（`type = "lib"`）和 `cbuild test`
- 补算法与系统设计的基础，把学到的东西继续写成能跑的项目
- 继续用 AI / Agent 的方式改自己的开发流程

> 代码不是为了「会写」，而是为了「能解决问题」。
> 真正能成长的，不只是技术，而是持续学习和不断迭代的态度。

---

<div align="center">

<a href="https://github.com/sheephearttidy">
  <img src="https://img.shields.io/badge/Thanks%20for%20visiting-My%20GitHub-ff6b6b?style=for-the-badge" alt="Thanks" />
</a>

<br /><br />

[![](https://img.shields.io/badge/powered_by-dsh-4D6BFE?style=flat-square&logo=deepseek&logoColor=white)](https://github.com/deepseek-ai/deepseek-harness)

</div>
