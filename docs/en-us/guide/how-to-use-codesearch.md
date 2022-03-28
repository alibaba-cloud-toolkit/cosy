# Code Search

Alibaba Cloud AI Coding Assistant provides a code search function of the API as well as natural language,  so that you can refer to a large number of high-quality open-source code samples in the IDE without switching to browsers when facing unfamiliar functional modules and get an immersive coding experience.

## Requirements

- Alibaba Cloud AI Coding Assistant has been installed and configured in IntelliJ IDEA, see [Install Plug-in](en-us/guide/quickstart.md)。
- System requirements: Windows 7 or later/Mac OS/Linux

## Search by functional description

When developers need to implement unfamiliar functional modules, they usually use general search engines to find relevant open source solutions. However, because the quality of results provided by general search engines is uneven, and it is impossible to quickly judge whether or not from the title of the result page It is because you need information that affects the developer's search efficiency. Cosy provides developers with natural language search capabilities, and developers can quickly find open source implementations of related functions through text descriptions of functions.

- Support English function description search
  - Enter the function description in the search box, such as How to read excel, press Enter, you can search for code examples for ***reading Excel***.
  - Enter a short keyword in the search box, such as oss download file, press Enter, you can search for the code examples for ***OSS download file***

If developers want to further filter the results of natural language search, they can perform secondary filtering through joint API search, for example:

- When the developer wants to implement the function of "reading Excel", the developer can search by entering "read excel". However, there are many open source libraries that can implement this function. If the developer wants to specify the use of the Apache POI library to implement this function, you can add an API (such as XSSFWorkbook) under the library to the search criteria, then you can search for code examples that use the XSSFWorkbook API to read Excel.

## Search by APIs

When developers encounter unfamiliar APIs, they want to find API-related usage examples. However, many official API documents are incomplete, either with simple text descriptions in Javadoc, or with only a few unit test cases, or lack of any Sample code, which requires developers to spend a lot of time to find sample code for the API.

Cosy provides developers with the ability to find API code samples. Developers can quickly find open source code samples that reference the API by simply entering the API name or triggering through shortcut keys.

### Quick search

Developers can right-click to select the current Class/Interface/Method during the coding process, and then click ***Code Search*** to search for code sample fragments of the specified API with one click. Developers can also search for the specified API through shortcut keys MacOS `command+shift+s` or Windows `ctrl+shift+s` .

![search_menu_example](https://img.alicdn.com/imgextra/i2/O1CN017x5C6w1dxoySqHXU4_!!6000000003803-2-tps-786-1070.png ':size=300')

### Search Condition

Developers can call up the search tool window by clicking `Code Sample Search` in the menu bar on the right, and manually enter the API name to search for code samples. The supported API name formats are as follows:

- Class name/Interface name/Enumeration name
   - i.e., XSSF can be used for searching class names such as XSSFWorkbook, XSSFRow, etc.
- Package name + Class name
   - i.e., org.apache.poi can be used for searching all classes/interfaces/enumerations under this package
   - org.apache.poi.xssf.usermodel.XSSFWorkbook can accurately search out the XSSFWorkbook class under the apache package
- Method name
   - createSh can be used for searching method names prefixed with createSh, such as createSheet, CreateShortcut, etc.
- class name/Interface name + Method name, Enumeration name + Attribute name
   - XSSFWorkbook.create can be used for searching XSSFWorkbook.createSheet, XSSFWorkbook.createFont, XSSFWorkbook.createCellStyle, etc. 
- Package name + Class name/Interface name + Method name, Package name + Enumeration name + Attribute name

![search_example](https://img.alicdn.com/imgextra/i4/O1CN01Az8BWf1JFaP9OzHye_!!6000000000999-2-tps-1096-1382.png ':size=500')


## Supported languages

- Currently supports Java, more languages versions will be supported soon.

## Demo Video

### Search by APIs

[code-search-demo.mp4](https://cosy-aliyun.oss-cn-hangzhou.aliyuncs.com/code-search-demo.mp4 ':include :size=500')

### Search by functional description

[code-search-demo.mp4](https://aliyun-cosy.oss-cn-hangzhou.aliyuncs.com/cosy_search_demo.mp4 ':include :size=500')