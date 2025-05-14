# HideWindowsLockClock

Удаляем время на Windows с экрана блокировки и с экрана входа самым простым способом

1. Под администратором в Powershell запускаем(убрать экран блокировки, другие способы намного сложнее)
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Personalization" /v NoLockScreen /t REG_DWORD /d 1 /f
2. Аналогично и отображение времени на экране входа
reg add "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Authentication\LogonUI" /v ShowClock /t REG_DWORD /d 0 /f

