# [学习uni-app开发仓库](https://github.com/daibeisi/uni-app)

## 项目结构
    mini-program
    ├── common                   // 通用配置文件夹
    │   ├── js                   	// js文件夹
	│   │   ├──api.js               	// GET,POST请求封装
	│   │   └──config.js				// 全局配置
    │   └── css                  	// css文件夹
	├── components               // 自定义组件文件夹
    ├── pages                    // 主包
    ├── pages_Application        // 分包一 功能应用         
    ├── static                   // 静态文件夹
    │   ├── css                      // 全局css
    │   └── image                    // 图片文件夹
    ├── uni_modules              // 插件模块
    ├── .gitignore               // Git忽略提交规则文件
    ├── App.vue                  // 项目的主组件
    ├── index.html               // 主渲染文件
    ├── main.js                  // Vue初始化入口文件
    ├── manifest.json            // 配置应用名称、appid、logo、版本等打包信息
    ├── pages.json               // 配置页面路由、导航条、选项卡等页面类信息
    ├── README.md                // 项目手册
    └── uni.scss                 // 内置的常用样式变量介绍
