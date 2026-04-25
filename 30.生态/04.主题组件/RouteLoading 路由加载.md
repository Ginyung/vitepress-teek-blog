---
url: /vitepress-teek-blog/30.生态/04.主题组件/RouteLoading 路由加载.md
---

# RouteLoading 路由加载

页面加载 Loading 组件，在切换路由前显示，在切换路由后消失。

## 基础使用

```ts
import { h } from "vue";
import DefaultTheme from "vitepress/theme";
import { TkRouteLoading, teekConfigContext } from "vitepress-theme-teek";
import "vitepress-theme-teek/theme-chalk/tk-article-update.css";

provide(teekConfigContext, {
  loading: "Teek 正在加载中...", // 指定加载 Loading 动画的文案
});

export default {
  extends: DefaultTheme,
  Layout: () => h("div", null, [h(TkRouteLoading), h(DefaultTheme.Layout)]),
};
```
