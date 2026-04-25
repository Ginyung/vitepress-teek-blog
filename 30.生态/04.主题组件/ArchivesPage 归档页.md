---
url: /vitepress-teek-blog/30.生态/04.主题组件/ArchivesPage 归档页.md
---

# ArchivesPage 归档页

## 基础使用

将归档页注册到全局里：

```ts
import DefaultTheme from "vitepress/theme";
import { TkArchivesPage } from "vitepress-theme-teek";
import "vitepress-theme-teek/theme-chalk/tk-archives-page.css";

export default {
  extends: DefaultTheme,
  enhanceApp({ app, siteData }) {
    app.component("TkArchivesPage", TkArchivesPage);
  },
};
```

创建一个 Markdown 文件，在 `frontmatter` 添加如下内容：

```yaml
---
layout: TkArchivesPage
---
```

此时访问该 Markdown 文件，即可看到效果。
