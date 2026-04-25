---
url: /vitepress-teek-blog/30.生态/04.主题组件/ArticleHeadingHighlight 标题高亮.md
---

# ArticleHeadingHighlight 标题高亮

使用标题高亮组件，可以在点击标题时，高亮标题，方便快速定位在哪个位置。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkArticleHeadingHighlight } from "vitepress-theme-teek";

export default {
  extends: DefaultTheme,
  Layout: () => h("div", null, [h(TkArticleHeadingHighlight), h(DefaultTheme.Layout)]),
};
```
