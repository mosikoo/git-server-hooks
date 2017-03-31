测试服务端自动部署...

后续补充完整的脚本

#### steps

* 在服务端git init --bare 一个仓库作为中转仓库
* vim hooks/post-receive脚本
* 在本地添加服务端源，如本地为`git remote add deploy ~xxx.git`
* 本地git push deploy master 便会触发脚本
