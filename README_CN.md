# 在线反汇编器和汇编器

一个纯前端的在线汇编/反汇编器，支持多种 CPU 架构。所有处理都在浏览器本地完成，无需服务器。

**[在线演示](https://secnotes.github.io/onlineasm/)**

## 功能特性

- **反汇编器** - 将机器码转换为汇编指令
- **汇编器** - 将汇编代码转换为机器码
- 支持多种架构：ARM, ARM64, MIPS, x86, PowerPC, SPARC, SystemZ, XCore
- 支持小端和大端字节序
- 支持多种模式：16 位、32 位、64 位、ARM、Thumb 等
- x86 语法支持：Intel、AT&T、NASM、MASM、GAS
- 实时显示结果，支持一键复制
- 深色/浅色主题（自动检测浏览器偏好）
- 多语言支持（中文/英文）
- 响应式设计

## 截图

![截图](screenshot.png)

## 使用方法

### 反汇编器

1. 选择架构（ARM、ARM64、MIPS、x86 等）
2. 选择字节序（小端或大端）
3. 选择模式（16 位、32 位、64 位、ARM、Thumb 等）
4. 输入十六进制格式的机器码
5. 点击"反汇编"按钮
6. 如需复制结果，点击"复制结果"按钮

### 汇编器

1. 选择架构
2. 选择字节序和模式
3. 选择语法（仅 x86 架构）
4. 输入汇编代码（每行一条指令）
5. 点击"汇编"按钮
6. 复制生成的机器码

## 输入格式

### 反汇编器（十六进制输入）

支持多种格式：
- 空格分隔：`55 31 D2 89 E5`
- 连续输入：`5531D289E5`
- 换行分隔：
  ```
  55
  31 D2
  89 E5
  ```

### 汇编器（汇编代码）

每行一条指令：
```asm
push rbp
xor edx, edx
mov ebp, esp
mov eax, dword ptr [rbp+8]
```

## 技术栈

- **[Capstone.js](https://github.com/AlexAltea/capstone.js)** - 多架构反汇编框架
- **[Keystone.js](https://github.com/AlexAltea/keystone.js)** - 多架构汇编引擎
- 纯 HTML/CSS/JavaScript（无框架）
- 无需后端

## 浏览器支持

- Chrome（推荐）
- Firefox
- Safari
- Edge

## 本地开发

1. 克隆仓库
   ```bash
   git clone https://github.com/secnotes/onlineasm.git
   cd onlineasm
   ```

2. 在浏览器中打开 `index.html`

无需构建过程或依赖安装。

## 文件结构

```
onlineasm/
├── index.html          # 主应用程序
├── capstone.min.js     # Capstone 反汇编库
├── keystone.min.js     # Keystone 汇编库
├── README.md           # 英文说明
└── README_CN.md        # 中文说明
```

## 许可证

MIT License

## 致谢

- [Capstone](https://www.capstone-engine.org/) - 终极反汇编器
- [Keystone](http://www.keystone-engine.org/) - 汇编引擎
- [Capstone.js](https://github.com/AlexAltea/capstone.js) - Capstone 的 JavaScript 移植
- [Keystone.js](https://github.com/AlexAltea/keystone.js) - Keystone 的 JavaScript 移植

## 作者

[Security Notes](https://github.com/secnotes)