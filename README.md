# unifi-person-detector




Create startscript with the following content (Ubuntu 16.04)
```
/etc/systemd/system/upd.service

[Unit]
Description=Unifi Person Detector
After=multi-user.target

[Service]
Type=simple
Environment=DISPLAY=:1
WorkingDirectory=/repo/unifi_person_detector
User=pi
ExecStart=/repo/unifi_person_detector/upd.py
StandardError=syslog

[Install]
WantedBy=multi-user.target
```
```
Controll upd with:
systemctl start upd.service
systemctl stop upd.service
systemctl status upd.service
```
Install darknet with YOLO in /opt/darknet/ 
```
git clone https://github.com/AlexeyAB/darknet.git /opt/darknet
```
