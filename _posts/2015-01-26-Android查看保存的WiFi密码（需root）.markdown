---
layout: post
title:  "Android查看保存到WiFi密码（需root）"
date:   2015-01-26 14:02:00
categories: Android
---

## 最近记忆力不太好，好久之前设置的WiFi因为太过久远以至于忘了连它所设置的各种密码（要搞的话得重置路由器~还别说，我上周末就干了一把。。。），有的时候拿到新设备想加WiFi加不上，蛮尴尬的~
有没有可能从连过的设备上查看那些WiFi的密码呢？？？答案是：能~

以Windows系统为例：
1、想查看Android手机所保存的WiFi密码，首先要保证设备是root过能拿到`su`（superuser）权限。
2、电脑上配有Android的开发环境，确保adb能用。
3、在命令行下输入一下命令
```bash
shell@android:/ $ su
su
shell@android:/ # cat -b /data/misc/wifi/wpa_supplicant.conf
```
4、然后设备里所保存的WiFi信息和密码都统统列到下面了
```bash
cat /data/misc/wifi/wpa_supplicant.conf
ctrl_interface=DIR=/data/misc/wpa_supplica
update_config=1
device_name=Wireless Client
manufacturer=MediaTek Inc.
model_name=MT6620
model_number=6620
serial_number=2.0
device_type=10-0050F204-5
os_version=01020300
config_methods=display push_button keypad


network={
        ssid="CMCC"
        key_mgmt=NONE
        priority=3
}

network={
        ssid="CMCC-EDU"
        key_mgmt=NONE
        priority=2
}

network={
        ssid="Mingway-PC"
        psk="1234567890"
        key_mgmt=WPA-PSK
        sim_slot="-1"
        imsi="none"
        pcsc="none"
        priority=1
}

network={
        ssid="Test-team"
        psk="0987654321"
        key_mgmt=WPA-PSK
        sim_slot="-1"
        imsi="none"
        pcsc="none"
        priority=5
}
```

### 引申一下，现在好多号称免费连全国WiFi的应用，据说也是获取到用户的WiFi密码然后上传到服务器再share给用户。回头看看有没有不root也拿的到设备里WiFi密码的方法么~~#