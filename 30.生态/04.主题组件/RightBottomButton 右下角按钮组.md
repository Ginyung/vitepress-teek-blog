---
url: /vitepress-teek-blog/30.生态/04.主题组件/RightBottomButton 右下角按钮组.md
---

# RightBottomButton 右下角按钮组

右下角按钮组组件提供返回顶部、跳转到评论区功能。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkRightBottomButton } from "vitepress-theme-teek";

export default {
  extends: DefaultTheme,
  Layout: () => h("div", null, [h(TkRightBottomButton), h(DefaultTheme.Layout)]),
};
```
