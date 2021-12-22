# 代码示例搜索

阿里云智能编码插件（Alibaba Cloud AI Coding Assistant）提供API的代码示例搜索功能，让你在面对不熟悉的功能模块时，无需来回跳转页面，在IDE内即可参考海量优质的开源代码示例，为你打造沉浸式编码体验。



你可以通过点击右侧菜单栏中的「代码示例搜索」唤起搜索窗口进行主动搜索，也可以在编码过程中通过鼠标右键选中当前类/接口/方法即可一键搜索其示例片段。
<p align="center">
<img src="https://img.alicdn.com/imgextra/i2/O1CN01LkVxJ71IktqQtmjbh_!!6000000000932-2-tps-852-1022.png" alt="example" width="500">
</p>

## 支持形式

- 英文自然语言搜索（[内测版本](https://github.com/alibaba-cloud-toolkit/cosy/wiki/%E5%86%85%E6%B5%8B%E7%89%88%E6%9C%AC)）
  - 在搜索框中输入搜索词，如How to read excel，敲击回车触发

- 类名/接口名/枚举名

  - 如：XSSF能搜出以XSSF为前缀的类名XSSFWorkbook、XSSFRow等

- 包名+类名

  - 如：org.apache.poi能搜出这个包下的所有类/接口/枚举
  - 如：org.apache.poi.xssf.usermodel.XSSFWorkbook能准确搜出apache包下的XSSFWorkbook类

- 方法名

  - 如：createSh能搜出以createSh为前缀的方法名createSheet、CreateShortcut、createShell等

- 类名/接口名+方法名，枚举名+属性名

  - 如：XSSFWorkbook.create能搜出以其为前缀的XSSFWorkbook.createSheet、XSSFWorkbook.createFont、XSSFWorkbook.createCellStyle等

- 包名+类名/接口名+方法名，包名+枚举名+属性名
<p align="center">
<img src="https://img.alicdn.com/imgextra/i3/O1CN01sV74ML1uRcZXp6PRe_!!6000000006034-2-tps-1258-1614.png" alt="example" width="500">
</p>

## 联合搜索
- API之间支持联合搜索
- 自然语言搜索和API也支持联合搜索（[内测版本](https://github.com/alibaba-cloud-toolkit/cosy/wiki/%E5%86%85%E6%B5%8B%E7%89%88%E6%9C%AC)）

## 前提条件

- 已在IntelliJ IDEA中安装和配置Alibaba Cloud AI Coding Assistant，[如何安装](https://github.com/alibaba-cloud-toolkit/cosy/wiki/%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B)。
- 系统要求：Windows 10/Mac OS/Linux

- 安装JDK8以上



## 支持语言

- 目前仅支持Java，后续会扩展JavaScript、Python等语言



# 使用示例
<p align="center">
<img src="https://github.com/alibaba-cloud-toolkit/cosy/blob/main/cosy-search-demo.gif" alt="demo">
</p>