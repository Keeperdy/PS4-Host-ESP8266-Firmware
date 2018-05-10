# PS4-Host-ESP8266-Firmware OFW 4.55/Прошивка для ESP8266 PS4 Хост (ПО 4.55) (описание на русском смотрите внизу)

ATTENTION!
1. Best combination for gaming: Original+HEN (load one after another)
2. Best combination for dumper/backup: HEN+Dumper/Backup (load one after another, increases processing speed significantly)
3. If any payload does not work properly (no notifications, long uploading), just try to reload it

Here you can find ESP8266 custom firmware for hosting PS 4 payloads for 4.55 OFW ONLY. It is simple and light firmware without any tools like autopayload, firmware upgrade, ftp server for uploading files, etc. This firmware is mostly based on Al-Azif repo, but some payloads were modified for better stability/workability.

The payloads list includes:
- Original
- HEN
- HEN+VR (in version 2)
- BackUp
- App2USB
- FTP
- Dumper
- Enable Browser
- Disable/Enable Updates

Upload firmware in .bin format via NodeMCU-PyFlasher 3.0 

PS4 Wi-Fi Settings:
- Network: PS4
- Password: qwertyuiop
- DNS: 13.13.13.1
- Other settings: automatic

CREDITS TO 
Al-Azif, Specter, Qwertyoruiopz, Flatz, XVortex, Stooged, LightningMods, Anonymous, Marcelstoer, etc


# Прошивка для ESP8266
Данный репозиторий содержит прошивку для модуля ESP8266 с поднятием вэб-сервера для хоста эксполитов/пэйлоадов Playstation 4 для ПО 4.55

ВНИМАНИЕ!
1. Наиболее стабильная комбинация для игры: Original+HEN (запускать по очереди)
2. Для Dumper'а/BackUp'а использовать комбинацию: HEN+Dumper/BackUp (запускать по очереди, существенно увеличивается скорость проработки команды, например Backup = 4 мин без HEN против 20 сек. с предварительно запущенным HEN)
3. Если и случается ошибка или долгое время ничего не происходит с активацией пэйлоада (нет уведомления), попробуйте просто повторно его запустить

Данная прошивка отличается от подобных упрощенным интейрфесом с полным набором модифицированных и оригинальных пейлоадов, включая:
- Original
- HEN
- HEN+VR (in version 2)
- BackUp
- App2USB
- FTP
- Dumper
- Enable Browser
- Disable/Enable Update

Прошивка собрана на сборке Al-Azif, но все пейлдоады тщательно проверяются на работоспособность, а только потом внедряются в прошивку, т.к. были преценденты с Dumper/BackUp

Прошивка предоставляется в формате bin для заливки в модуль с помощью NodeMCU-PyFlasher 3.0

Настройки Wi-Fi для PS4:
- Сеть: PS4
- Пароль: qwertyuiop
- DNS: 13.13.13.1 (прописывается вручную)
- Остальные: автоматически

Особая благодарность разработчикам: Al-Azif, Specter, Qwertyoruiopz, Flatz, XVortex, Stooged, LightningMods, Anonymous, Marcelstoer и т.д.
