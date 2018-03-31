---
permalink: /finalizing-setup.html
title: Завершение установки
author_profile: true
---
{% include toc title="Разделы" %}

#### Описание шагов

В процессе мы установим и настроим следующие программы:

* **MaiDumpTool** *(позволяет дампить картриджи и устанавливать цифровые версии игр)*
* **TEMA** *(позволяет устанавливать кастомные темы для LiveArea и VitaShell)*
* **Adrenaline** *(ePSP CFW)*
* **Download Enabler** *(плагин, позволяющий скачивать файлы через браузер Vita в ux0:download)*
* **Save Manager** *(программа для дампа и восстановления сохранений)*
* **ТОЛЬКО PSTV: AntiBlacklist** *(программа, которая позволяет запускать на PSTV все игры от PS Vita)*

<div class="notice--info">{{ notice-2 | markdownify }}</div>

#### Что понадобится

* FTP-клиент, например [FileZilla](https://filezilla-project.org/download.php)
* Интернет соединение на PS Vita
* Свежая версия [MaiDumpTool](https://github.com/LioMajor/MaiDumpToolEN/releases/latest)
* Свежая версия [TEMA](https://github.com/Mithrenes/TEMA/releases/latest)
* Свежая версия [Adrenaline](https://github.com/TheOfficialFloW/Adrenaline/releases)
* Свежая версия [vita-savemgr](https://github.com/d3m3vilurr/vita-savemgr/releases/latest)
* Свежая версия [Download Enabler](https://github.com/TheOfficialFloW/DownloadEnabler/releases/latest)
* **Только PS TV:** [AntiBlacklist v1.2](http://vitadb.rinnegatamante.it/#/info/11)

#### Инструкции

##### Часть I - Подготовительные работы

1. Запустите VitaShell на PS Vita и нажмите (SELECT), чтобы активировать FTP-сервер.
2. Соединитесь с Vita, используя ваш FTP-клиент.
3. Скопируйте `MaiDumpTool_Vxxx.xxxx_eng.vpk` в папку `ux0:` на вашей PS Vita.
4. Скопируйте `TEMA.vpk` в папку `ux0:` на вашей PS Vita.
5. Скопируйте `Adrenaline.vpk` в папку `ux0:` на вашей PS Vita.
6. Скопируйте `savemgr.vpk` в папку `ux0:` на вашей PS Vita.
7. Скопируйте `download_enabler.suprx` в папку `ux0:tai/` на вашей PS Vita.
8. **Только PS TV:** Скопируйте `AntiBlacklist.vpk` в папку `ux0:` на вашей PS Vita.
    
    ![]({{ base_path }}/images/screenshots/finalizing-setup-file-layout.png) {: .notice--info}

9. Нажмите ⭕ на приставке для остановки FTP-сервера.

##### Часть II - Установка программ

1. Находясь в VitaShell, перейдите в папку `ux0:`.
2. Выберите `MaiDumpTool_Vxxx.xxxx_eng.vpk` и нажмите (X) для начала установки
3. Выберите `TEMA.vpk` и нажмите (X) для начала установки
4. Выберите `Adrenaline.vpk` и нажмите (X) для начала установки
5. Выберите `savemgr.vpk` и нажмите (X) для начала установки
6. **Только PS TV:**  Выберите `AntiBlacklist.vpk` и нажмите (X) для начала установки
7. Закройте VitaShell.

##### Часть III - Установка Adrenaline

1. Запустите Adrenaline
2. Нажмите X для загрузки файла 661.PBP.
3. После того как Adrenaline закроется, запустите его повторно.
4. Нажмите X для установки прошивки 6.61 ePSP.
5. После окончания установки, нажмите Х для загрузки в PSP XMB.
6. Настройте ePSP.
7. Дважды нажмите кнопку PS, чтобы выйти из эмулятора PSP.
9. Добавьте следующую строку в `ux0:tai/config.txt` под строкой `*KERNEL`: `ux0:app/PSPEMUCFW/sce_module/adrenaline_kernel.skprx`.

##### Часть IV - Настраиваем Download Enabler

1. Добавьте следующую строку в `ux0:tai/config.txt` под строкой `*main`: `ux0:tai/download_enabler.suprx`.

##### Section V - PS TV ONLY: Setting up AntiBlacklist

1. (TODO: need to find someone with a pstv to help with this or just buy a pstv myself)

##### Section VI - Cleaning up

1. You may now delete the `.vpk` files from the `ux0:` folder on your Vita.

* * *

{% capture notice-6 %}  
You will now have homebrew access every time you power on your Vita. TaiHEN plugins will now be loaded at boot, you can disable plugin loading by holding L during boot. {% endcapture %}

<div class="notice--info">{{ notice-6 | markdownify }}</div>

For information on using MaiDumpTool to dump and install your games, check out the [MaiDumpTool Usage](maidumptool-usage) page. {: .notice--success}

For information on the SD2Vita, the cartridge slot MicroSD Adapter check out the [SD2Vita Information and Setup](sd2vita-info-setup) page. {: .notice--success}