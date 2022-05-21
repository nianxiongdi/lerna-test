


##


* `lerna init` 

    * 初始化lerna，会生成lerna.json文件与packages文件夹。
    * 会自动创建git
```js
{
  "packages": [ // 子package
    "packages/*" //
  ],
  "version": "1.0.0"
}
```

```
info cli using local version of lerna
lerna notice cli v4.0.0
lerna info Initializing Git repository
lerna info Updating package.json
lerna info Creating lerna.json
lerna info Creating packages directory
lerna success Initialized Lerna files
```


* `learn create 子包名`


* `learn add 包名 路径`

lerna add @sqf/utils packages/core[可选]


* `lerna add -h` 查下帮助文档

* `lerna bootstrap` 将本地包链接在一起并安装剩余的包依赖项 软链接
```js
    info cli using local version of lerna
    lerna notice cli v4.0.0
    lerna info Bootstrapping 2 packages
    lerna info Installing external dependencies
    lerna info Symlinking packages and binaries
    lerna success Bootstrapped 2 packages
```

* `npm link` - Symlink together all packages that are dependencies of each other

```js
    // core下面的utils的链接目录
    utils -> ../../../utils
```

* `lerna exec --  rm -rf ./node_modules` - 执行命令

    * 可以在根目录 package都可以使用 

```js
// --scope 指定包名 为package的name
lerna exec --scope @sqf/core --  rm -rf ./**/node_modules

```


* `lerna run test` - 运行npm命令