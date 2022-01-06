在IntelliJ IDEA中安装阿里云智能编码插件（Alibaba Cloud AI Coding Assistant）后，你可以在本地编辑器内享受代码智能补全、代码示例搜索等功能。

# 准备工作

- 下载并安装JDK1.8或更高版本
- 下载并安装IntelliJ IDEA（2020.1或更高版本）

# 安装插件

当前阿里云智能编码插件已经发布**公测**版本，你可以通过插件市场或离线包完成安装。

<!-- tabs:start -->

#### **直接安装**

注意事项：
* 至少有一个IntelliJ IDEA已经启动
* 如果安装失败，请尝试重启IDE，或通过插件市场手动安装

<span id='intellij-plugin-button'>数据加载中...</span>
<noscript>
抱歉，你的浏览器不支持直接安装，请尝试通过插件市场手动安装。
</noscript>


#### **插件市场安装**

1. 在IntelliJ IDEA顶部菜单栏中选择**IntelliJ IDEA** > **Preferences**。
2. 在**Preferences**对话框的左侧导航栏中单击**Plugins**。
3. 在**Plugins**区域单击**Marketplace**。
4. 在搜索栏中输入 ***Alibaba Cloud AI Coding Assistant*** 或 ***cosy***
5. **Search Results**区域会出现 ***Alibaba Cloud AI Coding Assistant*** ，单击**Install**。
6. 等待下载、安装完成后，单击**Restart IDE**。
![image](https://img.alicdn.com/imgextra/i2/O1CN01qjwZzO28UHVo3pufL_!!6000000007935-0-tps-2390-1412.jpg)

#### **离线包安装**

1. 复制链接 <a href="http://toolkit.aliyun.com/idea/cosy-intellij-beta-latest.zip" download=“download”>http://toolkit.aliyun.com/idea/cosy-intellij-beta-latest.zip</a> 至新窗口页即可下载，或通过[Github Release](https://github.com/alibaba-cloud-toolkit/cosy/releases)下载。
2. 在IntelliJ IDEA顶部菜单栏中选择**IntelliJ IDEA** > **Preferences**。
3. 在**Preferences**对话框的左侧导航栏中单击**Plugins**。
4. 在**Plugins**区域单击**Settings Icon**，再单击**Install Plugin from Disk**。
5. 在**Choose Plugin File**对话框中选择步骤1中下载的cosy-intellij-XXX.zip，安装完成后，单击**Restart IDE**。
![image](https://img.alicdn.com/imgextra/i3/O1CN01hzRLdp1LACysYVSiN_!!6000000001258-2-tps-1958-616.png)

<!-- tabs:end -->

## 验证结果

IntelliJ IDEA重启后，右侧边栏有【代码示例搜索】Tab，或者代码编辑过程中出现来自Alibaba Cloud AI Coding Assistant即右侧有"Cosy"标识的的补全项，则说明安装成功。

# 功能体验

## 代码智能补全

[代码智能补全使用帮助](zh-cn/guide/how-to-use-completion.md)

## 代码示例搜索

[代码示例搜索使用帮助](zh-cn/guide/how-to-use-codesearch.md)

# 联系我们

如果在使用阿里云智能编程插件时遇到问题或有任何建议，欢迎在[Issues](https://github.com/alibaba-cloud-toolkit/cosy/issues)中向我们反馈！

<script>
function getQueryVariable(target_param){
    let urlHash = window.location.hash;
    let index = urlHash.indexOf("?");
    if (index < 0) {
        return "";
    }
    let query = urlHash.substring(index+1);
    let vars = query.split("&");
    for (let i = 0; i < vars.length; i++) {
        let pair = vars[i].split("=");
        if(pair[0] == target_param) {
            return pair[1];
        }
    }
    return "";
}
let dataMap = {
    "direct_install": "直接安装",
    "market_install": "插件市场安装",
    "offline_install": "离线包安装",
};
let tabValue = getQueryVariable("tab");
if (tabValue && dataMap.hasOwnProperty(tabValue)) {
    let tabs = document.querySelectorAll(".docsify-tabs__tab");
    for (let tab of tabs) {
        let tabName = tab.getAttribute("data-tab");
        if (tabName === dataMap[tabValue]) {
            tab.setAttribute("class", "docsify-tabs__tab docsify-tabs__tab--active");
        } else {
            tab.setAttribute("class", "docsify-tabs__tab");
        }
    }
}


</script>