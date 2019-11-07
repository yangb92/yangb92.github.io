# Hexo 个人博客

## 自动推送

推送配置 
```
deploy:
  type: git
  repo: git@gitee.com:yangb92/yangb92.git
  message: hexo auto commit
  branch: master
```
会推送导该仓库的master分支. 使用`hexo deploy`命令部署,简写 `hexo d`, 部署前需要重新生成静态资源 `hexo g` 