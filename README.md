## TDLib (Alpine)

This is the TDLib precompiled binaries for Alpine Linux

### Install

```bash
apk add --no-cache curl
curl -L "https://github.com/zelenin/tdlib-alpine/releases/download/0.1.4/tdlib-1.3.0-r0.apk" > tdlib.apk
curl -L "https://github.com/zelenin/tdlib-alpine/releases/download/0.1.4/tdlib-dev-1.3.0-r0.apk" > tdlib-dev.apk
apk add --no-cache --allow tdlib.apk tdlib-dev.apk
rm tdlib*.apk
```
