---
title: 预渲染插件
tags: [vue, prerender]
---

- 插件名
`prerender-spa-plugin`

`vue add prerender-spa`

[Github](https://github.com/SolarLiner/vue-cli-plugin-prerender-spa)

- 使用会添加 `puppeteer` 依赖，（可能安装失败）

    type puppeteer_download_host = https://npm.taobao.org/mirrors

- 使用配置添加 `routes，timeout`，如：

```javascript

pluginOptions: {
    prerenderSpa: {
        registry: undefined,
        renderRoutes: [
            '/'
        ],
        useRenderEvent: true,
        headless: true,
        onlyProduction: true,
        customRendererConfig: {
            slowMo: 1000,
            timeout: 5e4,
            defaultViewport: {
                width: 1920,
                height: 1080
            }
        }
    }
}

```

- 生产环境生成单独静态 `html` 文件

- 故应使用 `history` 路由模式，配置服务器容器指向对应文件
