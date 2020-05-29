# TypeScript-Starter - TypeScript 库开发框架

## 特性

 - 零配置，只需更改库名称与运行 `npm install` :wink:

 - 支持全量引入与按需加载

 - 使用 **[RollupJS](https://rollupjs.org/)** 打包，并遵循了 [Tree-shaking](https://alexjoverm.github.io/2017/03/06/Tree-shaking-with-Webpack-2-TypeScript-and-Babel/) 与 [standard convention](http://2ality.com/2017/04/setting-up-multi-platform-packages.html)

 - 使用 **[Jest](http://facebook.github.io/jest/)** 进行测试并给出测试覆盖率

 - 使用 **[Prettier](https://github.com/prettier/prettier)** 与 **[TSLint](https://palantir.github.io/tslint/)** 规范代码

 - 使用 **[TypeDoc](http://typedoc.org/)** 生成代码文档

 - 自动生成 `(*.d.ts)` 类型文件

 - 使用 [Commitizen](https://github.com/commitizen/cz-cli), [Conventional changelog](https://github.com/conventional-changelog/conventional-changelog) 与 [Husky](https://github.com/typicode/husky) (for the git hooks) 来规范 git flow

## 开发说明

### 强制遵循

- 使用 TypeScript 进行开发

- 需要为每一个类或方法进行注释，最小化注释为：方法说明、参数、返回值

- 需要为每一个导出的类或方法编写测试

- 使用 `git add` 与 `npm run commit` 来提交代码

### 约定

- src/index.ts 作为入口文件，应该在这里导出所有方法

### 开始

- Fork 该仓库后 Clone 到本地

- 更改项目信息：仓库地址、名称、作者等

- 安装依赖

- 开始开发

## NPM 脚本说明

 - `npm run lint`: 使用 tslint 规范代码

 - `npm run rm`: 移除 dist / docs 目录

 - `npm run build`: 生成 bundles、`.d.ts`文件、以及文档

 - `npm start`: 以 live-reload 模式运行 `npm run build`

 - `npm run test`: 运行测试

 - `npm run test:watch`: 以 [观察模式](http://facebook.github.io/jest/docs/cli.html#watch) 运行测试

 - `npm run test:prod`: lint 代码、运行测试并生成测试文档(包含测试覆盖率)

 - `npm run commit`: 规范化、可交互的代码提交流程，基于 conventional 规范

## 库的使用

全量引入：

```javascript
import awesomeLib from 'awesomeLib'
```

从 `dist/lib` 按需引入：

```javascript
import coolFn from 'mylib/dist/lib/coolFn'
```

