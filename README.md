# nuxt-demo

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

* 创建项目，选择组件，框架，并下载依赖
  npx create-nuxt-app nuxt-demo

* 进入项目根目录
  cd nuxt-demo

* 开发模式，热更新
  npm run dev

静态部署，可以部署到静态服务器：

* 构建静态文件

* npm run generate

* 使用generate打包后每个对应的页面都会生成一个html，你在打包的时候不能关闭后台，他会请求后台数据生成首屏的数据

* 这样打包有一个弊端，当你首屏的数据发生更改的时候，他还是显示的是之前的数据，要想改变的话，需要重新打包发布才行。所以，如果你的首屏是动态的就不建议使用这种打包方式了。

* 打包之后每个页面都生成了HTML页面，只有首屏（首次打开）的数据是之前渲染好了，但是其它数据还是从后台获取，比如翻页，第二页数据是重新请求后台的，你再次返回第一页也是再次请求的。

动态部署，需要部署到nodejs服务器

* 构建生产环境项目文件

* npm run build

* 运行项目

* npm run start

* build打包生成的是动态页面，当然是同样具有SEO功能，但是首屏（首次打开）的数据是请求后台的。
