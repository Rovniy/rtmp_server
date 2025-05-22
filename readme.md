# RTMP Server

## Steps

1) Install Nodejs 22+ (https://nodejs.org/en/download)
2) Create folder C:/server
3) Move files into folder c:/server
4) In CMD run:
```bash
c:
cd /server
npm install
```
5) Create symlink of RTMP.bat and move to desktop
6) Run RTMP.bat symlink 

## node-media-server
https://www.npmjs.com/package/node-media-server/v/2.6.6

## Ports

Open 8000 port:
```bash
New-NetFirewallRule `
    -DisplayName "Open TCP 8000" `
    -Direction Inbound `
    -Protocol TCP `
    -LocalPort 8000 `
    -Action Allow
```

Open 1935:
```bash
New-NetFirewallRule -DisplayName "Open RTMP 1935" -Direction Inbound -Protocol TCP -LocalPort 1935 -Action Allow
```