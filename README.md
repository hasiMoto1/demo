Invoke-Command -ComputerName Windows10 -ScriptBlock { Remove-Item -path E:\MyFolder -recurse } -credential admin
