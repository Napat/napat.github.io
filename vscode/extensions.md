# Vscode workspace recommended extensions

เราสามารถแนะนำ vscode extensions สำหรับ repository ได้โดยการเพิ่มไฟล์ `extensions.json` ไว้ใน .vscode  
เมื่อคนอื่น clone repository ไปเปิดด้วย vscode ก็จะมีหน้าต่างขึ้นมาแนะนำให้ติดตั้ง entensions ตามชื่อที่เราใส่เอาไว้

ตัวอย่างไฟล์ `extensions.json`

``` json
{
    "recommendations": [
        "golang.go", 
        "mhutchie.git-graph",
        "humao.rest-client", 
        "redhat.vscode-yaml", 
        "tabnine.tabnine-vscode", 
        "bierner.markdown-mermaid",
        "aykutsarac.jsoncrack-vscode", 
        "naumovs.color-highlight", 
        "ms-azuretools.vscode-docker",
        "ritwickdey.liveserver", 
        "davidanson.vscode-markdownlint", 
        "quicktype.quicktype",
        "ms-vscode-remote.remote-containers"
    ],
    "unwantedRecommendations": []
}
```

## References

- [Workspace recommended extensions](https://code.visualstudio.com/docs/editor/extension-marketplace#_workspace-recommended-extensions)
