# Vscode Setup for golang

## Extensions 

1. ติดตั้ง [Go for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=golang.go) Extension ให้เรีบร้อย  
2. เปิด Command Palette โดยการกด `Cmd+Shift+P` และเลือกไปที่ `Install/Update Tools command` ติ๊กเลือก tools ที่อยู่ใน list ทุกตัวและ install

## Settings

เราสามารถเพิ่ม settings ให้กับ workspace ได้ด้วยการเพิ่ม `.vscode/settings.json` เข้าไปยัง root ของ project

``` bash
├── demoapp
    ├── .vscode
    │   └──settings.json
    ...
```

ตัวอย่าง settings.json

``` json
{
    "editor.formatOnSave": false,
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

- https://dev.to/ko31/how-to-setup-golang-with-vscode-1i4i
- https://code.visualstudio.com/docs/languages/go#_intellisense
- https://github.com/mvdan/gofumpt
