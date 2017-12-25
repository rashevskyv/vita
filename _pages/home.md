---
permalink: /
title: "PS Vita Guide"
author_profile: true
header:
  overlay_color: "#5e616c"
  overlay_image: images/home-page-feature.jpg
  overlay_filter: 0.5
  caption:
excerpt: 'Полное руководство по прошивке PS Vita / Vita TV, от стоковой прошивки до HENkaku Ensō (3.60), ePSP CFW (3.61-3.63) или ePSP Homebrew (3.65+).<br />**Последнее изменение:** 25 декабря 2017'
---

{% include toc title="Разделы" %}

Вдумчиво прочитайте каждую вступительную страницу инструкции (включая эту!) перед тем, как начать. Ознакомьтесь с [FAQ](faq) и пройдитесь по руководству, мысленно выполняя шаги, соответствующие вашей конфигурации. 
{: .notice--warning}

Это руководство - форк гайда от [T3CHNOLOG1C](http://psvita.guide), переведенный на русский язык для группы [VK:portablegaming](https://vk.com/portablegaming) и дополненный информацией из базы знаний и опыта администрации этой группы. 
{: .notice--success}

Это руководство применимо *только* для консолей, продающихся в рознице. Приставки для разработчиков невозможно прошить по этой инструкции!  
{: .notice--danger}

## Что такое Homebrew?

Под словом [**Homebrew (хомбрю)**](https://ru.wikipedia.org/wiki/homebrew_(%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%BD%D1%8B%D0%B5_%D0%B8%D0%B3%D1%80%D1%8B)) обычно подразумевают программное обеспечение не авторизованное Sony. В качестве примера можно привести разные самописные игры, программы для бэкапа и редактирования сохранений и эмуляторы консолей предыдущих поколений.

В большинстве случаев запуск Homebrew на 100% бесплатен и использует [интернет браузер PS Vita](running-henkaku). Если системное ПО вашей приставки 3.61-3.63, сможете использовать ePSP CFW или обычное Homebrew. Если у вас 3.65, то для доступа к Homebrew вам понадобится скачанная через PSN игра для PSP.

## Что такое Homebrew Enabler?

**Homebrew Enabler** ("HEN") enables you to use more advanced hacks that userland homebrew can't easily do. For instance, signature patches let you install unsigned apps that appear right on your LiveArea screen.

HEN can be easily set up on any console that is on 3.60 or lower.

## What does this guide install?

This guide has the end goal of taking a completely unmodified Vita from stock firmware to a boot time homebrew enabler called HENkaku Ensō (3.60). If your console is on 3.61 or higher, the best you can do is get ePSP CFW or Homebrew.

HENkaku Ensō is currently the only feasible method for running native homebrew on our PS Vita / TV systems. It will install an application that can be used to install packages and manage files called "molecularShell" which we will use to install "VitaShell", another package / file manager with more features. We will also install a boot time exploit to run HENkaku called HENkaku Ensō.

For information on how HENkaku works, please see [this blog post](https://yifan.lu/2016/10/20/henkaku-koth-solved/) by [Yifan Lu](https://twitter.com/yifanlu).

## What can I do with a Homebrew Enabler?

+ Customize your LiveArea Screen with user-created [themes](http://vstema.com/).
+ Use "ROM hacks" for games that you own
+ [Backup, edit, and restore](https://github.com/d3m3vilurr/vita-savemgr) saves for many games.
+ Play games for older systems with various emulators, using RetroArch or other standalone emulators.
+ Dump your game cards to a format you can install, and play them without needing the card.
+ Certain games only: stream live gameplay to your PC wirelessly with Rincheat Streamer.
+ Play backups of your PSP games on your Vita with Adrenaline ePSP CFW

## What do I need to know before starting?

+ **Before beginning the guide, you must know the risks of Vita hacking: EVERY time you modify your system, there is always the potential for an UNRECOVERABLE brick. They're very very rare and usually only happen after modifying system files, but still a possibility, however that possibility is slim to none, considering that this guide does not have you modify any critical system files without using specially designed tools to do these modifications.**
+ This guide will work on PS Vita, PS Vita Slim, and PSTV in all regions on firmware 3.60 or below.
+ If everything goes according to plan, you will lose no data and end up with everything that you started with (games, PSN Account, saves, etc will be preserved).
+ **Keep your device plugged in and charged throughout the entire process to avoid data loss or damage from an unexpected power-off!**
+ The PS Vita Slim is essentially identical to the Original PS Vita in terms of software, and that any steps which say "PS Vita" also apply to the slim model.

___

<center><a href="get-started" style="margin:20px auto; text-align:center; display:block; width:200px;" class="btn btn--short">Начнем!!</a></center>
{: .notice--success}