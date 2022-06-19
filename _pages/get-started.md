---
title: "Начало"
---

{% include toc title="Содержание" %}

### Обязательно к прочтению

Разные версии системного ПО консоли требуют различных действий для установки кастомной прошивки. Эта страница поможет вам понять, откуда именно следует начать.

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов, а так же скрытые и системные файлы. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](https://customfw.xyz/file-extensions-windows)!

Выберите подходящую для вашей версии страницу из таблицы ниже. Обратите внимание, что столбцы "С" и "По" обозначают границы диапазона. 

Столбцы "С" и "По" обозначают границы диапазона. Это означает, к примеру, что диапазон "с 1.03 по 3.57" включает в себя как 1.03, так и 3.57, а так же все версии системного ПО, что были между ними.

Версия прошивки вашей консоли отображается в меню **Информация о системе** в приложении **Настройки**.

![]({{ "/images/screenshots/system-version_365.png" | absolute_url }})
{: .text-center}
{: .notice--info}

### Блокировка обновлений 

Для предотвращения нежелательных обновлений мы изменим настройки DNS вашей консоли, чтобы использовать кастомный сервер обновлений, который указывает на 3.60 в качестве последней доступной версии. Это действие заблокирует установку любых версий прошивки выше 3.60, когда консоль попытается выполнить обновление.

Обратите внимание, что адреса этих DNS серверов должны быть настроены для каждой сети, к которой вы подключаете свою консоль, чтобы обновления блокировались!
{: .notice--warning}

1. Запустите приложение Настройки
1. Перейдите в "**Сеть**" -> "**Настройки Wi-Fi**"
  + Подключитесь к сети Wi-Fi, если вы еще этого не сделали
1. Выберите ваше текущее подключение
  + Оно обозначено зелёной точкой рядом с сетью
1. Выберите "**Дополнительные настройки**"
1. Измените "**Настройки DNS" на "Вручную**"
1. Измените "**Основной DNS**" и "**Дополнительный DNS**" на `212.47.229.76`
1. Убедитесь, что настройка "**Прокси-сервер**" выставлена в значение "**Не использовать**"
1. Нажмите "**ОК**"
1. Вернитесь в главное меню настроек
1. Перейдите в **Система** -> **Настройка автозапуска**
1. Снимите флажок "**Загружать файл обновления для системного программного обеспечения**"
1. Нажмите {% include inc/btn.md btn="PS" %} для выхода на главный экран


### Таблица версий

<table>
  <colgroup>
    <col span="1" style="width: 10%;">
    <col span="1" style="width: 10%;">
    <col span="1" style="width: 80%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;">С</th>
      <th style="text-align: center; font-weight: bold;">По</th>
      <th style="text-align: center; font-weight: bold;"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">1.03</td>
      <td style="text-align: center; font-weight: bold;">3.57</td>
      <td style="text-align: center; font-weight: bold;"><a href="updating-to-360">Обновление прошивки до 3.60</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" colspan="2">3.60</td>
      <td style="text-align: center; font-weight: bold;"><a href="installing-henkaku">Установка HENkaku</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">3.61</td>
      <td style="text-align: center; font-weight: bold;">3.63</td>
      <td style="text-align: center; font-weight: bold;"><a href="updating-firmware-ps-vita-365">Обновление прошивки (PS Vita)</a> или <a href="updating-firmware-ps-tv-365">Обновление прошивки (PS TV)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">3.65</td>
      <td style="text-align: center; font-weight: bold;">{% include vars/sys_version.txt %}</td>
      <td style="text-align: center; font-weight: bold;"><a href="installing-h-encore">Установка h-encore</a></td>
    </tr>
  </tbody>
</table>
