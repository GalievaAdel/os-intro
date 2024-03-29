---
## Front matter
title: "Лабораторная работа №10"
subtitle: "Программирование в командном процессоре ОС UNIX. Командные файлы"
author: "Галиева Аделина Руслановна"

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


Изучить основы программирования в оболочке ОС UNIX/Linux. Научиться писать небольшие командные файлы.


# Выполнение лабораторной работы


1. Пишем скрипт, который при запуске будет делать резервную копию самого себя (то есть файла, в котором содержится его исходный код) в другую директорию backup в нашем домашнем каталоге. (рис. @fig:001) (рис. @fig:002) 


![Прописываем команды](image/1.png){#fig:001 width=70% }

![Пишем скрипт](image/2.png){#fig:002 width=70% }


2. Пишем пример командного файла, обрабатывающего любое произвольное число аргументов командной строки, в том числе превышающее десять. (рис. @fig:003) (рис. @fig:004) 


![Прописываем команды](image/3.png){#fig:003 width=70% }

![Пишем пример](image/4.png){#fig:004 width=70% }


3. Пишем командный файл — аналог команды ls (без использования самой этой команды и команды dir). (рис. @fig:005) (рис. @fig:006) 


![Прописываем команды](image/5.png){#fig:005 width=70% }

![Пишем командный файл](image/6.png){#fig:006 width=70% }


4. Пишем командный файл, который получает в качестве аргумента командной строки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки. (рис. @fig:007) (рис. @fig:008) 


![Прописываем команды](image/7.png){#fig:007 width=70% }

![Пишем командный файл](image/8.png){#fig:008 width=70% }


# Контрольная работа


1. Объясните понятие командной оболочки. Приведите примеры командных оболочек. Чем они отличаются?
a)	sh — стандартная командная оболочка UNIX/Linux, содержащая базовый, 	полный набор функций
b)	csh — использующая С-подобный синтаксис команд с возможностью 	сохранения истории выполнения команд
c)	ksh — напоминает оболочку С, но операторы управления программой 	совместимы с операторами оболочки Борна
d)	bash — сокращение от Bourne Again Shell (опять оболочка Борна), в основе 	своей совмещает свойства оболочек С и Корна

2. Что такое POSIX?
POSIX (Portable Operating System Interface for Computer Environments) — набор  стандартов описания интерфейсов взаимодействия операционной системы и прикладных программ.

3. Как определяются переменные и массивы в языке программирования bash?
Переменные вызываются $var, где var=чему-то, указанному пользователем, неважно что бы то не было, название файла, каталога или еще чего.
Для массивов используется команда set -A

4. Каково назначение операторов let и read?
let — вычисляет далее заданное математическое значение
read — позволяет читать значения переменных со стандартного ввода

5. Какие арифметические операции можно применять в языке программирования bash?
Прибавление, умножение, вычисление, деление), сравнение значений, экспонирование и др.

6. Что означает операция (( ))?
Это обозначение используется для облегчения программирования для условий bash 

7. Какие стандартные имена переменных Вам известны?
Нам известны HOME, PATH, BASH, ENV, PWD, UID, OLDPWD, PPID, GROUPS, OSTYPE, PS1 - PS4, LANG, HOSTFILE, MAIL, TERM, LOGNAME, USERNAME, IFS и др.

8. Что такое метасимволы?
Метасимволы это специальные знаки, которые могут использоваться для сокращения пути, 	поиска объекта по расширению, перед переменными, например «$» или «*» .

9. Как экранировать метасимволы?
Добавить перед метасимволом метасимвол «\»

10. Как создавать и запускать командные файлы?
При помощи команды chmod. Надо дать права на запуск chmod +x название файла, затем запустить bash  ./название файла
Например у нас файл lab
Пишем: 
chmod +x lab
./lab

11. Как определяются функции в языке программирования bash?
Объединяя несколько команд с помощью function

12. Каким образом можно выяснить, является файл каталогом или обычным файлом?
Можно задать команду на проверку диретория ли это test -d директория

13. Каково назначение команд set, typeset и unset?
Set — используется для создания массивов
Unset — используется для изъятия переменной
Typeset — используется для присваивания каких-либо функций

14. Как передаются параметры в командные файлы?
Добавлением аршументов после команды запуска bash скрипта

15. Назовите специальные переменные языка bash и их назначение.
```
–	$* — отображается вся командная строка или параметры оболочки;
–	$? — код завершения последней выполненной команды;
–	$$ — уникальный идентификатор процесса, в рамках которого выполняется командный процессор;
–	$! — номер процесса, в рамках которого выполняется последняя вызванная на выполнение в командном режиме команда;
–	$- — значение флагов командного процессора;
–	${#*} — возвращает целое число — количество слов, которые были результатом
$*;
–	${#name} — возвращает целое значение длины строки в переменной name;
–	${name[n]} — обращение к n-му элементу массива;
–	${name[*]} — перечисляет все элементы массива, разделённые пробелом;
–	${name[@]} — то же самое, но позволяет учитывать символы пробелы в самих переменных;
–	${name:-value}—еслизначениепеременнойnameнеопределено,тоонобудет заменено на указанное value;
–	${name:value} — проверяется факт существования переменной;
–	${name=value} — если name не определено, то ему присваивается значение value;
–	${name?value} — останавливает выполнение, если имя переменной не определено, и выводит value как сообщение об ошибке;
–	${name+value} — это выражение работает противоположно ${name-value}. Если переменная определена, то подставляется value;
–	${name#pattern} — представляет значение переменной name с удалённым самым коротким левым образцом (pattern);
–	${#name[*]}и${#name[@]}—этивыражениявозвращаютколичествоэлементов в массиве name.
```


# Выводы


Я изучила основы программирования в оболочке ОС UNIX/Linux. Научилась писать небольшие командные файлы.


# Список литературы{.unnumbered}

::: {#refs}
:::
