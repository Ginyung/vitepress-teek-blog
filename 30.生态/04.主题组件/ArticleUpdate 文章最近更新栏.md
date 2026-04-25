---
url: /vitepress-teek-blog/30.生态/04.主题组件/ArticleUpdate 文章最近更新栏.md
---

# ArticleUpdate 文章最近更新栏&#x20;

在文章页底部使用文章最近更新栏组件，可以显示最近更新的文章信息，方便点击查看。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkArticleUpdate, teekConfigContext } from "vitepress-theme-teek";
import "vitepress-theme-teek/theme-chalk/tk-article-update.css";

provide(teekConfigContext, {
  articleUpdate: {
    limit: 3, // 默认为 3，表示最多显示 3 条最近更新文章
  },
});

export default {
  extends: DefaultTheme,
  Layout: () =>
    h(DefaultTheme.Layout, null, {
      "doc-after": () => h(TkArticleUpdate),
    }),
};
```
