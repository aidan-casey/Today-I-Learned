# Completely Reset VSS Writers

To completely reset VSS writers, use the script below. First it will restart all the VSS services, and then it will re-register the DLL's.

```powershell
net stop vss /y && net start vss
net stop bits /y && net start bits
net stop certsvc /y && net start certsvc
net stop DFSR /y && net start dfsr
net stop DHCPServer /y && net start dhcpserver
net stop NtFrs /y && net start NtFrs
net stop srmsvc /y && net start srmsvc
net stop AppHostSvc /y && net start AppHostSvc
net stop IISADMIN /y && net start IISADMIN
net stop MSExchangeRepl /y && net start MSExchangeRepl
net stop MSExchangeIS /y && net start MSExchangeIS
net stop vmms /y && net start vmms
net stop MSMQ /y && net start MSMQ
net stop WSearch /y && net start WSearch
net stop EventSystem /y && net start EventSystem
net stop NTDS /y && net start NTDS
net stop OSearch /y && net start OSearch
net stop OSearch14 /y && net start OSearch14
net stop SMS_SITE_VSS_WRITER /y && net start SMS_SITE_VSS_WRITER
net stop SPSearch /y && net start SPSearch
net stop SPSearch4 /y && net start SPSearch4
net stop SQLWriter /y && net start SQLWriter
net stop CryptSvc /y && net start CryptSvc
net stop TermServLicensing /y && net start TermServLicensing
net stop WDSServer /y && net start WDSServer
net stop WIDWriter /y && net start WIDWriter
net stop WINS /y && net start WINS
net stop Winmgmt /y && net stop Winmgmt
net stop "System Event Notification Service"
net stop "Background Intelligent Transfer Service"
net stop "COM+ Event System"
net stop "Microsoft Software Shadow Copy Provider"
net stop "Volume Shadow Copy"
cd /d %windir%\system32
net stop vss
net stop swprv
regsvr32 /s ATL.DLL
regsvr32 /s comsvcs.DLL
regsvr32 /s credui.DLL
regsvr32 /s CRYPTNET.DLL
regsvr32 /s CRYPTUI.DLL
regsvr32 /s dhcpqec.DLL
regsvr32 /s dssenh.DLL
regsvr32 /s eapqec.DLL
regsvr32 /s esscli.DLL
regsvr32 /s FastProx.DLL
regsvr32 /s FirewallAPI.DLL
regsvr32 /s kmsvc.DLL
regsvr32 /s lsmproxy.DLL
regsvr32 /s MSCTF.DLL
regsvr32 /s msi.DLL
regsvr32 /s msxml3.DLL
regsvr32 /s ncprov.DLL
regsvr32 /s ole32.DLL
regsvr32 /s OLEACC.DLL
regsvr32 /s OLEAUT32.DLL
regsvr32 /s PROPSYS.DLL
regsvr32 /s QAgent.DLL
regsvr32 /s qagentrt.DLL
regsvr32 /s QUtil.DLL
regsvr32 /s raschap.DLL
regsvr32 /s RASQEC.DLL
regsvr32 /s rastls.DLL
regsvr32 /s repdrvfs.DLL
regsvr32 /s RPCRT4.DLL
regsvr32 /s rsaenh.DLL
regsvr32 /s SHELL32.DLL
regsvr32 /s shsvcs.DLL
regsvr32 /s /i swprv.DLL
regsvr32 /s tschannel.DLL
regsvr32 /s USERENV.DLL
regsvr32 /s vss_ps.DLL
regsvr32 /s wbemcons.DLL
regsvr32 /s wbemcore.DLL
regsvr32 /s wbemess.DLL
regsvr32 /s wbemsvc.DLL
regsvr32 /s WINHTTP.DLL
regsvr32 /s WINTRUST.DLL
regsvr32 /s wmiprvsd.DLL
regsvr32 /s wmisvc.DLL
regsvr32 /s wmiutils.DLL
regsvr32 /s wuaueng.DLL
sfc /SCANFILE=%windir%\system32\catsrv.DLL
sfc /SCANFILE=%windir%\system32\catsrvut.DLL
sfc /SCANFILE=%windir%\system32\CLBCatQ.DLL
net start "COM+ Event System"
```



