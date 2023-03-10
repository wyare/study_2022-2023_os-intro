---
## Front matter
title: "Лабораторная работа № 4"
subtitle: "Основы интерфейса взаимодействия пользователя с системой Unix на уровне командной строки"
author: "Овчинников Данил Евгеньевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков взаимодействия пользователя с системой по-
средством командной строки.

# Выполнение лабораторной работы

Определим полное имя вашего домашнего каталога. Далее относительно этого ката-
лога будут выполним последующие упражнения.(рис. @fig:001).

![Опеределение имени домашнего каталога](image/1.png){#fig:001 width=70%}


Перейдем в каталог /tmp и выведем на экран его содержимое при помощи различных опций команды ls.(рис. @fig:002 @fig:003 @fig:004).

![Переход в каталог /tmp, проверка его содержимого](image/2.png){#fig:002 width=70%}

![Выбор другой опции для проверки содержимого каталога](image/3.png){#fig:003 width=70%}


![Выбор другой опции для проверки содержимого каталога](image/4.png){#fig:004 width=70%}


Проверим есть ли в каталоге /var/spool подкаталог с именем cron, в нашем случае он есть.(рис. @fig:005).

![Проверка каталога /var/spool](image/5.png){#fig:005 width=70%}

Перейдем в Ваш домашний каталог и выведите на экран его содержимое. Опередилм, что я deovchinnikov являюсь владельцев файлов и подкаталогов.(рис. @fig:006).

![Домашний каталог, владелец файлов](image/6.png){#fig:006 width=70%}

В домашнем каталоге создадим новый каталог с именем newdir.(рис. @fig:007).

![Создание каталога newdir](image/7.png){#fig:007 width=70%}

В каталоге ~/newdir создадим новый каталог с именем morefun.(рис. @fig:008).

![Создание подкаталога morefun](image/8.png){#fig:008 width=70%}

В домашнем каталоге создадим одной командой три новых каталога с именами
letters, memos, misk. Затем удалим эти каталоги при помощи одной команды.(рис. @fig:009 @fig:011).

![Создание каталогов letters, memos, misk](image/9.png){#fig:009 width=70%}

![Удаление каталогов letters, memos, misk](image/11.png){#fig:011 width=70%}

Удалим ранее созданный каталог ~/newdir командой rm и проверим его.(рис. @fig:010).

![Удаление каталога newdir](image/10.png){#fig:010 width=70%}

С помощью команды man определим, какую опцию команды ls нужно использо-
вать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него.(рис. @fig:015).

![Просмотр опций ls](image/15.png){#fig:015 width=70%}

С помощью команды man определим набор опций команды ls, позволяющий отсорти-
ровать по времени последнего изменения выводимый список содержимого каталога
с развёрнутым описанием файлов. При помощи опции -c -lt.(рис. @fig:017).

![Просмотр опций ls](image/17.png){#fig:017 width=70%}

Используя команду man для просмотра описания следующих команд: cd, pwd, mkdir,
rmdir, r, узнаем и поясним их основные функции.(рис. @fig:018).

![Просмотр описания команд](image/18.png){#fig:018 width=70%}

Используя информацию, полученную при помощи команды history, выполним мо-
дификацию и исполнение нескольких команд из буфера команд.(рис. @fig:019 @fig:020).

![Модификация и исполнение команд при помощи history](image/19.png){#fig:019 width=70%}

![Модификация и исполнение команд при помощи history](image/20.png){#fig:020 width=70%}

# Выводы

В ходе лабораторной работы приобрел практически навыки взаимодействия с системой посредством командной строки.

# Контрольные вопросы

1. Что такое командная строка? Командная строка – это специальная программа, которая позволяет управлять компьютером путем ввода текстовых команд с клавиатуры.
2. При помощи какой команды можно определить абсолютный путь текущего каталога? При помощи команды pwd.
3. При помощи какой команды и каких опций можно определить только тип файлов и их имена в текущем каталоге? При помощи команды ls -F.
4. Каким образом отобразить информацию о скрытых файлах? При помощи команды ls -a.
5. При помощи каких команд можно удалить файл и каталог? Можно ли это сделать одной и той же командой? Файл можно удалить при помощи команды rm, а каталог при помощи команды rmdir. Одной командой это не получится сделать.
6. Каким образом можно вывести информацию о последних выполненных пользователем командах? При помощи команды history.
7. Как воспользоваться историей команд для их модифицированного выполнения? При помощи команды !:s//.
8. Приведите примеры запуска нескольких команд в одной строке. Например, cd; ls.
9. Дайте определение и приведите примеры символов экранирования. Экранирование символов — замена в тексте управляющих символов на соответствующие текстовые подстановки. Один из видов управляющих последовательностей.
10. Охарактеризуйте вывод информации на экран после выполнения команды ls с опцией l. Будут отображаться владелец, группа, дата создания.
11. Что такое относительный путь к файлу? Относительный путь — это путь к файлу относительно текущего каталога.
12. Как получить информацию об интересующей вас команде? С помощью команды man.
13. Какая клавиша или комбинация клавиш служит для автоматического дополнения вводимых команд? С помощью клавиши Tab.