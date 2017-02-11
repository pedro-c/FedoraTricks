#FedoraTricks

##Create a Desktop entry
Add a .desktop file to /usr/share/applications/
```
[Desktop Entry]
Type=Application
Encoding=UTF-8
Name=GitKraken
Comment=GitKraken
Exec=/usr/share/GitKraken/gitkraken
Icon=/usr/share/GitKraken/gitkraken.png
```
##Allow VPN connections in firewall
```
firewall-cmd --permanent --direct --add-rule ipv4 filter INPUT 0 -p gre -j ACCEPT
firewall-cmd --permanent --direct --add-rule ipv6 filter INPUT 0 -p gre -j ACCEPT
firewall-cmd --reload
```
