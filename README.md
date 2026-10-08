# Haotai Huang · 个人主页

基于 Astro 的个人学术主页，采用白色与浅灰色界面、清爽无衬线排版和低调蓝色点缀，支持日夜主题和响应式布局。

## 内容维护

主要内容集中在 `src/pages/index.astro` 文件顶部：

- `profile`：姓名、简介、邮箱、GitHub 和可选的 CV、Scholar、头像链接。
- `education`：教育经历、专业和时间。
- `interests`：研究兴趣及具体关心的问题。有真实成果后再加入项目或论文，不必为了填满页面编写占位成果。
- `notes`：笔记标题、日期和链接；数组为空时，笔记区和对应导航自动隐藏。

默认不显示头像或头像占位。需要照片时，可放在 `public/avatar.jpg`，然后设置 `profile.avatar = "avatar.jpg"`。CV 可放在 `public/cv.pdf`，再设置 `profile.cv = "cv.pdf"`。Scholar 和其他链接按实际资料填写，尚无资料时保留空字符串。

## 本地开发

在项目根目录运行：

```sh
npm install
npm run dev -- --background
```

后台开发服务器管理：

```sh
npm run dev -- status
npm run dev -- logs
npm run dev -- stop
```

生成生产站点：

```sh
npm run build
```

输出目录为 `dist/`。推送到 `main` 会触发 `.github/workflows/deploy.yml` 中的 GitHub Pages 构建与部署工作流。

Astro 文档：[docs.astro.build](https://docs.astro.build)。
