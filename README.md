# DTM子应用模板
```
在根目录引用DTM子应用公共项目(DTMillerAppsPublic)
请使用git submodule：
    git submodule add <path> DTMillerAppsPublic 添加子模块
    git submodule init 初始化子模块
    git submodule update 更新子模块
```

# app.json
```
app.json内必须包含以下内容
{
    "appName": "模板项目",
    "appNameEn": "template project",
    "appId": "app-test",
    "appIcon": "",
    "description": "",
    "descriptionEn": "",
    "versions": "v1.1.0"
}
```

# main.js
```
每个子应用必须执行appStart方法，并提供testMode(本地调试时可产生对应的全部页面、按钮权限)
```

# router
```
router内所有文件必须为.mjs，需使用的modules必须在index.mjs中被引用，引用顺序影响菜单结构
```

# views
```
_layout文件内.vue文件必须保留
```

# i18n
```
i18n文件夹下需要有en.js、zh.mjs，并在index中引用
en.js、zh.mjs保持以下结构
{
    "routes": { ... } 菜单、页面名称
    "views": { 页面内容
        [二级菜单]: {
            [三级页面]: { ... },
            [四级页面(tab)]: { ... }
        }
    } 
    "components": { 组件内容
        [组件名称]: { ... }
    } 
}
```