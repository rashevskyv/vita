---
permalink: /ark-epsp-psvimgtools.html
title: Установка ARK ePSP CFW
author_profile: true
---
{% include toc title="Разделы" %}

ARK - это кастомная прошивка для эмулятора PSP (ePSP), встроенного в Vita. Эксплойт, необходимый для установки ARK, работает только на Vita с прошивкой 3.61-3.63, поскольку в прошивке 3.65 уязвимость в ядре ePSP была закрыта {: .notice--info}

На этой странице мы установим ARK. {: .notice--info}

#### Что понадобится

* Игра для PSP, загруженная на Vita.
* Свежая версия [QCMA](https://codestation.github.io/qcma/) для вашей операционной системы на ПК.
* Свежая версия [psvimgtools](https://github.com/yifanlu/psvimgtools/releases/latest) для вашей операционной системы на ПК.
* Архив с [ARK PBOOT](http://www.mediafire.com/file/rfqhsjuvs6ax6co/FW360_ARK_pboot_bubble.zip).

#### Инструкции

##### Часть I - Установка ARK

1. Скачайте и установите QCMA и установите соединение программы и PS Vita.
2. Раздобудьте PSN AID. По умолчанию в Windows он расположен по пути `C:/Users/Username/Documents/PS Vita/PGAME/xxxxxxxxxxxxxxxx/`. Набор символов вида `xxxxxxxxxxxxxxxx` и есть искомый PSN AID.
3. На компьютере перейдите по адресу <http://cma.henkaku.xyz/> и скопируйте туда ваш PSN AID.
4. Скопируйте полученный ключ в надежное место (например, в файл "AID KEY")
5. Распакуйте архив psvimgtools в удобное место на вашем ПК
6. Создайте резервную копию PSP-игры с помощью QCMA.
7. Найдите резервную копию игры по пути /PSvita/PGAME/xxxxxxxxxxxxxxxx/[GAMEID]/game/game.psvimg
8. Скопируйте `game.psvimg` в папку psvimgtools.
9. Откройте командную строку Windows (нажмите Win+R и напечатайте `cmd`, затем нажмите Enter) или Terminal (macOS/Linux).
10. Перейдите в папку psvimgtools, используя команду `cd`
11. Введите команду, соответствующую вашей операционной системе на ПК: + Windows: `psvimg-extract -K YOUR-KEY game.psvimg` + macOS/Linux: `./psvimg-extract -K YOUR-KEY game.psvimg game` Где `YOUR-KEY` - это ключ, который вы получили на сайте http://cma.henkaku.xyz/.
12. По завершению вы получите папку с названием `ux0_pspemu_temp_game_PSP_GAME_ID`, где `PSP_GAME_ID` - GAME ID вашей игры для PSP.
13. Распакуйте архив ARK PBOOT и найдите в нем файл `PBOOT.PBP`
14. Замените PBOOT.PBP, находящийся в папке с распакованной игрой (`ux0_pspemu_temp_game_PSP_GAME_ID`) файлом PBOOT.PBP из архива с ARK PBOOT
15. Введите команду, соответствующую вашей операционной системе на ПК: + Windows: `psvimg-create -n game -K YOUR-KEY game game` + macOS/Linux: `./psvimg-create -n game -K YOUR-KEY game game` Где `YOUR-KEY` - это ключ, который вы получили на сайте http://cma.henkaku.xyz/. Вы получите папку `ux0_pspemu_temp_game_PSP_GAME_ID` с файлами `game.psvimg` и `game.psvmd`.
16. Скопируйте эти файлы в папку с резервной копией игры для PSP в папку с резервной копией игры от QCMA.
17. Восстановите резервную копию вашей PSP-игры через QCMA, после того как скопируете файлы.
18. Скопируйте папку "ARK_01234" из архива с ARK PBOOT в папку /PSvita/PSAVEGAME/xxxxxxxxxxxxxxxx/. (где xxxxxxxxxxxxxxxx - ваш PSN AID).
19. Восстановите данные сохранений ARK-2 (PSP SAVEDATA) на PS Vita через QCMA.

____

Следующий шаг: [Завершение установки ARK](finalizing-setup-ark) {: .notice--primary}