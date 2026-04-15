# SleepToAirPlane
SleepToAirplane is a simple program for Windows aiming at reducing battery drain while sleeping of laptops using Modern Standby (S0).
To do so, it automatically enables Airplane mode when the system enters the standby state and disables it upon wake-up. 

This turns off connectivity devices (Wi-Fi, Bluetooth, Cellular) while sleeping, which significantly reduces power consumption. If a laptop is frequently on Modern Standby mode while unplugged, this can achieve longer battery runtimes.

To monitor standby energy consumption, the integrated Windows tool `powercfg /sleepstudy` may be used via PowerShell and CMD.

> **_NOTE:_** While using the program, certain functionalities of Modern Standby (such as background updates or notifications) will not work.

## Utilization:
Simply run the executable. A console window will appear, logging the program's actions.

The following options can be used via the command line to modify the program's behavior:
- `h`: Hides the console window. The process must then be closed via Task Manager.
- `DisableSuspendAC`: Prevents Airplane Mode from being enabled when entering sleep if the AC adapter is plugged in.
- `DisableResumeAC`: Prevents Airplane Mode from being disabled when waking up if the AC adapter is plugged in.

The program may also be launched using a shortcut with the desired options (e.g. `SleepToAirPlane.exe h DisableSuspendAC`).
To run the program automatically at login, place a shortcut in the `shell:startup` folder.

### TODO
- Tasktray icon
- Startup Installer
