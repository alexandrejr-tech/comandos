# Docker: reiniciar Docker Desktop travado

## Matar e reabrir (PowerShell)
```powershell
Stop-Process -Name "Docker Desktop" -Force
Start-Sleep 3
& "C:\Program Files\Docker\Docker\Docker Desktop.exe"
```
Fecha o Docker Desktop à força, espera 3 segundos e abre de novo.
