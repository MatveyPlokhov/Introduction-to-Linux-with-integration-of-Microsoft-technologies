# Введение в Linux с интеграцией технологий Microsoft
**Для начала работы у вас должно быть устройство с [Windows 10](https://www.microsoft.com/ru-ru/software-download/windows10)**
---
## Оглавление:
1) [Плюсы и минусы Linux](#Плюсы-и-минусы-Linux)
2) [Что такое терминал?](#Что-такое-терминал)
3) [Эмуляторы терминала:](#Эмуляторы-терминала)
4) [Основные команды Linux](#Основные-команды-Linux)
5) [Snap пакеты:](#Snap-пакеты)
6) [Chocolatey:](#Chocolatey)
7) [Установка WSL](#Установка-WSL)
8) [Установка Neofetch](#Установка-Neofetch)
9) [Удалённая разработка в VS Code](#Удалённая-разработка-в-VS-Code)
10) [GitHub](#GitHub)
---
## Плюсы и минусы Linux
* Востребованность
  * Android  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/01.png)
  * Дистрибутивы  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/02.png)
  * Суперкомпьютеры  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/03.jpg)
  * Фондовая биржа (New York)  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/04.jpg)
  * CERN  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/05.jpg)
  * Сервера  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/06.jpg)
* Стоимость  
  Linux полностью бесплатен за исключением некоторых дистрибутивов (Red Hat, SUSE).
* Большой выбор  
  Существует огромный выбор дистрибутивов.
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/07.png)
* Приложения  
  Отсутствие многих популярных приложений, но у них есть замены (некоторые из них не очень удобные):
  * Microsoft Office - Libre Office
  * 3D Studio Max - Blender
  * Adobe Photoshop - GIMP
  * Adobe Premiere Pro - Open Movie Editor
  * Adobe Audition - Audacity
  * Adobe Lightroom - Darktable
  * CPU Z - I-Nex
  * FL Studio - Linux MultiMedia Studio
  * uTorrent - Transmission
  * AIMP - Audacious
* Гибкость  
  Linux можно сделать похожим на что угодно. Вы можете изменить интерфейс до неузнаваемости добавить новые команды и многое другое.
* [Безопасность](https://habr.com/ru/company/1cloud/blog/309696/)  
  На Linux дистрибутивы делается немного вирусов, и я даже не могу вспомнить хотя бы один. Из-за своей гибкости вы вправе отключить любую службу или добавить.
* Скорость 
  Linux обладает куда меньшими требованиями к железу и способна летать на любом устройстве.
* Баги 
  Всё зависит от дистрибутива. Если дистрибутив поддерживается, то баги очень быстро фиксятся, но они все равно могут присутствовать.
* Освоение 
  Linux уже давно имеет хороший интерфейс и лёгок в освоении.

[:arrow_up:Оглавление](#Оглавление)
---
## Что такое терминал?  
* Терминал (виртуальная консоль) — это часть системы, предназначенная для того, чтобы выполнять нужные для вас команды, и делать это эффективнее по скорости. Но это вовсе не обязательно, многим вполне достаточно графического интерфейса. Сейчас использование терминала отошло на второй план, но он остается основным средством для доступа к удаленным серверам и инструментом для профессионалов. 

[:arrow_up:Оглавление](#Оглавление)
---
## Эмуляторы терминала:  
* Эмуляторы терминала - это графическое приложение для терминала похожее на CMD, но отличающаяся по функционалу.
  * Thermex - терминал на Android.
  * Upterm - можно использовать как IDE с автодополнением.
  * Terminator -  можно создать сетку из множества терминалов в одном окне.
  * Alacritty - самый быстрый терминал.
  * Hyper - красивый.
  * TERMITE - ничем не примечательный эмулятор терминала.
```
ctrl+alt+t - эмулятор терминала  
ctrl+alt+(f1 - f6) - терминал
```

[:arrow_up:Оглавление](#Оглавление)
---
## Основные команды Linux:  
* примеры показаны на Linux Mint на других дистрибутивах могут быть различия:
  * pwd - показывает в каком каталоге вы находитесь
  * ls -a - показывает ВСЕ файлы каталога
  * cd - переместиться в главный каталог
  * cd .. - переместиться на уровень выше
  * cd folder\ name - переместиться в определенную папку
  * mkdir folder\ name- создание папки
  * rm -r - удаление каталога
  * rm - удаление каталога и файлов внутри
  * touch name.txt - создание любого файла
  * nano name.txt - открытие файла и его редактирование
  * cp имя1 имя2 - копирование файла
  * mv путь1 путь2 - перемещение файла
  * sudo команда - выполнение команды с правами администратора
  * sudo updatedb - обновление базы данных
  * locate -i - поиск файла игнорируя регистр
  * sudo apt-get - используется для установки пакетов
  * sudo apt-get update - поиск обновлений пакетов из репозиториев
  * sudo apt-get upgrade - обновление пакетов, которые нашла система
  * sudo apt-get install sl
  * sl - запуск паровоза который мы установили 
  * sudo apt-get remove sl - удаление паровоза
  * sudo apt-get autoremove - удаление зависимостей, которые уже не используются
  * xkill - завершение процесса

[:arrow_up:Оглавление](#Оглавление)
---
## Snap пакеты:
* snap пакеты позволяют скачать не только саму программу, но и все зависимости, которые требуются для запуска. 
  * sudo apt install snapd - установка пакета snapd
  * snap find - показывает список доступных пакетов
  * sudo snap install skype - установка пакета gimp
  * snap list - список установленных пакетов
  * snap refresh имя_пакета - обновление всех пакетов (конкретный)
  * snap info skype - информация о пакете 
  * snap disable skype - отключить пакет
  * snap enable skype - включить пакет
  * snap run skype - запуск пакета
  * Кликаем ПКМ по рабочему столу и выбираем ```Создать кнопку запуска здесь...```  
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/08.png)  
  Теперь вы можете назначить иконку, команду и название ярлыка для запуска
  ![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/09.png)
  * snap remove skype - удаление пакета

[:arrow_up:Оглавление](#Оглавление)
---
## Chocolatey:
* Это приложение, которое добавляет apt-get для Windows.
  * choco list - список программ
  * choco install имя_пакета - установка приложения
  * choco update имя_пакета - обновление приложения
  * choco uninstall имя_пакета - удаление пакета

[:arrow_up:Оглавление](#Оглавление)
---
## Установка WSL
* Открываем PowerShell от имени администратора.  
![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/10.png)
* Вписываем команду:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/11.png)
* Перезагружаем устройство если написано:
```
RestartNeeded : True
```
* Открываем Microsoft Store и скачиваем Ubuntu 18.04 LTS
![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/12.png)
* Запускаем скаченный Ubuntu 18.04 LTS и ждём
```
Installing, this may take a few minutes...
```
* Создаём логин и пароль для пользователя  

![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/13.png)  
* Обновляем и устанавливаем все пакеты:
```
sudo apt update && sudo apt upgrade
```
![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/14.png)
* Всё готово для работы

[:arrow_up:Оглавление](#Оглавление)
---
## Установка Neofetch


[:arrow_up:Оглавление](#Оглавление)
---
## Удалённая разработка в VS Code


[:arrow_up:Оглавление](#Оглавление)
---
## GitHub


[:arrow_up:Оглавление](#Оглавление)
---
## Ссылки:
* [Плюсы и минусы Linux (презентация)](![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/Linux+-.pptx)
* [Терминал (презентация)](![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/Terminal.pptx)
* [Краткий конспект к презентациям](![](https://github.com/MatveyPlokhov/Introduction-to-Linux-with-integration-of-Microsoft-technologies/blob/master/Files/Terminal.docx)

[:arrow_up:Оглавление](#Оглавление)
---
