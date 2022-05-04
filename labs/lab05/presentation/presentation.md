---
## Front matter
lang: ru-RU
title: lab05
author: |
	Kate P. Mitichkina \inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 28 April, 2022 Moscow, Russia

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---
# Лабораторная работа № 5. Анализ файловой системы Linux. Команды для работы с файлами и каталогами

## Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

## Задача

1. Выполните все примеры, приведённые в первой части описания лабораторной работы.
2. Выполните следующие действия, зафиксировав в отчёте по лабораторной работе используемые при этом команды и результаты их выполнения:
	1. Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его equipment. Если файла io.h нет, то используйте любой другой файл в каталоге /usr/include/sys/ вместо него.
	2. В домашнем каталоге создайте директорию ~/ski.plases.
	3. Переместите файл equipment в каталог ~/ski.plases.
	4. Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.
	5. Создайте в  домашнем  каталоге  файл  abc1 и  скопируйте  его  в  каталог ~/ski.plases, назовите его equiplist2.
	6. Создайте каталог с именем equipment в каталоге ~/ski.plases.
	7. Переместите  файлы   ~/ski.plases/equiplist и   equiplist2 в   каталог ~/ski.plases/equipment.
	8. Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите его plans.
3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав нет:
	1. drwxr--r--	...	australia
	2. drwx--x--x	...	play
	3. -r-xr--r--	...	my_os
	4. -rw-rw-r--	...	feathers
	При необходимости создайте нужные файлы.
4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной работе используемые при этом команды:
	1. Просмотрите содержимое файла /etc/password.
	2. Скопируйте файл ~/feathers в файл ~/file.old.
	3. Переместите файл ~/file.old в каталог ~/play.
	4. Скопируйте каталог ~/play в каталог ~/fun.
	5. Переместите каталог ~/fun в каталог ~/play и назовите его games.
	6. Лишите владельца файла ~/feathers права на чтение.
	7. Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой cat?
	8. Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?
	9. Дайте владельцу файла ~/feathers право на чтение.
	10. Лишите владельца каталога ~/play права на выполнение.
	11. Перейдите в каталог ~/play. Что произошло?
	12. Дайте владельцу каталога ~/play право на выполнение.
5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте, приведя примеры.

# Выполнение лабораторной работы

## Выполните все примеры, приведённые в первой части описания лабораторной работы.
### Пример №1 
1. Копирование файла в текущем каталоге. Скопировать файл ~/abc1 в файл april и в файл may:
![1](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.48.52.png)
2. Копирование нескольких файлов в каталог. Скопировать файлы april и may в каталог monthly:
![2](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.50.50.png)
3. Копирование файлов в произвольном каталоге. Скопировать файл monthly/may в файл с именем june:
![3](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.52.16.png)
### Пример №2 
1. Копирование каталогов в текущем каталоге. Скопировать каталог monthly в каталог monthly.00:
![1](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.53.49.png)
2. Копирование каталогов в произвольном каталоге. Скопировать каталог monthly.00 в каталог /tmp
![2.1](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.56.25.png)
![2.2](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2013.58.02.png)
### Пример №3
1. Переименование файлов в текущем каталоге. Изменить название файла april на july в домашнем каталоге:
![1](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.00.01.png)
2. Перемещение файлов в другой каталог. Переместить файл july в каталог monthly.00:
![2](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.01.02.png)
3. Переименование каталогов в текущем каталоге. Переименовать каталог monthly.00 в monthly.01
![3](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.01.56.png)
4. Перемещение каталога в другой каталог. Переместить каталог monthly.01 в каталог reports:
![4](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.03.50.png)
5. Переименование  каталога,  не  являющегося  текущим.  Переименовать  каталог reports/monthly.01 в reports/monthly:
![5](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.05.20.png)
### Пример №4
1. Требуется создать файл ~/may с правом выполнения для владельца:
![1](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.07.52.png)
2. Требуется лишить владельца файла ~/may права на выполнение:
![2](https://github.com/ate4/study_2022-2023_os-intro/blob/740588d3389f288c368b52f5cdf920d1a2e6af8e/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.08.29.png)
3. Требуется создать каталог monthly с запретом на чтение для членов группы и всех остальных пользователей:
![3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.52.41.png)
4. Требуется создать файл ~/abc1 с правом записи для членов группы:
![4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.10.56.png)
### Пример №5 
1. Для просмотра используемых в операционной системе файловых систем можно воспользоваться командой mount без параметров. В результате её применения можно получить примерно следующее:
![1](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.11.46.png)
2. Другой способ определения смонтированных в операционной системе файловых систем — просмотр файла/etc/fstab. Сделать это можно например с помощью команды cat:
![2](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.13.47.png)
3. Для определения объёма свободного пространства на файловой системе можно воспользоваться командой df, которая выведет на экран список всех файловых систем в соответствии с именами устройств, с указанием размера и точки монтирования. 
![3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.14.26.png)
4. С помощью команды fsck можно проверить (а в ряде случаев восстановить) целостность файловой системы:
![4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.15.50.png)
## 2.	Выполните следующие действия, зафиксировав в отчёте по лабораторной работе используемые при этом команды и результаты их выполнения:
1. Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его equipment. Если файла io.h нет, то используйте любой другой файл в каталоге
/usr/include/sys/ вместо него.
![2.1](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.21.41.png)
2. В домашнем каталоге создайте директорию ~/ski.plases.
![2.2](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.22.29.png)
3. Переместите файл equipment в каталог ~/ski.plases.
![2.3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.23.17.png)
4. Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.
![2.4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.24.23.png)
5. Создайте в  домашнем  каталоге  файл  abc1 и  скопируйте  его  в  каталог ~/ski.plases, назовите его equiplist2.
![2.5](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.25.58.png)
6. Создайте каталог с именем equipment в каталоге ~/ski.plases.
![2.6](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.28.48.png)
7. Переместите  файлы   ~/ski.plases/equiplist и   equiplist2 в   каталог ~/ski.plases/equipment.
![2.7](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.30.17.png)
8. Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите его plans.
![2.8](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.33.25.png)

## 3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав нет:
1. drwxr--r--	...	australia
![3.1](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.37.02.png)
2. drwx--x--x	...	play
![3.2](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.40.16.png)
3.  -r-xr--r--	...	my_os
![3.3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.43.11.png)
4.  -rw-rw-r--	...	feathers
![3.4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.44.20.png)
## 4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной работе используемые при этом команды:
4.1.	Просмотрите содержимое файла /etc/password.
![4.1](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.45.15.png)
4.2.	Скопируйте файл ~/feathers в файл ~/file.old.
![4.2](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.46.29.png)
4.3.	Переместите файл ~/file.old в каталог ~/play.
![4.3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.51.29.png)
4.4.	Скопируйте каталог ~/play в каталог ~/fun.
![4.4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.53.01.png)
4.5.	Переместите каталог ~/fun в каталог ~/play и назовите его games.
![4.5](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.54.36.png)
4.6.	Лишите владельца файла ~/feathers права на чтение.
![4.6](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.56.38.png)
4.7.	Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой cat?
![4.7](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.57.06.png)
4.8.	Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?
![4.8](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.57.44.png)
4.9.	Дайте владельцу файла ~/feathers право на чтение.
![4.9](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.58.27.png)
4.10.	Лишите владельца каталога ~/play права на выполнение.
![4.10](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.59.31.png)
4.11.	Перейдите в каталог ~/play. Что произошло?
![4.11](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2014.59.59.png)
4.12.	Дайте владельцу каталога ~/play право на выполнение.
![4.12](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.00.32.png)
## 5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте, приведя примеры.
1. **mount** монтирует запоминающее устройство или файловую систему , делая их доступными и присоединяя к существующей структуре каталогов
![5.1](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.01.09.png)
2. **fsck** утилита командной строки, которая позволяет выполнять проверки согласованности и интерактивное исправление в одной или нескольких файловых системах Linux.
![5.2](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.01.33.png)
3. **mkfs** создаёт новую файловую систему Linux  
![5.3](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.01.51.png)
4. **kill** посылает сигнал процессу или выводит список допустимых сигналов 
![5.4](https://github.com/ate4/study_2022-2023_os-intro/blob/c6a8dc76f0f30cadef5d65519842d8e6d11c8822/labs/lab05/report/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-05-04%20%D0%B2%2015.02.07.png)


# Выводы
В результате работы ознакомилась с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретила практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.



