1. 使用管理员打开 powershell
2. 一次执行下面的命令：
```
Stop-Process -Name "claude" -Force
Remove-Item -Path "$env:USERPROFILE\.local\bin\claude.exe" -Force
Remove-Item -Path "$env:USERPROFILE\.local\share\claude" -Recurse -Force

```

检查是否还有 claude,在终端输入 claude，找不到命令则是删除完毕。