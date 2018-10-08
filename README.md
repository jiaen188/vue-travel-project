# where-to-travel

> 一个关于练习vue的demo [预览](https://jiaen188.github.io/vue-travel-project/#/)

&nbsp;&nbsp;覆盖大部分vue基础知识点,除了使用better-scoll实现接近原生的滚动效果，vue-awesome-swiper实现轮播效果，其他全部使用stylus自定义组件
ps：目前由于使用本地接口，需要访问8080端口,如果想要修改，请在/config/index.js中修改proxyTable

## 技术栈

>	vue + vue-router + vuex + axios

## 目录结构

```

|——build                                                //构建
|——config                                               //配置

|——node_modules                                         //npm项目依赖

|——src
	  |——assets——
|			  |——styles                                       //样式
	|
|
    |——common——                                         //基础组件
|			  |——fade                                         //渐变动画组件
	|
|			  |——gallary                                      //画廊组件
	|
|
    |——base——                                           //业务页面
|			  |——city
  |         |——city.vue                                 //城市页面
|
  |         |——components
|               |
  |             |——Alphabet.vue                         //字母导航栏组件
|               |——Header.vue                           //Header组件
	|             |——List.vue                             //城市列表组件
|               |——Search.vue                           //搜索组件
  |
|			  |——detail
  |         |——detail.vue                               //推荐详情页面
|
  |         |——components
|               |
  |             |——Banner.vue                           //Banner组件
|               |——Header.vue                           //Header组件
	|             |——List.vue                             //票价树型组件
|
  |
|			  |——home
  |         |——home.vue                                 //主页面
|
  |         |——components
|               |
  |             |——Header.vue                           //Header组件
|               |——Icons.vue                            //Icon组件
	|             |——Recommend.vue                        //推荐列表组件
|               |——Swiper.vue                           //轮播组件
  |             |——Weekend.vue                          //列表组件
|
	  |——router——                                         //路由
|		      |——index.js
    |
|
	  |——store——                                          //vuex状态管理
|		     |——index.js
  |      |——mutations.js
|        |——state.js
  |
|
	  |——app.vue                                           //主文件
|
	  |——main.js                                           //主文件入口
|
  |
|——static
  |   |——mock                                           //mock数据
|
  |
|
  |
|——index.html	                                          //首页

```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
