# Online Disassembler and Assembler

[English](README.md) | [中文](README_CN.md) | [Live Demo](https://secnotes.github.io/onlineasm/)


A pure frontend online disassembler and assembler supporting multiple CPU architectures. All processing is done locally in the browser, no server required.

## Features

- **Disassembler** - Convert machine code to assembly instructions
- **Assembler** - Convert assembly code to machine code
- Support for multiple architectures: ARM, ARM64, MIPS, x86, PowerPC, SPARC, SystemZ, XCore
- Little-Endian and Big-Endian support
- Multiple modes: 16-bit, 32-bit, 64-bit, ARM, Thumb, etc.
- x86 syntax support: Intel, AT&T, NASM, MASM, GAS
- Real-time results with copy functionality
- Dark/Light theme (auto-detect browser preference)
- Multilingual support (English/Chinese)
- Responsive design

## Screenshots

![Screenshot](screenshot.png)

## Usage

### Disassembler

1. Select architecture (ARM, ARM64, MIPS, x86, etc.)
2. Select endianness (Little-Endian or Big-Endian)
3. Select mode (16-bit, 32-bit, 64-bit, ARM, Thumb, etc.)
4. Enter machine code in hexadecimal format
5. Click "Disassemble" button
6. Copy results if needed

### Assembler

1. Select architecture
2. Select endianness and mode
3. Select syntax (x86 only)
4. Enter assembly code (one instruction per line)
5. Click "Assemble" button
6. Copy generated machine code

## Input Formats

### Disassembler (Hex Input)

Supports multiple formats:
- Space-separated: `55 31 D2 89 E5`
- Continuous: `5531D289E5`
- Line-separated:
  ```
  55
  31 D2
  89 E5
  ```

### Assembler (Assembly Code)

One instruction per line:
```asm
push rbp
xor edx, edx
mov ebp, esp
mov eax, dword ptr [rbp+8]
```

## Technology Stack

- **[Capstone.js](https://github.com/AlexAltea/capstone.js)** - Multi-architecture disassembly framework
- **[Keystone.js](https://github.com/AlexAltea/keystone.js)** - Multi-architecture assembler engine
- Pure HTML/CSS/JavaScript (no frameworks)
- No backend required

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Local Development

1. Clone the repository
   ```bash
   git clone https://github.com/secnotes/onlineasm.git
   cd onlineasm
   ```

2. Open `assembler.html` in your browser

No build process or dependencies required.

## File Structure

```
onlineasm/
├── assembler.html      # Main application
├── capstone.min.js     # Capstone disassembler library
├── keystone.min.js     # Keystone assembler library
├── README.md           # English README
└── README_CN.md        # Chinese README
```

## License

MIT License

## Credits

- [Capstone](https://www.capstone-engine.org/) - The ultimate disassembler
- [Keystone](http://www.keystone-engine.org/) - The assembler engine
- [Capstone.js](https://github.com/AlexAltea/capstone.js) - JavaScript port of Capstone
- [Keystone.js](https://github.com/AlexAltea/keystone.js) - JavaScript port of Keystone

## Author

[Security Notes](https://github.com/secnotes)