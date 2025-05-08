# Quick Tip - How to compare text files using Powershell

Used the following to compare and export:
```Powershell
$File1 = "C:\SecureLocation\ExportReceiveConnector - Initial.csv"
$File2 = "C:\SecureLocation\Receive Connectors after HCW.csv"
$File3 = "compareresult.csv"

compare-object -ReferenceObject (Get-Content $file1) -DifferenceObject (Get-content $file2) | Export-Csv $File3
```

