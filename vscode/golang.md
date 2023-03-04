# Golang Vscode Setup

## Installation

1. ติดตั้ง [Go for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=golang.go) extension
2. เปิด Command Palette (`Cmd+Shift+P`) เลือกไปที่ `Install/Update Tools command` และติดตั้ง tools ใน list ทุกตัว

![vscode-gotools](/images/vscode-gotools-install.jpg)

## Settings

สร้างไฟล์ `.vscode/settings.json` เข้าไปยัง root ของ project เพื่อกำหนด settings ให้กับ workspace

``` bash
├── foo
    ├── .vscode
    │   └──settings.json
    ...
```

ตัวอย่าง settings.json

``` json
{
    "editor.formatOnSave": true,
    "[go]": {
        "editor.defaultFormatter": "golang.go"
    },
    "go.useLanguageServer": true,
    "gopls": { 
        "ui.semanticTokens": true,
        "formatting.gofumpt": true
    }
}
```

## Reference

- [How to setup golang with vscode](https://dev.to/ko31/how-to-setup-golang-with-vscode-1i4i)
- [Go intellisense](https://code.visualstudio.com/docs/languages/go#_intellisense)
- [gofumpt](https://github.com/mvdan/gofumpt)
