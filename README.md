
test environ：windows 7  \
1 install sysmon: \
download sysmon:https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon \
downlaod conf.xml :https://raw.githubusercontent.com/gongwenbo/sysmon-config/master/sysmonconfig-export.xml \
open cmd by administor permission: Sysmon.ext -i sysmonconfig-export.xml

2 use EvSubscrib API get sysmon  \
https://docs.microsoft.com/en-us/windows/win32/wes/subscribing-to-events#pull-subscriptions 

3 modify EventCop\
    https://docs.microsoft.com/en-us/windows/win32/wes/eventschema-eventtype-complextype \
    https://docs.microsoft.com/en-us/windows/win32/wes/eventschema-systempropertiestype-complextype \
    LPWSTR pwsPath = L"Microsoft-Windows-Sysmon/Operational";    
    LPWSTR pwsQuery = L"*[System[EventID=12 or EventID=13]]"    
    LPWSTR pwsQuery = L" * " 


    
4 parse sysmon (xml) 
