##gh-pages发布步骤
1. gitbook build 
2. cd _book
3. git init 
4. git checkout --orphan gh-pages //新建分支gh-pages并切换到该分支
5. git add
6. git commit -m 'message'
7. git remote add origin url //设置远程仓库源，url为github仓库地址
8. git push -u origin gh-pages  //推送到远程仓库
9. 访问方式： github用户名.github.io/项目名
10. 添加域名解析：项目中添加一个CNAME文件，文件内容为域名,登录服务器添加域名解析。



