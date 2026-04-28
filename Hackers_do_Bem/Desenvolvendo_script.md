# Scripts

Neste curso, você irá conhecer sobre os scripts de Windows e sua importância para a linguagem de programação. 
Conhecerá sobre as técnicas avançadas de desenvolvimento de scripts em Windows e as características e diferenças entre os sistemas Batch e PowerShell.

Além disso, aprenderá sobre os scripts do sistema Linux, as características de ambiente de desenvolvimento e como realizar 
a manipulação de arquivos mantendo a segurança no desenvolvimento de scipts. 

## arquivos de texto execultaveis



* **Power Shall**
* **Bash**
* **VBScript**
* **JavaScript**





### Alguns comandos Scripts

#### PowerShell
```
# Script para listar os processos em execução no sistema
Get-Process | Format-Tabel -AutoSize

# Script para criar um arquivo zip com os arquivos de uma pasta
$source = "C:\Users\user\Documents"
$destination = "C:\User\user\Documents.zip"
Compress-Archive -Path $source - DestinationPath $destination


# Script para enciar um email usando o Outlook
$Outlook = New-Object -ComObject Outlook.Application
$Mail = $Outlook.CreateItem(0)
$Mail.To = "destinatario@email.com"
$Mail.Subject = "Assunto do email"
$Mail.Body = "Corpo do email"
$Mail.Send()

```


#### Batch

```batch
:: Script para exibir a data e a hora atuais
echo %date% %time%

:: Script para copiar um arquivo para outra pasta
copy C:\Users\user\file.txt D:\Backup\file.txt

:: Script para executar um ping em um site
ping www.bing.com

```



#### VBScript
```
' Script para exibir uma mensagem na tela
MsgBox "Olá mundo!"

' Script para criar uma pasta no desktop
Set objFSO = CreateObject("Scripting.FileSystemObject")
strDesktop = objFSO.GetSpecialFolder(0)
objFSO.CreateFolder strDesktop & "\Nova Pasta"

' Script para abrir o Internet Explorer e navegar para um site
Set objIE = CreateObject("InternetExplorer.Application")
objIE.Visible = True
objIE.Navigate "https://www.bing.com"

```


## JavaScript
```
// Script para exibir uma mensagem na tela
WScript.Echo("Olá mundo!");

// Script para criar um arquivo de texto no desktop
var fso = new ActiveXObject("Scripting.FileSystemObject");
var desktop = fso.GetSpecialFolder(0);
var file = fso.CreateTextFile(desktop + "\\Arquivo.txt", true);
file.WriteLine("Este é um arquivo de texto criado por um script.");
file.Close();

// Script para abrir o Notepad e escrever algo nele
var shell = new ActiveXObject("WScript.Shell");
shell.Run("notepad.exe");
WScript.Sleep(1000);
shell.SendKeys("Este é um texto escrito por um script.");

```

# Avancados

### PowerShell
```
Write-Host "Hello, World!“
if ($a -gt $b) {
  Write-Host "A é maior que B"
} else {
  Write-Host "B é maior que A"
}
for ($i=1; $i -le 5; $i++) {
  Write-Host "Iteração $i"
}
function Saudacao {
  param ([string]$nome)Write-Host "Olá, $nome!"
}

# Chamando a função
Saudação -nome "Amigo"
function Saudacao {
  param ([string]$nome,[string]$cumprimento = "Olá")Write-Host "$cumprimento, $nome!"
}
# Chamando a função
Saudacao -nome "Amigo"
Saudacao -nome "Amigo" -cumprimento "Bom dia"


```


### Remoção de Malwares no Registro
```
$chaveMaliciosa = "HKCU:\Software\Microsoft\Windows\CurrentVersion\Run\EncryptorMalicioso"
if (Test-Path $chaveMaliciosa) {
  Write-Host "Removendo chave maliciosa do Registro..."
  Remove-Item -Path $chaveMaliciosa -Force
  Write-Host "Chave maliciosa removida com sucesso."
} else {
  Write-Host "Nenhuma chave maliciosa encontrada no Registro."
}
```

### Criptografia e Descriptografia de msg
```
# Encryption Key (16, 24, or 32 bytes)
$encryptionKey = [Text.Encoding]::UTF8.GetBytes("MySecretEncryptionKey")
# Text to encrypt
$textToEncrypt = "SENAI 123."
# Convert the text to bytes
$bytesToEncrypt = [Text.Encoding]::UTF8.GetBytes($textToEncrypt)
# Create AES encryption object
$aes = [System.Security.Cryptography.Aes]::Create()
$aes.Mode = [System.Security.Cryptography.CipherMode]::CBC
$aes.Padding = [System.Security.Cryptography.PaddingMode]::PKCS7
$aes = [System.Security.Cryptography.Aes]::Create()
$aes.Mode = [System.Security.Cryptography.CipherMode]::CBC
$aes.Padding = [System.Security.Cryptography.PaddingMode]::PKCS7

# Generate a random IV (Initialization Vector)
$aes.GenerateIV()
# Create an encryption stream
$encryptor = $aes.CreateEncryptor()
# Encrypt the bytes
$encryptedBytes = $encryptor.TransformFinalBlock($bytesToEncrypt, 0, $bytesToEncrypt.Length)
# Convert the encrypted bytes to Base64 for storage
$encryptedText = [Convert]::ToBase64String($aes.IV + $encryptedBytes)
# Display the encrypted text
Write-Host "Encrypted Text: $encryptedText"

# Convert the Base64 encrypted text back to bytes
$encryptedBytesWithIV = [Convert]::FromBase64String($encryptedText)
$iv = $encryptedBytesWithIV[0..15]
$encryptedBytesOnly = $encryptedBytesWithIV[16..($encryptedBytesWithIV.Length - 1)]
# Set the IV and decrypt
$aes.IV = $iv
$decryptor = $aes.CreateDecryptor()
$decryptedBytes = $decryptor.TransformFinalBlock($encryptedBytesOnly, 0, $encryptedBytesOnly.Length)
# Convert the decrypted bytes back to text
$decryptedText = [Text.Encoding]::UTF8.GetString($decryptedBytes)
# Display the decrypted text
Write-Host "Decrypted Text: $decryptedText"
```



### Verificação de Politicas de Segurança
```
Get-ExecutionPolicy
Get-ProcessMitigation-System
Get-MpPreference | Select-Object -Property *Detection*
#Este script exibe informações sobre a política de execução, políticas de mitigação de processo e preferências de 
# detecção do Windows Defender.
```

### Varredura de Portas e Conexões Ativas
```
Get-NetTCPConnection | Select-Object -Property LocalAddress, LocalPort, RemoteAddress, RemotePort, State
Test-NetConnection-ComputerName localhost -Port 80
Este script lista as conexões TCP ativas e verifica a conectividade com uma porta específica.

```

### Verificação de Atividades de Logon
```
Get-WinEvent-LogName Security | Where-Object { $_.Id -eq 4624 -or $_.Id -eq 4634 } | Select-Object -Property 
TimeCreated, Id, Message
Este script analisa eventos de logon no log de segurança do Windows.

```

### Analise de Processos Susppeitos
```
Get-Process | Where-Object { $_.Path -eq $null -and $_.Handles -gt 500 -and $_.CPU -gt 50 }
#Este script lista processos que não têm um caminho de arquivo associado, têm um número significativo de 
#identificadores de objeto ou estão usando uma quantidade considerável de CPU
```

