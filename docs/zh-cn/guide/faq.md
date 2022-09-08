# 常见问题

### Q: 安装之后无法使用，且每当在输入和使用Cosy搜索的时候，IDE下方状态栏都会显示【正在更新阿里云智能编码助手 Cosy】

A：这是由于我们上游依赖数据库的一个bug导致。你可以按照如下步骤尝试修复：

1. 关掉IDE，并且杀掉cosy.exe进程
2. 把`[用户路径]/.cosy/tmp`删掉
3. 重启IDE，等待Cosy初始化
4. 如果依然有问题，可以尝试把`[用户路径]/.cosy`完全删掉再重试

### Q：为什么插件卡在“正在更新阿里云智能编码插件Cosy”？

A：同上，请耐心等待模型下载完成。模型只会下载一次，下载完成后即可离线使用代码智能补全功能。

### Q：代码示例搜索功能也可以离线使用吗？

A：代码示例搜索必须在联网的状态下使用。

### Q：代码搜索无结果怎么办？

A：您可以选择按照如下步骤进行自助排查：

1. Cosy搜索服务目前是依赖网络访问的，请检查本地网络环境，确认是否可以连通外网。可以尝试ping codeup.cn-hangzhou.aliyuncs.com 查看网络连通性。

2. Cosy搜索请求会进行基础安全校验，请检查本地系统时间是否正确，避免因为请求时间戳异常而被错误拦截。

3. 查看日志文件 cosy.log，确认Cosy进程是否正常，根据日志信息重启IDEA（Mac用户：`~/.cosy/logs`，Windows用户：`C盘/用户/[用户名]/.cosy/logs`）

4. 检查本地Host，是否有 `127.0.0.1 localhost`，如果没有则需要添加

5. 以上还是不能解决，请在[GitHub Issues](https://github.com/alibaba-cloud-toolkit/cosy/issues)中上传日志信息联系我们，我们会第一时间为你排查。

### Q: 代码补全无结果怎么办？

A：如果你是Windows用户，可以检查`C盘/用户/[用户名]/.cosy/logs/cosy.log`，如果`cosy.log`文件中，出现有类似
```
Unable to serve local completion, exit status: 0xc0000135 
```
的日志，说明可能是本地没有安装.NET框架，或者某些dll依赖找不到所致。您可以尝试手动打开`C盘/用户/[用户名]/.cosy/bin/版本号/x86_64_windows/cosylocal.exe`，系统会显示缺少的dll文件名。下载对应的文件到该目录即可解决。

如果您是其他平台用户，或者上面的方案未能解决问题，请在[GitHub Issues](https://github.com/alibaba-cloud-toolkit/cosy/issues)中上传日志信息或加入[钉钉用户群](https://h5.dingtalk.com/circle/healthCheckin.html?dtaction=os&corpId=dingc5c1c8e7c328ad4e883b3bd722e90a8c&54de2a8c-e74a-4=16c4441b-9a75-4&cbdbhh=qwertyuiop)联系我们，我们会第一时间为你排查。

### Q：为什么安装之后没有代码补全提示，也搜索不到内容？

A：在首次安装插件后，Cosy需要联网下载模型和依赖文件，下载完成之后才可以提供离线代码提示，因此请等待Cosy初始化完毕之后试用。如果IDE底栏中没有“正在更新阿里云智能编码插件Cosy”的提示，那么请重启IDE尝试，一般可以解决。如果仍然没有提示，那么请在https://github.com/alibaba-cloud-toolkit/cosy/issues 反馈给我们，并且附上`~/.cosy/logs/cosy.log`。
