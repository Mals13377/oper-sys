---
## Front matter
title: "Лабораторная работа №6"
subtitle: "Текстовой редактор vi"
author: "Мальсагов Акрамат Абу-Бакарович"

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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Выполнение лабораторной работы

1. Создал новый каталог **work/os/lab06**. С помощью vi создал файл hello.sh.(рис. [-@fig:001])

![Вызов vi](image/1.png){ #fig:001 width=70% }

2. Перешел в режим вставки и ввел текст. (рис. [-@fig:002])

![Ввод текста](image/2.png){ #fig:002 width=70% }

3. Сохранил изменениея.(рис. [-@fig:003])

![Сохранение](image/3.png){ #fig:003 width=70% }

4. Сделал файл исполняемым.(рис. [-@fig:004])

![Изменение прав доступа](image/4.png){ #fig:004 width=70% }

5. Заменил **HELL** на **HELLO**.(рис. [-@fig:005])

![Замена слова HELL](image/5.png){ #fig:005 width=70% }

6. Заменил **LOCAL** на **local**. (рис. [-@fig:006])

![Замена слова LOCAL](image/6.png){ #fig:006 width=70% }

7. Вставил в конец файла текст.(рис. [-@fig:007])

![Вставка строки в конец файла](image/7.png){ #fig:007 width=70% }

8. Удалил последнюю строку.(рис. [-@fig:008])

![Удаление последней строки](image/8.png){ #fig:008 width=70% }

9. Отменил последнее действие.(рис. [-@fig:009])

![Отмена последнего действия](image/9.png){ #fig:009 width=70% }

10. Сохранил изменениея.(рис. [-@fig:010])

![Сохранение](image/10.png){ #fig:010 width=70% }

# Выводы

Мы получили базовые навыки использования vi.

# Контрольные вопросы


1. Редактор vi имеет три режима работы:
– командный режим — предназначен для ввода команд редактирования и навигации по
редактируемому файлу;
– режим вставки — предназначен для ввода содержания редактируемого файла;
– режим последней (или командной) строки — используется для записи изменений в файл
и выхода из редактора.

2. Набрать символ q (или q!), если требуется выйти из редактора без сохранения

3. Команды позиционирования
- 0 (ноль) — переход в начало строки;
- $ — переход в конец строки;
- G — переход в конец файла;
- nG — переход на строку с номером 𝑛.


4. При использовании прописных W и B под разделителями понимаются только пробел, табуляция и возврат
каретки. При использовании строчных w и b под разделителями понимаются также любые знаки пунктуации.

5. Для того, чтобы переместить курсор в начало файла, можно использовать команду 1G. Для перехода в конец файла необходимо нажать G.

6. Команды редактирования: вставка текста, вставка строки, удаление текста, отмена и повтор произведённых изменений, копирование текста в буфер, вставка текста из буфера, замена текста, поиск текста.

7. Перейду в режим вставки и введу необходимое количество *$*.

8. Отменить последнее действие с помощью команды *u*.

9. Команды редактирования в режиме командной строки: копирование и перемещение текста, запись в файл и выход из редактора

10. Необходимо перейти в конец строки с помощью *$*.

11. Опции
Опции редактора vi позволяют настроить рабочую среду. Для задания опций используется команда set (в режиме последней строки):
- : set all — вывести полный список опций;
- : set nu — вывести номера строк;
- : set list — вывести невидимые символы;
- : set ic — не учитывать при поиске, является ли символ прописным или строчным.
Если вы хотите отказаться от использования опции, то в команде set перед именем
опции надо поставить no.

12. Если в нижнем углу выводиться *Insert* - мы находимся в режиме вставки.
  Если курсор находится в конце файла и можно увидеть там двоеточие - режим последней (или командной) строки
  В ином случаи - мы находимся в командном режиме

13.   Командный режим.
        - режим вставки.
        - режим последней строки.