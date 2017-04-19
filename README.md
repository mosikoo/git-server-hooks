测试服务端自动部署...

后续补充完整的脚本

#### steps

* 在服务端git init --bare 一个仓库作为中转仓库,如`git init --bare test.git`
* vim hooks/post-receive脚本，如`cd test.git && vim hooks/post-receive`
* 在本地git（即源代码）添加服务端源，如本地为`git remote add deploy ~xxx.git`
* 本地git push deploy master 便会触发脚本

这里是依靠自己在服务端新建一个git服务端源来触发脚本，实际情况应该直接写github或gitlab中的hook即可
