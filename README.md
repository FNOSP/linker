<div align="center">
<p><img src="./src/docker/app/ui/images/icon_256.png" height="240"></p> 

# Linker

<a href="https://linker.snltty.com">应用网站</a>、<a href="https://linker-doc.snltty.com">应用文档</a>、<a href="https://github.com/snltty/linker" target="_blank">原开源项目</a>

</div>

这是linker项目的fnos(飞牛)应用打包库
1. 暂时只有docker应用版本，使用snltty/linker-musl镜像，Compressed size不到20MB，卸载后自动删除容器和镜像


## 1、[🎖️]发布
进入src/docker目录，使用
```
fnpack build
```
或者
```
sed -i 's/\r$//' manifest
sed -i 's/\r$//' cmd/main
sed -i 's/\r$//' cmd/uninstall_callback

tar -czf app.tgz --transform='s,app/,,g' app/docker app/ui config
tar -czf linker.fpk --exclude='app' *
mv linker.fpk linker-docker-x64.fpk
```
