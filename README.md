# 模仿音乐盒
## react + es6 + webpack架构模式
## 技术栈
- 基础列库：react
- 路由：react-router4
- 数据管理：react-redux + redux-thunk中间件 + redux-devtool
- 路由信息同步：react-router-redux
- 音乐播放内核：jplayer
- 样式：less

###项目目录结构：
```
.
├─ server/           # node模拟后台
├─  ├─ mock/         # 数据存储模块
├─  ├─  ├─ file.json    # 模拟音乐数据
├─  ├─  ├─ hots.js      # 模拟热搜数据
├─  ├─  ├─ silder.js    # 模拟轮播图数据
├─  ├─ server.js    # 模拟后台处理请求
├─ src/              # 源码目录（开发都在这里进行）
│   ├─ api/         # 前端请求数据方法
|   ├─ common/     # 放置无需经由 Webpack 处理的静态文件
│   ├─ components/     # 组件（COMPONENT）
|   ├─ containers/      # 路由
│   ├─ redux/          # Redux 一箩筐
│   │   ├─ actions/      # （ACTION）
│   │   ├─ reducers/     # （REDUCER）
│   │   ├─ store/        # （STORE）
│   ├── main.js        # 入口文件
├── .babelrc         # Babel 转码配置
├── .index.html      # 静态基页
├── .gitignore       # （配置）需被 Git 忽略的文件（夹）
├── package.json     # （这个就不用多解释了吧）
├── .webpack.config.js        # ESLint 配置
```
### 安装和运行程序
- 克隆项目
```
$ git clone https://github.com
```
- 安装依赖
```$xslt
npm install
```
- 安装依赖模块
```$xslt
npm install webpack webpack-dev-server babel-core babel-loader babel-preset-es2015 babel-preset-react babel-preset-stage-0 less less-loader style-loader css-loader url-loader file-loader html-webpack-plugin -D
```
> 其他项目依赖安装请看`package.json`

- 在server目录下启动后台服务
```$xslt
直接运行server.js文件即可
```
- 在cmd中启动webpack服务
```$xslt
npm run dev
```


