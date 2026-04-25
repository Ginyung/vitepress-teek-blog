---
url: /vitepress-teek-blog/30.生态/03.公共组件/InputSlide 滑块.md
---

# InputSlide 滑块

## 基础用法

::: demo
inputSlide/basic
:::

## API

### 配置项

| 名称     | 说明              | 类型                      | 默认值 |
| -------- | ----------------- | ------------------------- | ------ |
| v-model  | 绑定值            | `number`                  | 0      |
| min      | 最小值            | `number`                  | 0      |
| max      | 最大值            | `number`                  | 100    |
| step     | 步长              | `number`                  | 1      |
| disabled | 是否禁用          | `boolean`                 | false  |
| format   | 格式化显示的内容  | `(val: number) => string` | —      |
| name     | input 标签的 name | `string`                  | Slider |
