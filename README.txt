see:
https://github.com/user95f85f/fresh-debian

GIMP image editor and Notepad++ text editor
https://drive.google.com/open?id=1s_I7nCEzCfjuyIS9wcjhHYtaaFCh8Xb7
<recommended>
microsoft store cache reset:
1) open up admin cmd
2) WSReset.exe
DNS cache reset:
1) open up admin cmd
2) ipconfig /flushDNS
File explorer reset:
1) open up file explorer with Windows+E
2) View->Options->Clear button

<optional>
search "disk cleanup"
run "disk cleanup"
use the application.

<optional>
search "privacy settings"
Location -> Clear button location history

<optional>
open microsoft edge
go to "Settings"
go to "Privacy, search, services"
click the "Choose what to clear" button
set preferences and clear all.
https://support.hp.com/us-en/drivers/selfservice/hp-pavilion-gaming-15-cx0000-laptop-pc/20284020/model/21910720?sku=3VT93UA

install intel driver and support assistant
and HP software to automate the driver-installing process.
google "intel drivers" to get the intel driver and support assistant.

REM start microsoft-edge:http://people.oregonstate.edu/
start shell:AppsFolder\Microsoft.MicrosoftEdge_8wekyb3d8bbwe!MicrosoftEdge about:blank
REM <doesn't work>
REM start "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" about:blank


#open admin cmd
netsh winsock reset
#reboot

#open admin cmd
ipconfig /flushdns
ipconfig /release
ipconfig /renew

#<extra doings>
#Win+r -> %localappdata%
#delete Epic Games Launcher folder
#reboot
#</*>

# figure out system definiciencies
SFC /SCANNOW
DISM /ONLINE /CLEANUP-IMAGE /RESTOREHEALTH

# get system information
dxdiag
MSInfo32

# get network information
(ipconfig /all & ping www.google.com & netsh firewall show config & netsh interface ipv4 show subinterfaces & netsh interface ipv4 show ipstats) > "%USERPROFILE%\Desktop\NetworkInfo.txt"

Win+R should allow you to run common applications
* _battle_: play video games
* _bdo_: play black desert online
* _charmap_: run microsoft character map
* _calc_: run microsoft calculator
* _diablo_: play diablo two (ie. C:\DiabloII\Diablo II.exe)
* _edge_: run microsoft edge web browser
* _epic_: play video games
* _moon_: run stellarium
* _notepads_: run text file editor
* _source_: go to programming source code directory
* _steam_: play video games (ie. C:\Program Files (x86)\Steam\Steam.exe)
* _tos_: play tree of savior
* _visualstudio_: run visual studio ide
* _website_: goto my online helloworld website
* _website2_: goto localhost:8080
* _xterm_: run cygwin terminal (ie. C:\cygwin64\bin\mintty.exe)


Install golang and use `go build __RUN_APPLICATION.go`
put the output executable somewhere into your %PATH% (eg. C:\Go\bin\*)

__RUN_APPLICATION.go

package main

import (
	"log"
	"os/exec"
	"os"
)

func main() {
//"C:\DiabloII\Diablo II.exe" -w -direct -txt
//cmd := exec.Command("C:\\cygwin64\\bin\\mintty.exe", "-")
//err := os.Chdir("C:\\DiabloII")
//err := os.Chdir("C:\\Program Files (x86)\\Steam")
//err := os.Chdir("C:\\Program Files (x86)\\Battle.net")
//err := os.Chdir("C:\\Program Files\\Stellarium")
//  err := os.Chdir("C:\\Program Files (x86)\\Epic Games")
  err := os.Chdir("C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\Community\\Common7\\IDE")
  if err != nil {
    panic(err)
  }
//cmd := exec.Command("C:\\DiabloII\\Diablo II.exe", "-w", "-direct", "-txt")
//cmd := exec.Command("C:\\Program Files (x86)\\Steam\\Steam.exe")

//cmd := exec.Command("C:\\Program Files (x86)\\Battle.net\\Battle.net Launcher.exe")
//cmd := exec.Command("C:\\Program Files\\Stellarium\\stellarium.exe")
//cmd := exec.Command("C:\\Program Files (x86)\\Epic Games\\Launcher\\Portal\\Binaries\\Win32\\EpicGamesLauncher.exe")
//cmd := exec.Command("C:\\cygwin64\\bin\\mintty.exe", "-i", "/Cygwin-Terminal.ico", "-")
  cmd := exec.Command("C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\Community\\Common7\\IDE\\devenv.exe")
  
  log.Printf("Running command and waiting for it to finish...")
  //err2 := cmd.Run()
  err2 := cmd.Start()
  log.Printf("Command finished with error: %v", err2)
}


<BDO.bat>
cd "C:\Program Files (x86)\Steam\steamapps\common\Black Desert Online"
set __COMPAT_LAYER=RunAsInvoker
"Black Desert Online Steam Launcher.exe"
</BDO.bat>

<BDO TODO>
b key on the controller should be set to LeftStickEnter
and LeftStickEnter should be what b was
</BDO TODO>



<TOS.bat>
cd "C:\Program Files (x86)\Steam\steamapps\common\TreeOfSavior"
set __COMPAT_LAYER=RunAsInvoker
REM "C:\Program Files (x86)\Steam\Steam.exe" "steam://rungameid/372000"
"release\patch\tos.exe"
</TOS.bat>
Dragon's dogma
Sleeping dogs
STALKER: shadow of Chernobyl
Farcry 2
the Saboteur
Prototype
Mad max
strongly recommended things to do with a fresh cygwin & get:
1) lynx (to connect to google.com to search safely)
        (to connect to youtube.com to search safely)
2) nano (because why not)
3) perl/php/python2/python3 (EG. to get youtube-dl running and
   have a web server running on port 8080)
4) vim/vim-doc (to quickly edit files)
5) wget (a great way to download files from the Internet)

for games I recommend:
1) steam (for tree of savior)
2) battle.net (for WoW)
3) epic games launcher (for fortnite)

for a text editor I recommend getting Notepads App from the Windows Store
then to launch Notepads App you just go Win+R to run and then "notepads"

I recommend for high DPI systems to use Win++ to zoom in and Win+- to zoom out

<services disabled>
Printer Spooler and Remote * and Workstation stopped and disabled in 'services.msc'
</services disabled>

<performance tune-up>
Personalization -> color tab -> disable Transparency
Advanced System Settings -> performance -> set to best performance -> check enable font
</performance tune-up>

<applications>
go to Applications and uninstall as many as you can
go to Optional Windows Features and uninstall as many as you can
</applications>

<startup>
open task manager and go to Startup tab and disable as many items as possible
</startup>

<windows 10 privacy settings>
search "privacy" enter settings and disable as much as you can
</windows 10 privacy settings>

<set CMOS/Linux/BIOS time so that Linux can boot with correct time>
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation
RealTimeIsUniversal=1
</set*>

<to show recycle bin>
WIN+R-> shell:desktop
cmd-> start shell:desktop
</to*>


Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation
RealTimeIsUniversal=1

Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection
DisableRealtimeMonitoring=1
and you'll want to disable Tamper Protection within
  Windows Defender settings by clicking the
  Windows Defender icon in the tray
System Properties: disable remote assistance
Network configuration: network properties:
  uncheck IPv6 and
  uncheck File and Printer Sharing For Microsoft Networks
Windows Update Delivery Optimizations:
  disable "Allow downloads from other PCs"
System properties
 ->far right tab
 ->disable remote connections
