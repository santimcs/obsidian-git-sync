	if taskbar icons do not show correctly then run powershell terminal
	and execute this command
	 Stop-Process -Name explorer -Force
	Remove-Item -Path   "$env:LOCALAPPDATA\Microsoft\Windows\Explorer\IconCache*" -Force
	Start-Process explorer.exe
