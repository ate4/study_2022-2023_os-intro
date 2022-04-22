---
## Front matter
lang: ru-RU
title: lab01
author: |
	Kate P. Mitichkina \inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 22 April, 2022 Moscow, Russia

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


# Лабораторная работа № 1. Установка и конфигурация операционной системы на виртуальную машину.

## Начало работы
![Приветствие](https://github.com/ate4/study_2022-2023_os-intro/blob/02ea7f607550d2c8232e8a3b3f22e7fc993909e9/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.39.18.png)

## Выбор операционной системы и имени виртуальной машины
![Выбор имени и дистрибутива](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.39.41.png)

## Выбор объема оперативной памяти
![Ползунок](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.39.50.png)

## Создание виртуального жесткого диска
![Создавать или нет виртуальный жесткий диск](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.39.57.png)

![Тип](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.40.12.png)

![Формат хранения](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.40.18.png)

![Объем жесткого диска и расположение его файла](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.40.29.png)

## Работа с виртуальной машиной
![Сайт Fedora Linux](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.44.41.png)

![Подключение диска](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.45.37.png)

![Попытка запустить виртуальную машину](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.46.30.png)


![Настройа языка](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.47.50.png)

![Настройа раскладки, времени и место расположения](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.48.08.png)

![Загрузка](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.48.18.png)

![Отключение диска](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.48.57.png)

![Настройка имя пользователя](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.49.40.png)

![Настройка пароля](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.49.50.png)

![Настройка завершина все готово к работке](https://github.com/ate4/study_2022-2023_os-intro/blob/07d0f762dae6b062e3e2231fba9d16f5d55c5dfb/labs/lab01/presentation/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-04-22%20%D0%B2%2014.50.02.png)
