alert tcp $EXTERNAL_NET any -> $HOME_NET any (msg: "NMAP TCP Scan";sid:10000005; rev:2; classtype:TCP-Scan)
alert tcp $EXTERNAL_NET any  -> $HOME_NET any (msg:"Nmap XMAS Scan"; flags:FPU; sid:1000006; rev:1; classtype:Xmas-Scan)
alert tcp $EXTERNAL_NET any  -> $HOME_NET any (msg:"Nmap FIN Scan"; flags:F; sid:1000008; rev:1;classtype:FIN-Scan)



snort -i1 -A console -c C:\Snort\etc\snort.conf -l C:\Snort\log -A full
