# LR6
## __Лабораторная работа №6__
### __Система контроля версий__
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке "Screenshots", каждый из скриншотов имеет название, соответствующее номеру пункта (например, _1.png_ для Пункта 1).
## Пункт 1
Был создан аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/NotChelovec/LR6/blob/master/Screenshots/1.png)_).
## Пункт 2
При помощи Fork была создана копия репозитория лабораторной работы (_см. [рис. 2](https://github.com/NotChelovec/LR6/blob/master/Screenshots/2.png)_).
## Пункт 3
Предварительно был установлен Git (_см. [рис. 3](https://github.com/NotChelovec/LR6/blob/master/Screenshots/3.png)_).
## Пункт 4
С помощью команд _git config user.name_ и _git config user.email_ был настроен клиент git (_см. [рис. 4](https://github.com/NotChelovec/LR6/blob/master/Screenshots/4.png)_).
## Пункт 5
В рабочей директории была создана копия личного удалённого репозитория с помощью команды _git clone_ (_см. [рис. 5](https://github.com/NotChelovec/LR6/blob/master/Screenshots/5.png)_).
## Пункт 6
Через интерфейс GitHub был добален файл с названием text, и с помощью команды _git pull_ изменения были подтянуты в локальный репозиторий (_см. [рис. 6](https://github.com/NotChelovec/LR6/blob/master/Screenshots/6.png)_).
## Пункт 7
История операций для каждой для веток была получена с помощью команды _git reflog_ (_см. [рис. 7](https://github.com/NotChelovec/LR6/blob/master/Screenshots/7.png)_).
## Пункт 8
Просмотр последних изменений был осуществлён с помощью команды _git log_ (_см. [рис. 8](https://github.com/NotChelovec/LR6/blob/master/Screenshots/8.png)_).
## Пункт 9
С помощью команды _git merge_ было выполнено слияние веток master и new_branch (_состояние файлов до и после слияния показано с помощью ls -1, см. [рис. 9](https://github.com/NotChelovec/LR6/blob/master/Screenshots/9.png)_).
## Пункт 10
После слияния побочная ветка была удалена командой _git branch -d_ (_см. [рис. 10](https://github.com/NotChelovec/LR6/blob/master/Screenshots/10.png)_).
## Пункт 11
Последовательно были созданы три текстовых файла. После каждого создания изменения фиксировались командой _git add_, создавался коммит (_git commit_) и обновлялся репозиторий (_git push_) (_см. [рис. 11.1](https://github.com/NotChelovec/LR6/blob/master/Screenshots/11.1.png), [рис. 11.2](https://github.com/NotChelovec/LR6/blob/master/Screenshots/11.2.png), [рис. 11.3](https://github.com/NotChelovec/LR6/blob/master/Screenshots/11.3.png)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлён откат последнего коммита (_см. [рис. 12](https://github.com/NotChelovec/LR6/blob/master/Screenshots/12.png)_).

# Лог команд
git config --global user.name "4316 Рябов Д.С."

git config --global user.email "totktonushen@gmail.com"

git clone https://github.com/NotChelovec/LR6

git pull

ls -1

git reflog

git log

git checkout new_branch

ls -1

git checkout master

ls -1

git merge new_branch

ls -1

git branch -d new_branch

echo "Some text" >> file1.txt

git status

git add file1.txt

git status

git commit -m "Файл 1 добавлен"

git push

echo "Some text" >> file2.txt

git status 

git add file2.txt

git status

git commit -m "Файл 2 добавлен"

git push

echo "Some text" >> file3.txt

git status

git add file3.txt

git status

git commit -m "Файл 3 добавлен"

git push

git revert HEAD --no-edit

# Историй операций
С помощью команды _git log --pretty=format:"%h - %ad - %an: %s" --date=short_ была получена история операций в укороченном виде.

b23d959 - 2024-11-14 - 4316 Рябов Д.С.: Revert "Файл 3 добавлен"

fc8ca2b - 2024-11-14 - 4316 Рябов Д.С.: Файл 3 добавлен

3b54516 - 2024-11-14 - 4316 Рябов Д.С.: Файл 2 добавлен

2f3ea4d - 2024-11-14 - 4316 Рябов Д.С.: Файл 1 добавлен

c8d18e9 - 2024-11-14 - 4316 Рябов Д.С.: Добавлен файл в ветку

52aa7ae - 2024-11-14 - Daniil: Create text

921f53b - 2020-11-21 - Kurtyanik: Обновление информации

c08a654 - 2020-11-21 - Kurtyanik: Файл создан пустым

3c6e913 - 2020-11-21 - Kurtyanik: Initial commit
