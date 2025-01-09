Collection of a useful bash commands

Identify your Wi-Fi interface:
`networksetup -listallhardwareports | awk '/Wi-Fi|AirPort/{getline; print $2}'`

Extract the SSID (Wi-Fi network name) and your current IP address:
`ipconfig getsummary en0 | awk -F'[=:] ' '/SSID/ {ssid=$2} /yiaddr/ {ip=$2} END {print "SSID: " ssid " | IP: " ip}'`
