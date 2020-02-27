# 基础镜像
FROM node:latest
# 作者
MAINTAINER linhey, qijie
# 安装hexo
RUN npm install -g hexo-cli
# 拉取
RUN git clone https://github.com/dodoyuan/hexo_template hexo_blog
# 切换目录
WORKDIR hexo_blog
# 添加权限与安装npm
RUN chmod +x /hexo_blog/ && npm install && npm install forever -g
# 挂载md目录
RUN git clone https://github.com/dodoyuan/hexo_pages_template source
# 端口暴露
EXPOSE 8080
# 运行 hexo 
CMD ["hexo","server"]

