# Hole——密语输入法，从源头保障您的隐私安全

###### 本项目仅为密语输入法的开源部分，由于某些原因，密语输入法暂时不能全部开源，若造成不便，请谅解。

### 密语输入法版本
当前在售：v1.4.0（该版本因审核问题迟到）  
主要内容：新增高度调节，优化键盘按钮布局，修复大量重要bug，确保所有功能正常。  
详见[App Store](https://appsto.re/cn/RzEw_.i)  

即将开发：v1.5.0 开发Mac端解密工具，尝试实现拼音连打。  
延迟开发：v1.?.0 支持中文EMoji，添加RSA（需要重构加密模块，涉及兼容性问题，需要延后）

### 开源内容摘要
1. 服务器端实现代码（限于团队实力，为了保障安全，需借助公共集体智慧）  
2. 部分加密算法实现细节（以使有需要的人，在不使用本输入法时，只要有密钥，也能正常解密本输入法加密的内容）
3. 输入法所用词库（文件格式仅因开源方便而制成文本）

### 加密算法
1. 随机打乱（不适用于文件）  
2. 凯撒密码（仅适用于英文字母,文件转换为十六进制数，对其中的字母移位）
3. Base 64
4. 字典加密（目前涵盖Emoji字典、摩尔斯摩尔斯码表，加密能力以字典为限）
5. AES-256-ECB（加密后的数据使用Base 64输出）

### Licence

Unlicence

词库部分：

词库词汇来源：CC-CEDICT，License: http://creativecommons.org/licenses/by-sa/3.0/

词频信息来源：https://github.com/ling0322/webdict
