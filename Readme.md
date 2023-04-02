# Инструкция по работе с *Markdown*

## Создание заголовков в языке *Markdown*
Для того, чтобы создать заголовок в языке *Markdown*, необходимо в начале строки написать несколько символов #. Количество символов # показывае уровень заголовка. Чем меньше уровень заголовка, тем больше текст(как в печате газет).

## Форматирование текста в языке *Markdown*
Для того, чтобы написать *курсивные текст*, необходимо этот текст поместить между двумя символами звёздочка, для **жирного текста** - между двумя парами звёздочек. ***Для курсивного жирного текста***, текст надо написать между двумя тройками звёздочек. Для написания ~~зачёркнутого~~ текста необходимо этот текст обрамить звумя парами символов ~(тильда).

Списки в языке *Markdown*
---------------------------
Списки в языке *Markdown* бывают:
+ Нумерованные
+ Ненумерованные
Для создания элемента нумерованного списка, перед текстом необходимо написать его номер в списке и поставить точку, например, 

Список продуктов:
1. Молоко
2. Яйца
3. Хлеб
Для создания элементов ненумерованного списка, перед элементом списка необходимо поставить любой из сиволов: +, -. 

Например, список продуктов:
+ Молоко
+ Яйца
+ Хлеб

## Ссылки в *Markdown*
Для добавления ссылки в языке *Markdown* необходимо написать в квадратных скобках текст ссылки, и рядом в круглых скобках адрес ссылки., например [Github](https://github.com)

## Работа с удаленными репозиториями

Для работы с удаленными репозиториями чаще всего используются следующие команды:
- **git clone** - копирует удаленную репозиторию в локальную папку компьютера;
- **git pull** - обновляет локальную репозиторию скачивая новые данные из связанной удаленной репозитории;
- **git push** - обновляет удаленную репозиторию закачивая новые данные из локальной репозитории;

Для публикации своего уже существующего локального проекта в сети необходимо:
1. создать пустую репозиторию в аккаунте (например на Github);
2. скопировать ее адрес;
3. в терминале *Git* локальной репозитории выполнить команды:
    - **git remote add <origin_repo> https://github.com/account/remote_repo.git**\
    , где *<origin_repo>* - это название удаленного репозитория, а *https://github.com/account/remote_repo.git* - это скопированная ссылка на этот удаленный репозиторий;
    - **git branch -M <main_branch>**\
    , где *main_branch* - это название новой ветки, которая станет главной в удаленной репозитории;
    - **git push -u <origin_repo> <main_branch>**;

    таким образом мы отправляем всю нашу локальную репозиторию в сеть на портал *Github* в свой аккаунт, где она сможет быть доступна всем желающим или ограниченному кругу лиц, если станет необходимо.

Для работы в коллективе над одним проектом наобходимо:
1. сделать копию рабочей репозитории на портале в сети к себе в аккаунт с помощью функции *fork* (вилка);
2. скопировать созданную удаленную репозиторию к себе в локальную папку и создать в ней новую рабочую ветку:
    - **git clone https://github.com/account/remote_repo.git**
    - **git branch _new_working_branch_**
3. после сохранения всех сделанных правок и коммита отослать предложение принять работу в общий проект:
    - **git pull**
    - **git push**
    - воспользоваться функцией *pull request* на портале
