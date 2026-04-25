---
url: /vitepress-teek-blog/30.生态/04.主题组件/ArticleAnalyze 文章分析.md
---

# ArticleAnalyze 文章分析

使用文章分析组件，可以获取文章的创建时间、字数、阅读时间、访问量等信息。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkArticleAnalyze, teekConfigContext } from "vitepress-theme-teek";

provide(teekConfigContext, {
  author: { name: "Teeker", link: "https://github.com/Kele-Bingtang" },
  articleAnalyze: {
    showIcon: true,
    dateFormat: "yyyy-MM-dd",
    showAuthor: true,
    showCreateDate: true,
    showUpdateDate: false,
    showCategory: false,
    showTag: false,
  },
  docAnalysis: {
    wordCount: true,
    readingTime: true,
  },

  // ... 更多配置请看配置系列文章
});

export default {
  extends: DefaultTheme,
  Layout: () =>
    h(DefaultTheme.Layout, null, {
      "doc-before": () => h(TkArticleAnalyze),
    }),
};
```
