---
url: /vitepress-teek-blog/30.生态/04.主题组件/ThemeEnhance 主题增强.md
---

# ThemeEnhance 主题增强&#x20;

使用文章分析组件，可以获取文章的创建时间、字数、阅读时间、访问量等信息。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkThemeEnhance, teekConfigContext } from "vitepress-theme-teek";

provide(teekConfigContext, {
  themeEnhance: {
    // ... 更多配置请看配置系列文章
  },
});

export default {
  extends: DefaultTheme,
  Layout: () =>
    h(DefaultTheme.Layout, null, {
      "nav-bar-content-after": () => h(TkThemeEnhance),
    }),
};
```
