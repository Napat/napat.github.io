# Golang Vscode Setup

## Installation

1. เปิด Vscode ขึ้นมาแล้วติดตั้ง extension ที่ชื่อว่า [Go for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=golang.go) ให้เรียบร้อย
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
    // Formater: gofumpt 
    "editor.formatOnSave": true,
    "[go]": {
        "editor.defaultFormatter": "golang.go"
    },
    "go.useLanguageServer": true,
    "gopls": { 
        "ui.semanticTokens": true,
        "formatting.gofumpt": true
    },
    
    // Unit Test
    "go.coverOnSave": true,
    "go.coverOnSingleTest": true,
    "go.coverageDecorator": {
        "type": "gutter",
        "coveredBorderColor" :  "rgba(64,128,128,0.5)",
        "uncoveredBorderColor" :    "rgba(128,64,64,0.25)",
        "coveredHighlightColor": "rgba(64,128,128,0.5)",
        "uncoveredHighlightColor": "rgba(128,64,64,0.25)",        
        "coveredGutterStyle": "blockgreen",
        "uncoveredGutterStyle": "blockred"
    },
    "go.coverageOptions": "showBothCoveredAndUncoveredCode",
}
```

## References

- [How to setup Golang with Vscode](https://dev.to/ko31/how-to-setup-golang-with-vscode-1i4i)
- [Go intellisense](https://code.visualstudio.com/docs/languages/go#_intellisense)
- [gofumpt](https://github.com/mvdan/gofumpt)
- [Unittest Vscode configuration](https://github.com/golang/vscode-go/blob/master/docs/settings.md#gocoveragedecorator)
