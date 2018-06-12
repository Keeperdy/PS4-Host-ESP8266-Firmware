# NB!!! STOLEN CODE FROM C0d3m4st4
Hi, guys! Concerning situation with c0d3m4st4 code used in my ESP firmwares - he blames me his code being stolen and used by me - I want to make it clear that it's just **a stupid mistake**, specifically, my mistake that I did not clear ESP flash memory before uploading any sketch in it. However, I've just found this function, too late. So, if you use somebody's firmware and then upload your sketch via Arduino (Not NodeMCU-flasher) over it, it will replace only sketch code and allocate SPIFF files in flash memory according to their size. The rest is unchanged, so if you firmware is smaller than all 4Mb, you can find the traces of previously loaded firmwares to ESP code!

The same happened with me:
- My first ESP firmware releases were beta, I tried to improve arduino code - debugging
- Some day I flashed my ESP with c0d3m4st4 firmware (I had some problem with dumper payload)
- After sometime I uploaded my new sketch via Arduino IDE without erasing c0d3m4st4 firmware from flash. I was pretty sure that Arduino IDE makes it by default, but not - I've already found this function, but too late.
- So that how it happened - some part of his code left in my firmware because I did not use all 4Mb flash memory size. His code is inactive - it's clear - because there is no links to it in basic sketch! It's just my fualt not to clear everything properly before making something own!

My firmware is written from the scratch, using Arduino in-built examples and modified by me!!! **I NEVER TOOK OR STOLE ANYONE'S WORK TO PRESENT IT LIKE MY OWN!!!**

I made a video of a full process where you can see how it works! Video: https://drive.google.com/open?id=1_Drp0A0sBM5yU9vVWsz9NjdxsnubvqVm … The file is over 700 Mb with step-by-step comments.

    Flashing ESP with blank 4mb bin file
    Uploading my sketch and dump bin file
    Checking it in WinHex (it crashes sometimes) for c0d3m4st4's code - no traces
    Flashing ESP with his last FW
    Upload again the SAME my sketch without full erasing of the c0d3m4st4's content and dumping a bin file again
    Finding with WinHex the pieces of his code!!!

Now I will clear all my firmwares from c0d3m4st4's code traces (and probably other devs too) and update them on Github!!! Sorry for inconveniences!!!


# PS4-Host-ESP8266-Firmware OFW 4.55/Прошивка для ESP8266 PS4 Хост (ПО 4.55) (описание на русском смотрите внизу)

**ATTENTION!**
1. Best combination for gaming: Original+HEN (load one after another)
2. Best combination for dumper/backup: HEN+Dumper/Backup (load one after another, increases processing speed significantly)
3. HEN in this repo is spoofed. One can play games, dumped on FW >4.55
4. If any payload does not work properly (no notifications, long uploading), just try to reload it

Here you can find ESP8266 custom firmware for hosting PS 4 payloads for 4.55 OFW ONLY. It is simple and light firmware without any tools like autopayload, firmware upgrade, ftp server for uploading files, etc. This firmware is mostly based on Al-Azif repo, but some payloads were modified for better stability/workability.

The payloads list includes:
- Original
- HEN
- HEN+VR
- BackUp
- App2USB
- FTP
- FTP+RW
- Dumper
- Enable Browser
- Disable/Enable Updates

**PS4 Wi-Fi Settings (EASY):**
- Network: PS4
- Password: qwertyuiop

"Test internet connection" also passes successfully with such settings!

Upload firmware in .bin format via NodeMCU-PyFlasher 3.0 

**CREDITS TO:** 

Al-Azif, Specter, Qwertyoruiopz, Flatz, XVortex, Stooged, LightningMods, Anonymous, Marcelstoer, etc


# Прошивка для ESP8266
Данный репозиторий содержит прошивку для модуля ESP8266 с поднятием вэб-сервера для хоста эксполитов/пэйлоадов Playstation 4 для ПО 4.55

**ВНИМАНИЕ!**
1. Наиболее стабильная комбинация для игры: Original+HEN (запускать по очереди)
2. Для Dumper'а/BackUp'а использовать комбинацию: HEN+Dumper/BackUp (запускать по очереди, существенно увеличивается скорость проработки команды, например Backup = 4 мин без HEN против 20 сек. с предварительно запущенным HEN)
3. HEN в составе сборки сожержит спуф. Возможно запускать игры, которые были сдампены на ПО >4.55.
4. Если и случается ошибка или долгое время ничего не происходит с активацией пэйлоада (нет уведомления), попробуйте просто повторно его запустить

Данная прошивка отличается от подобных упрощенным интейрфесом с полным набором модифицированных и оригинальных пейлоадов, включая:
- Original
- HEN
- HEN+VR
- BackUp
- App2USB
- FTP
- FTP+RW
- Dumper
- Enable Browser
- Disable/Enable Update

Прошивка собрана на сборке Al-Azif, но все пейлдоады тщательно проверяются на работоспособность, а только потом внедряются в прошивку, т.к. были преценденты с Dumper/BackUp

Прошивка предоставляется в формате bin для заливки в модуль с помощью NodeMCU-PyFlasher 3.0

**Настройки Wi-Fi для PS4 (режим "ПРОСТОЙ"):**
- Сеть: PS4
- Пароль: qwertyuiop

С данными настройками так же успешно проходится тест на подключение к интернету!

**Особая благодарность разработчикам:**

Al-Azif, Specter, Qwertyoruiopz, Flatz, XVortex, Stooged, LightningMods, Anonymous, Marcelstoer и т.д.
