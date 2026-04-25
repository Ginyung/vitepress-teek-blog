---
url: /vitepress-teek-blog/30.生态/04.主题组件/ArticleShare 文章分享.md
---

# ArticleShare 文章分享

使用文章分享组件可以分享文章页的链接。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkArticleShare, teekConfigContext } from "vitepress-theme-teek";
import "vitepress-theme-teek/theme-chalk/tk-article-share.css";

provide(teekConfigContext, {
  articleShare: {
    // ... 更多配置请看配置系列文章
  },
});

export default {
  extends: DefaultTheme,
  Layout: () =>
    h(DefaultTheme.Layout, null, {
      "aside-outline-before": () => h(TkArticleShare),
    }),
};
```
