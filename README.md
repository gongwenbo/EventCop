# EventCop
Gets list of users who have tried to connect to your machine.
test environ：windows 7 
1 install sysmon:
download sysmon:https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon
downlaod conf.xml :https://raw.githubusercontent.com/gongwenbo/sysmon-config/master/sysmonconfig-export.xml 
open cmd by administor permission: Sysmon.ext -i sysmonconfig-export.xml

2 modify EventCop
    LPWSTR pwsPath = L"Microsoft-Windows-Sysmon/Operational";
    LPWSTR pwsQuery = L"*";
3 parse sysmon (xml) 
