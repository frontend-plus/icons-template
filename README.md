# icons-template

根据 svg 生成 vue3 icon组件的模板库。

基于 [element-plus-icons](https://github.com/element-plus/element-plus-icons) 的 `35b91fd484b4cb0904cf0818e2734ad22160a787` 版本改造。

# 模板修改

假设你需要生成的 icons 前缀名叫：your-icons-name 。那么，需要修改：

1. `packages/svg/package.json` 中的 `name` 字段为： `@your-icons-name/icons-svg`。
2. `packages/vue/package.json` 中的 `name` 字段为： `@your-icons-name/icons-vue`。
3. `packages/vue/package.json` 中的 `devDependencies` 下的 `@element-plus/` 包替换为 `@your-icons-name/`。
4. `packages/vue/build/generate.ts` 中的 `@element-plus/` 包替换为 `@your-imcons-name/`。
5. `playground/package.json` 中的 `dependencies` 下的 `@element-plus/` 包替换为 `@your-icons-name/`。
6. `playground/src/App.vue` 中的 `@element-plus/icons-vue` 替换为 `@your-icons-name/icons-vue`。

# 使用

```bash
# 安装依赖包
pnpm i
# 本地查看
pnpm dev
# 编译
pnpm build
```
