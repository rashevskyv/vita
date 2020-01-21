---
title: "Обновление ПО до 3.65 (PS TV)"
redirect_from: /updating-firmware-ps-tv-365-and-368
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Эксплойт h-encore совместим только с приставками, версия системного ПО которых 3.65 и выше. Поэтому консоли с другой версией прошивки должны быть обновлены при помощи кастомного приложения для обновлений, чтобы использовать этот эксплойт.

Несмотря на то, что h-encore совместим с системным ПО даже последней версии, только на 3.65 и 3.60 есть Ensō - эксплойт, который срабатывает при загрузке приставки, тем самым исключая необходимость запускать прошивку после каждого выключения или перезагрузки PS Vita

Обратите внимание, что кастомное приложение для обновлений может лишь увеличить версию прошивки, но не понизить её. Если ваша прошивка выше, чем 3.65, вернитесь к [Началу](get-started) и выберите вашу версию прошивки.

### Что понадобится

* Отформатированный в FAT32 USB-накопитель, имеющий 150 МБ свободного места
    + [torrent](magnet:?xt=urn:btih:5f2437f2141408c925ffc5d81ff76e94e1a4c493&dn=PSP2UPDAT.PUP&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker3.itzmx.com%3A6961%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce&tr=udp%3A%2F%2Fdenis.stalker.upeer.me%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker1.itzmx.com%3A8080%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker4.itzmx.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce)
    * [WebArchive](https://web.archive.org/web/20180630222648id_/http://dus01.psp2.update.playstation.net/update/psp2/image/2017_0317/rel_0a0f2a9ae58968ac5d1d2127049c3cba/PSP2UPDAT.PUP)
    * [YD](https://yadi.sk/d/gqbm9Tk3tNtvbA)
    * [GD](https://drive.google.com/file/d/12JGlB-GZM58LS50LK57oeh65MDsSh4i4)
    * [MEGA](https://mega.nz/#!Y1VjVQ7D!i3kzQ7Hhf9tAdebJcSQEs1ieNIAYzt-ts475YwstGuM)

### Инструкция

#### Часть I - Подготовка накопителя

1. Создайте папку `PSVITA` в корне USB-накопителя
1. Создайте папку `UPDATE` внутри папки `PSVITA` на USB-накопителе
1. Переименуйте скачанный файл `PSP2UPDAT.PUP` в `PSVUPDAT.PUP`
1. Переместите файл `PSVUPDAT.PUP` в созданную папку `UPDATE`

#### Часть II - Обновление прошивки

1. Полностью выключите PS TV
1. Держите нажатой кнопку питания не менее 7 секунд, чтобы загрузиться в безопасный режим
1. Подключите контроллер с помощью USB кабеля, затем нажмите кнопку (PS)
1. Перейдите в `Обновить системное ПО` -> `Обновить из накопителя USB`
1. Подключите USB-накопитель к PS TV
1. Следуйте инструкциям на экране, чтобы обновить консоль
  + После завершения процесса консоль перезагрузится автоматически

___

### Следующий шаг: [Установка h-encore](installing-h-encore)
{: .notice--success}
