## Vscode 使用 Vetur+Prettier 格式化代码（团队统一配置文件）

------



## 一、Vscode 安装插件

1. Vetur
2. Prettier

------



## 二、使用配置文件

## vscode setting.json

```json
// Prettier js文件格式化配置
"[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode" // 使用prettier格式化js文件
},

// Vetur vue文件格式化配置
"[vue]": {
    "editor.defaultFormatter": "octref.vetur"
},
"vetur.format.defaultFormatter.html": "prettyhtml",
```

## .prettierrc.yml

```yaml
arrowParens: 'avoid' # 箭头函数单个参数不加括号
singleQuote: true # 单引号
trailingComma: 'none' # 无尾随逗号
printWidth: 150 # 每行代码最佳长度
semi: false # 不已分号结尾
```

------



## 三、不使用配置文件（直接在 vscode 全局配置）

## vscode setting.json

```json
// Prettier js文件格式化配置
"[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode" // 使用prettier格式化js文件
},
"prettier.useEditorConfig": false,  // 不启用配置文件
"prettier.arrowParens": "avoid",  // 箭头函数单个参数不加括号
"prettier.singleQuote": true,    // 单引号
"prettier.trailingComma": "none",   // 无尾随逗号
"prettier.printWidth": 150,  // 每行代码最佳长度
"prettier.semi": false,  // 不已分号结尾

// Vetur vue文件格式化配置
"[vue]": {
    "editor.defaultFormatter": "octref.vetur"
},
"vetur.format.defaultFormatterOptions": {   // 使用prettier格式化vue文件中<script>
    "prettier": {
        "useEditorConfig": true, // 不启用配置文件
        "arrowParens": "avoid",  // 箭头函数单个参数不加括号
        "singleQuote": true,    // 单引号
        "trailingComma": "none",   // 无尾随逗号
        "printWidth": 150,  // 每行代码最佳长度
        "semi": false,  // 不已分号结尾
    },
},
"vetur.format.defaultFormatter.html": "prettyhtml",
```
