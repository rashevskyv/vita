---
title: "Завершение установки"
---

{% include toc title="Содержание" %}

## Выберите версию вашей консоли:

<div class=".select_fw__wrapper">
    <div class="select_fw">
        <input type="radio" id="365" name="fw" value="365" checked>
        <label for="365">PS Vita</label>
        <input type="radio" id="370" name="fw" value="370" />
        <label for="370">PS Vita TV</label>
    </div>
</div>

## Обязательно к прочтению

Мы установим и настроим следующие приложения и плагины:
+ **[NoNpDrm](https://github.com/TheOfficialFloW/NoNpDrm)** - позволяет использовать зашифрованные игры и приложения
+ **[0syscall6](https://github.com/SKGleba/0syscall6)** - позволяет прозрачно расшифровывать игры и приложения на любой версии прошивки
+ **[rePatch reDux0](https://github.com/dots-tb/rePatch-reDux0)** - позволяет использовать модификации на манер LayeredFS y 3DS или Switch
+ **[FdFix](https://github.com/TheOfficialFloW/FdFix)** - патч, предотвращающий зависание homebrew после спящего режима 
+ **[DownloadEnabler](https://github.com/TheOfficialFloW/VitaTweaks/releases/tag/DownloadEnabler) + [iTLS](https://github.com/SKGleba/iTLS-Enso)** - позволяет скачивать файлы любых типов с помощью браузера
+ **[notrophymsg](https://github.com/TheOfficialFloW/VitaTweaks/releases/tag/NoTrophyMsg)** - убирает назойливое сообщение про трофеи, при использовании homebrew
+ **[shellbat](https://github.com/nowrep/vita-shellbat)** - отображает процент заряда батареи в строке состояния
+ **[pngshot](https://github.com/xyzz/pngshot)** - улучшает встроенную утилиту для скриншотов
+ **[PSVShell](https://github.com/Electry/PSVshell)** - плагин для разгона процессора и GPU приставки 
+ **[NoPowerLimitsVita](https://github.com/Electry/NoPowerLimitsVita)** - плагин, снимающий ограничения на максимальную яркость экрана и использование WiFi в некоторых играх
+ **[Quick Menu Plus](https://forum.devchroma.nl/index.php/topic,78.0.html)** - плагин, добавляющий кнопки выключения и перезагрузки приставки, а так же регуляторы громкости,  в быстрое меню. Для перезагрузки приставки удерживайте кнопку "**Power Off・Restart**"
+ **[JAV](https://forum.devchroma.nl/index.php/topic,46.0.html)** - Плагин запоминает уровень громкости для динамиков, наушников и bluetooth, и автоматически переходит на нужный уровень громкости при смене устройства воспроизведения
+ **[Adrenaline](https://github.com/TheOfficialFloW/Adrenaline)** - это программа, которая модифицирует официальный эмулятор PSP, чтобы он запускал специальную прошивку PSP 6.61. В итоге, запустив Adrenaline, вы сможете использовать PSP и почти все её возможности в привычном для пользователей PSP окружении 
+ **[pkgj](https://github.com/blastrock/pkgj)** - приложение, позволяющее качать и распаковывать игры для PS Vita прямо на приставке 
+ **[VitaShell](https://github.com/TheOfficialFloW/VitaShell/releases/latest)** - файловый менеджер, способный так же устанавливать `vpk-файлы` приложений
+ **[TF-Card-Plugin-Tool](https://github.com/theheroGAC/TF-Card-Plugin-Tool)** - **опциональный** плагин, позволяющий монитровать обычную SD-карту через специальный переходник, вставляемый в слот картриджа приставки
+ **[Application Storage Manager](https://bitbucket.org/Lupo511/appstoragemanager/downloads/)** - программа, позволяющая заменить системное приложение своим, что позволит не остаться без VitaShell даже при случайном его удалении
+ **[Vita 3G Disabler](https://www.psx-place.com/threads/release-ps-vita-3g-disabler.14652/)** - **опционально** для приставок с 3G-модулем, чтобы отключить его назойливые ошибки
{% capture notice-1 %}
+ **[DolcePolce](https://github.com/KuromeSan/DolcePolce)** - плагин, снимающий ограничения на запуск некоторых приложений на PS Vits TV, а так же приложений от PS Vita TV на обычной PS Vita
+ **[DSMotion](https://github.com/OperationNT414C/DSMotion)** - плагин, активирующий возможность управления гироскопом на DualSchock-контроллере. Необходим для тех игр на PS Vita TV, которые подразумевают управление движением на PS Vita. 
+ **[FakeCamera](https://github.com/OperationNT414C/FakeCamera)** - плагин, необходимый для запуска тех игр, которым необходима камера для правильной работы. 
{% endcapture %}
<div class="hideble 370 hide">{{ notice-1 | markdownify }}</div>

## Что понадобится

* Свежая версия {% include inc/sdfiles.md %}

## Инструкция

### Часть I - Подготовительные работы

{% capture notice-1 %}
Выполните следующее, если ещё не скидывали на приставку {% include inc/sdfiles.md %}:
{: .notice--success}

1. Скачайте и разархивируйте {% include inc/sdfiles.md %} на ПК в удобное для вас место
{% include inc/mount_vs_usb.md %}
1. На ПК, на примонтированном диске, удалите папку `tai`
    * Если вы уже удаляли эту папку на предыдущих страницах, пропустите этот шаг
    * Если вы не можете найти эту папку, убедитесь, что вы [настроили проводник](https://customfw.xyz/file-extensions-windows) для отображения всех файлов и папок на диске
    * Если папки всё равно нет, отключите PS Vita от ПК и убедитесь, что и в VitaShell её тоже нет 
1. Скопируйте содержимое {% include inc/sdfiles.md %} на PS Vita удобным для вас способом
    * Если вы не знаете как перенести файлы на PS Vita, [воспользуйтесь этой  инструкцией](vitashell#доступ-к-памяти-приставки-через-пк){:target="_blank"}
1. Нажмите {% include inc/btn.md btn="CIRCLE" %} на консоли чтобы отключить PS Vita от ПК
{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>

### Часть II - Установка VPK

1. Установите следующие файлы из папки `ux0:/VPK`
    * **Если вы не знаете как устанавливать `vpk-файлы` на PS Vita, [воспользуйтесь этой  инструкцией](vitashell#установка-файлов-в-формате-vpk){:target="_blank"}**
    * `Adrenaline_offline.vpk`
    * `AppStorageManager.vpk`
    * `iTLS-Enso.vpk`
    * `pkgj.vpk`
    * `disable_3g.vpk` - только в том случае, если у вас PS Vita с 3G-модулем
    * `TF.Card.Plugin.Tool.vpk` - только в том случае, если вы планируете использовать с PS Vita переходник sd2vita и microSD-карту. О настройке и использовании sd2vita мы поговорим [отдельно](sd2vita){:target="_blank"}
    * `VitaShell.vpk` - только в том случае, если он у вас не установлен
1. Выйдите в главное меню PS Vita, нажав на кнопку {% include inc/btn.md btn="PS" %}
    
### Часть III - Настройка системы 

1. Запустите "**iTLS-Enso**"
    1. Выберите "**Install the full iTLS package**" и нажмите {% include inc/btn.md btn="CROSS" %}, чтобы начать установку сертификатов
    1. Дождитесь окончания установки и выйдите в главное меню PS Vita, нажав на кнопку {% include inc/btn.md btn="PS" %}
    1. Перезапустите приставку
1. Запустите "**Adrenaline**"
    * Если приложение закрылось, запустите его повторно. Ниже, после установки плагинов, этот недостаток будет исправлен
    1. Нажмите {% include inc/btn.md btn="CROSS" %}, чтобы начать установку Adrenaline
    1. Когда на экране появится надпись "**The firmware has been installed successfully**", нажмите {% include inc/btn.md btn="CROSS" %}, чтобы запустить Adrenaline 
    1. Настройте его, затем нажмите дважды на кнопку {% include inc/btn.md btn="PS" %}, чтобы выйти в главное меню PS Vita и закройте Adrenaline
        * Подробнее об использовании Adrenaline, можно почитать на странице [Adrenaline](adrenaline){:target="_blank"}
1. Запустите "**AppStorageManager**"
    1. Выберите "**Memory Card -> Internal Storage**"
        1. Выберите "**[VITASHELL] VitaShell**"
            1. Нажмите {% include inc/btn.md btn="CROSS" %} для  подтверждения перемещения
            1. Нажмите {% include inc/btn.md btn="CROSS" %} для продолжения работы, как только на экране появится зелёная надпись
        1. Выберите "**[TFCARDPL0] TF Card Plugin Tool**", если таковой устанавливался на приставку
            1. Нажмите {% include inc/btn.md btn="CROSS" %} для  подтверждения перемещения
            1. Нажмите {% include inc/btn.md btn="CROSS" %} для продолжения работы, как только на экране появится зелёная надпись
    1. Выйдите в главное меню PS Vita, нажав на кнопку {% include inc/btn.md btn="PS" %}
1. Запустите "**3G Disabler**", если в вашей PS Vita есть 3G-модуль и вы устанавливали это приложение
    1. Нажмите {% include inc/btn.md btn="CROSS" %}, чтобы отключить функции 3G на PS Vita
    1. Выйдите в главное меню PS Vita, нажав на кнопку {% include inc/btn.md btn="PS" %}
    
### Часть IV - Установка плагинов

1. Запустите **VitaShell**
1. Удалите папку `tai` из раздел `ux0:`, если таковая тут есть
1. Перейдите в `ux0:/plugins`
1. Переместите папку `tai` из папки `ux0:/plugins` в корень раздела `ur0:` с заменой (если таковая потребуется)
    * **ОБРАТИТЕ ВНИМАНИЕ**, мы переносим папку из раздела u**x**0 в раздел u**r**0!
    * Для перемещения, нажмите {% include inc/btn.md btn="TRIANGLE" %} на выбранной папке и выберите `Move`
    * Для того, чтобы вставить скопированное в другую папку, зайдите в папку, в которую хотите скопировать данные, нажмите {% include inc/btn.md btn="TRIANGLE" %} и выберите `Paste`
{% capture notice-1 %}
{:start="12"}
1. Перейдите в папку `tai` на диске, которым смонтирована PS Vita, и удалите файл `config.txt`
1. Переименуйте файл `config_psvtv.txt` в `config.txt`
    * Для переименования нажмите на файле {% include inc/btn.md btn="TRIANGLE" %} и выберите **Rename**
{% endcapture %}
<div class="hideble 370 hide">{{ notice-1 | markdownify }}</div>

### Часть V - Установка SD2Vita (опционально)

**SD2Vita** - это адаптер для microSD карты, который вставляется в слот для картриджа с игрой, а **psvd** это адаптер для microSD карты, который заменяет собой 3g модем на моделях PS Vita с поддержкой 3g. При помощи SD2Vita, microSD карта (или USB диск, если у вас PS Vita TV) могут быть смонтированы как `ux0:` вместо карты памяти Sony. Это весьма полезно, поскольку оригинальные карты Sony, сколь-либо значимой ёмкости, стоят невероятно дорого. 
{: .notice--info}

Если вы не планируете использовать SD2Vita, пропустите этот шаг
{: .notice--warning}

1. Запустите **VitaShell**
1. Удалите папку `tai` из раздел `ux0:`, если таковая тут есть
1. Перейдите в `ux0:/plugins`
1. Переместите `storage_config.txt` и `storagemgr.skprx` из папки `ux0:/plugins` в папку `ur0:tai` с заменой (если таковая потребуется)
    * **ОБРАТИТЕ ВНИМАНИЕ**, мы переносим файлы из раздела u**x**0 в раздел u**r**0!
    * Для перемещения, нажмите {% include inc/btn.md btn="TRIANGLE" %} на выбранной папке и выберите `Move`
    * Для того, чтобы вставить скопированное в другую папку, зайдите в папку, в которую хотите скопировать данные, нажмите {% include inc/btn.md btn="TRIANGLE" %} и выберите `Paste`

### Часть VI - Очистка

1. Запустите приложение **Управление данными**
1. Выберите "**Управление данными на карте памяти**"
1. Выберите "**PS Vita**"
1. Удалите следующие приложения, если они есть (в зависимости от метода установки некоторые либо все эти приложения могут отсутствовать):
  + "**3G Disabler**"
  + "**Application Storage Manager**"
  + "**ensō**"
  + "**iTLS-Enso**"
  + "**modoru 戻る**"
  + "**molecularShell**"
1. Закройте приложение **Управление данными**
1. Запустите **VitaShell**
1. Удалите папки `plugins` и `VPK` из `ux0:/`
1. Перезапустите PS Vita

Если всё сделано правильно, вы сможете запускать и обновлять игры от PS Vita, PSP и PSX бесплатно, устанавливать для PSV-игр патчи и модификации. Благодаря плагинам у вас появится возможность [разгонять приставку](games#разгон-на-ps-vita){:target="blank_"} по нажатию {% include inc/btn.md btn="SELECT" %}+{% include inc/btn.md btn="UP" %}, процентное значение заряда возле индикатора батареи, дополнительные пункты в быстром меню (вызывается по долгому нажатию кнопки {% include inc/btn.md btn="PS" %}), возможность прослушивать свою музыку даже в играх и управлять ей через быстрое меню, делать скриншоты в PNG по нажатию {% include inc/btn.md btn="PS" %}+{% include inc/btn.md btn="START" %}.
{: .notice--info}

___


Для получения информации о замене карты памяти Sony на microSD карту (или USB диск, если у вас PS Vita TV), перейдите к странице [sd2vita](sd2vita){:target="_blank"}.
{: .notice--success}

[Полезные инструкции](addons){:target="_blank"}
{: .notice--success}

Для получения информации об установке игр, перейдите к странице [Установка игр](games){:target="_blank"}.
{: .notice--success}

Для получения информации об установке CFW во встроенный эмулятор PSP, перейдите к странице [Adrenaline](adrenaline).
{: .notice--success}

Подробнее про установку плагинов можете почитать [здесь](plugins){:target="_blank"}.
{: .notice--success}

Вы можете найти новые хоумбрю приложения на [VitaDB](https://vitadb.rinnegatamante.it/).
{: .notice--info}

*НЕ* рекомендуется модифицировать кастомную прошивку путём установки хоумбрю приложений, предназначенных для опытных пользователей (таких как "Enso EX"). Такие действия без полного понимания системы могут привести к БРИКУ!
{: .notice--danger}