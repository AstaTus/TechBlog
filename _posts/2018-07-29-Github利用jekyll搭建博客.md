# Github利用jekyll搭建博客

##### 准备

- ruby

##### 搭建过程

1. 创建git仓库
2. 仓库改名成userame.github.io
3. 在setting中设置gitPage
4. 安装ruby
5. 打开cmd模式
6. 安装 jekyll：gem install jekyll
7. 创建博客：jekyll new <name>
8. cd <name>
9. 启动：bundle exec jekyll serve --port 1234(如果有错误 查看缺少哪些包 则执行 gem install <package name>安装)

##### 注意事项

- gem代理：gem install --http-proxy http://127.0.0.1:1080 <package name>

