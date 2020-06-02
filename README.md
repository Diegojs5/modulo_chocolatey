REQUISITOS PARA INSTALAÇÃO

Windows 7+ / Windows Server 2003+
PowerShell v2 + (o mínimo é a v3 para instalação neste site devido ao requisito do TLS 1.2 )
.NET Framework 4+ (a instalação tentará instalar o .NET 4.0 se você não o tiver instalado) (o mínimo é 4,5 para instalação neste site devido ao requisito do TLS 1.2 )

verifique se você está usando um shell administrativo - você também pode instalar como um não administrador, consulte Instalação Não Administrativa.

Instale com powershell.exe

Com o PowerShell, você deve garantir que Get-ExecutionPolicy não seja restrito. Sugerimos usar Bypasspara ignorar a política para instalar as coisas ou AllSignedpara um pouco mais de segurança.

EXECUTE Get-ExecutionPolicy. Se retornar Restricted, execute Set-ExecutionPolicy AllSignedou Set-ExecutionPolicy Bypass -Scope Process.

(Set-ExecutionPolicy Unrestricted)

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

CHOCOLATEY

Comando para validação choco ?
