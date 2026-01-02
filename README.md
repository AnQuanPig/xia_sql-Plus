## Xia SQL Plus 公开终极版 V1.5.1x 
## 交流群
<img width="315" height="289" alt="image" src="https://github.com/user-attachments/assets/1977ad0c-d5cd-45d4-9d5b-acf030a0f261" />


### 插件介绍

迄今为止公开二开瞎注插件中最强版本：Xia SQL Plus，基于 "瞎注" xia_sql：https://github.com/smxiazi/xia_sql ，二次开发的 BurpSuite SQL 注入检测插件，专门用于检测各种数据格式中的 SQL 注入漏洞。插件支持多种参数格式的注入探测，具有高度可配置性和易用性。
<img width="1895" height="881" alt="image" src="https://github.com/user-attachments/assets/1c7a8e2b-f61b-484f-83f3-c543c116cb2f" />

------

### 核心功能

#### 1. **多格式参数检测支持**

- ✅ **URL 参数检测**：传统 GET/POST 参数
- ✅ **JSON 格式检测**：不再局限于简单Json，支持多层Json以及数组嵌套格式的检测
- ✅ **Multipart/form-data 检测**：支持文件上传表单数据包格式中的参数探测，精准识别参数
- ✅ **GraphQL 查询检测**：支持 GraphQL API 中的参数注入探测
- ✅ **URL 编码的 JSON 检测**：自动识别并解码 URL 编码的 JSON 参数
<img width="1895" height="885" alt="image" src="https://github.com/user-attachments/assets/87af2362-0900-4563-ab3d-1c13e1e0517d" />



#### 2. **智能 JSON 处理引擎**

- 🔄 **多层嵌套支持**：完整支持 JSON 对象、数组的多层嵌套结构
- 🔄 **动态路径解析**：自动识别 JSON 中所有可注入的字段
- 🔄 **值类型感知**：根据字段值类型（字符串、数字）智能选择 payload
 <img width="1865" height="875" alt="image" src="https://github.com/user-attachments/assets/61be959e-e505-4226-a218-674aa6bb21d4" />

#### 3. **高级匹配机制**

- 🎯 **强匹配检测**：针对 JSON 数组和多层嵌套的精确匹配
- 🎯 **上下文感知**：根据参数名/值内容自动调整 payload 策略，精准匹配参数值，为数值型则自动进行 -1、-0判断
- 🎯 **排序参数识别**：自动识别 limit、order、sort 等排序相关参数
<img width="1498" height="704" alt="image" src="https://github.com/user-attachments/assets/ccbff255-eca5-47c9-875d-121d959505eb" />


#### 4. **友好的响应分析**

- 📊 **长度变化检测**：精确计算响应包长度变化
- 📊 **差值显示策略**：
  - 变化 ≤ 6666：显示具体差值（如 "✔ 123"）
  - 变化 > 6666：显示 "✔ ==> ?"
  - 无变化：显示 "end!"
- 📊 **时间延迟检测**：响应时间 > 3s 时标记 "Time > 3s"
- 📊 **错误模式识别**：内置 70+ 种 SQL 错误模式正则表达式
- 📊 **结果显示顺序**：✔ 长度差值 Err Time > 3s
  - 有长度变化时：优先在结果中注入 ✔，表示响应变化异常，而后显示具体差值，如果变化超出 6666 则显示为 ✔ ==> ?
  - 检测页面报错：内置大量报错匹配正则表达式，精准匹配页面报错信息，检测到时在结果中注入提示词：Err
  - 检测响应时长：当响应时间超过3秒时，在结果中注入提示词：Time > 3s
<img width="1865" height="880" alt="image" src="https://github.com/user-attachments/assets/baa33740-881b-4f4b-87e8-698edb37c921" />



#### 5. **数据处理优化**

- 🔧 **自动去重机制**：基于请求特征 MD5 去重，避免重复测试
- 🔧 **白名单系统**：
  - 域名白名单：排除特定域名的检测
  - 参数白名单：排除特定参数名的检测
- 🔧 **静态文件过滤**：自动跳过图片、CSS、JS 等静态资源



#### 6. **Payload 自定义管理**

- 📂 **外部文件支持**：从 `~/xlzsql.txt` 加载自定义 payload
- 📂 **内置默认 payload**：8 条基础 SQL 测试 payload
- 📂 **实时编辑**：插件界面直接编辑 payload 列表
- 📂 **保存/重载**：支持保存到文件并实时重载
<img width="1864" height="885" alt="image" src="https://github.com/user-attachments/assets/133d9a9c-ea41-4263-9181-8d7ddb9ce78f" />

## 最新版本
 当前最新版本为 V1.6.6，有兴趣的师傅可以联系：XiLZ-B
<img width="1894" height="893" alt="image" src="https://github.com/user-attachments/assets/fbbcd13e-24a6-47fa-826e-8bb7d9c6724c" />
<img width="1889" height="890" alt="image" src="https://github.com/user-attachments/assets/d6491378-d95f-4d6c-9c18-30b0a26dde47" />
<img width="1153" height="495" alt="image" src="https://github.com/user-attachments/assets/44af5e70-a7cb-468d-bb12-d1a7f0eed717" />




