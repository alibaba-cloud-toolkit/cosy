After installing the Alibaba Cloud AI Coding Assistant in your IntelliJ IDEA, you can enjoy features such as intelligent code completion and code sample search in the local editor.

# Get Ready

- JDK1.8 or higher
- IntelliJ IDEA (2020.1 or later)

# Installation

Currently, the Alibaba Cloud AI Coding Assistant has released a public beta version. You can install it through the marketplace or by an offline package.

<!-- tabs:start -->

#### **Direct Installation**

Pre-request:
* At least one IntelliJ IDEA has been started
* If the installation fails, try restarting the IDE, or manually installing through the plugin marketplace

<span id='intellij-plugin-button'>Data Loading...</span>
<noscript>
Sorry, your browser does not support direct installation. Please try installing manually through the plug-in market.
</noscript>


#### **Marketplace Installation**

1. Select **IntelliJ IDEA** > **Preferences** in the IntelliJ IDEA top menu bar.
2. Click **Plugins** in the left navigation bar of the **Preferences** page.
3. Click **Marketplace** in the **Plugins** area.
4. Search for **Alibaba Cloud AI Coding Assistan**t or **Cosy**
5. Alibaba Cloud AI Coding Assistant will appear in the **Search Results** area, click Install.
6. After waiting for the download and installation to complete, click **Restart IDE**. 
![image](https://img.alicdn.com/imgextra/i4/O1CN01jERvSm1ejSAJWWgDC_!!6000000003907-0-tps-2654-1400.jpg)

#### **Offline Package Installation**

Provide two offline packages, you can directly click to download or download through [Github Release](https://github.com/alibaba-cloud-toolkit/cosy/releases):

* Lightweight package: https://toolkit.aliyun.com/idea/cosy-intellij-beta-latest.zip
* All-In-One package: http://toolkit.aliyun.com/idea/cosy-intellij-beta-latest-all-in-one.zip

Installation method:

1. Select **IntelliJ IDEA** > **Preferences** in the IntelliJ IDEA top menu bar.
2. Click **Plugins** in the left navigation bar of the **Preferences** page.
3. Click the **Settings** Icon in the **Plugins** area, and then click **Install Plugin from Disk....**
4. In the **Choose Plugin File** dialog box, select the **cosy-intellij-beta-latest.zip** downloaded in step 1. After the installation is complete, click **Restart IDE**. 
![image](https://img.alicdn.com/imgextra/i3/O1CN01hzRLdp1LACysYVSiN_!!6000000001258-2-tps-1958-616.png)

<!-- tabs:end -->

## Validation results

After IntelliJ IDEA restarts, if there is a [**Code Search**] Tab on the right sidebar, or a completion item from Alibaba Cloud AI Coding Assistant, that is, with the **"Cosy"** logo on the right side appears during the coding process, then the installation is successful.

# Documentation

## Code Completion

[Code Completion Documentation](en-us/guide/how-to-use-completion.md)

## Code Search

[Code Search Documentation](en-us/guide/how-to-use-codesearch.md)

# Contact Us

If you encounter problems or have any suggestions when using the Alibaba Cloud AI Coding AI Assistant, please give us feedback in [Issues]([https://github.com/alibaba-cloud-toolkit/cosy/issues](https://github.com/alibaba-cloud-toolkit/cosy/issues)):-)

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
