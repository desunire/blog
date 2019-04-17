# blog
mime blog

参考文档
https://www.cnblogs.com/liuxianan/p/build-blog-website-by-hexo-github.html

本地运行
hexo s 然后访问http://localhost:4000

hexo常用命令
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #部署到GitHub
hexo help  # 查看帮助
hexo version  #查看Hexo的版本
缩写版本
hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy

组合命令
hexo s -g #生成并本地预览
hexo d -g #生成并上传  ----最终访问地址 https://desunire.github.io/



使用演示
1:hexo new "newpage"
2:编辑newpage页面
3:hexo d -g 上传到github

