# SiteOnlineCheckerBot. Just adjust the siteIPtoCheck variable to your desired.
```` Ruby
$Notification = 0
$siteIPtoCheck  = "8.8.8.8 or DNS Name"

Do{
    Write-Host 'Checking Connection...'
    $Online = Test-Connection -ComputerName $siteIPtoCheck -Count 1 -Quiet
    if ($Online){
        $Notification = 1
    }else {
        Start-Sleep -Seconds 5
    }

}While ($Notification -eq 0)

$TodaysDate = Date
Write-Host -BackgroundColor black -ForegroundColor green " Hello The test is successfully on $TodaysDate"
````

