# LR6
## Лабораторная работа №6
### Система контроля версий
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название, соответствующее номеру пункта, выполнение которого необходимо подкрепить этим самым скриншотом. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/ctpaterasd/LR6/blob/b7c1638ca4aadf3b3ec42a3d1939fc9c4c4610d4/screenshots/6.1.png)_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. [рис. 2](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.2.png)_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. [рис. 3](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.3.png)_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. [рис. 4](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.4.png)_).
## Пункт 5
Затем на диске С в папке infa была создана копия своего личного удалённого репозитория на компьютер (_см. [рис. 5](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.5.png)_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. [рис. 6](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.6.png)_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7, 8](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.7-8.png)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _patch-1_ были объединены (содержимое patch-1 появилось в ветке master, _см. [рис. 9](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.9.png)_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. [рис. 10](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.10.png)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: asd.txt, wasd.txt, qwerty.txt, созданные командой _echo "text" >> name.txt_. Извенения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 11.1](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.11.png); [рис. 11.2](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.12.png); [рис. 11.3](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.13.png)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 12](https://github.com/ctpaterasd/LR6/blob/101f7163fb8e13d134cfea9044413a541b1d2931/screenshots/6.14.png)_).

# Лог команд
git config --global user.name "4315 Демидов А.Д."

git config --global user.email "kerizmatik2@mail.ru"

cd /c/infs

git clone https://github.com/ctpaterasd/LR6

ls -1

git pull

ls -1

git reflog

git log

git checkout branch1

ls -1

git checkout master

ls -1

git merge branch1

ls -1

git branch -d branch1

git push origin --delete patch-1

echo "first in first out" >> first.txt

git add first.txt

git status

git commit -m "Добавлен первый файл"

echo "second lifesad" >> second.txt

git add second.txt

git status

git commit -m "Добавлен второй файл"

echo "thirdsasas" >> third.txt

git add third.txt

git status

git commit -m "Добавлен третий файл"

git push
git revert HEAD --no-edit

git commit -m "Откат коммита"

git push


# История операций
С помощью команды _git log --pretty=format:"%h - %ad - %an: %s" --date=short_ была получена история операций в укороченном виде.

101f716 - 2024-11-25 - 4315 Демидов А.Д. - Папка скриншотов*
b7c1638 - 2024-11-25 - 4315 Демидов А.Д. - Папка скриншотов
d3f4d79 - 2024-11-25 - 4315 Демидов А.Д. - Revert "Создан третий файл"
dcf88af - 2024-11-25 - 4315 Демидов А.Д. - Создан третий файл
09906b1 - 2024-11-25 - 4315 Демидов А.Д. - Создан второй файл
bebd961 - 2024-11-25 - 4315 Демидов А.Д. - Создан первый файл
086e8c6 - 2024-11-24 - 4315 Демидов А.Д. - Разрешен конфликт
13fbaba - 2024-11-24 - ctpaterasd - Update mergefile.txt
917fc4d - 2024-11-24 - ctpaterasd - Update mergefile.txt
a841cf6 - 2024-11-24 - ctpaterasd - Create alexeydas
6497beb - 2024-11-24 - ctpaterasd - Create alexeyasd
921f53b - 2020-11-21 - Kurtyanik - Обновление информации
c08a654 - 2020-11-21 - Kurtyanik - Файл создан пустым
3c6e913 - 2020-11-21 - Kurtyanik - Initial commit

