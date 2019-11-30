#gitbook 安装步骤
 1. npm install gitbook-cli -g   //电子书命令行工具全局安装
   
 2. gitbook install  //安装
 3. gitbook init     //初始化，会生成README.md(首页)和SUMMARY.md(目录)文件。
 4. gitbook build  //将所有.md文件生成静态页面，放在一个_book文件夹中
 5. gitbook serve  //开启服务
 6. gitbook install 安装折叠菜单插件
    >需要添加一个book.json文件，文件内容为:
      ```javascript
      {
    "plugins": [
        "expandable-chapters"
              ],
   }
      ```
