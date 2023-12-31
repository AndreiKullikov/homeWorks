![git logo](Git-Logo-1788C.png)
# Работа с  GIT и GITHub
## 1. Проверка наличия установленного Git
В терминале выполнить команду `git version` Если git установлен появится сообщение о версии программы иначе будет сообщение о ошибке.
## 2. Установка Git
Загружаем последнюю версию git c сайта [установка git](https://git-scm.com/downloads).
Устанавливаем с найстройкми по умолчанию.
## 3. Настройка Git 
При первом использовании Git необходимо представиться.
Для этого нужно ввести в терминале 2 команды:
```
git config --global user.name «Ваше имя английскими буквами»
git config --global user.email ваша почта@example.com
```
## 4. Инициализация репозитория
в терминале переходим к папке, в которой хотим создать репозиторий. Выполняем команду: 
```
git init
```
## 5.Создание коммитов
1.Для добавления изменений в коммит используется команда *git add*.Чтобы использовать команду *git add* напишите *git add <имя файла>*

2.Для того,чтобы посмотреть состояние репозитория используется команда *git status* Для жтого необходимо в папке с репозиторием написать *git status* и Вы увидите были ли изменения в файлах, или их не было.
3.Для того, чтобы создать commit(сохранение)необходимо выполнить команду *git commit*
Выполняеться она так: 
```
**git commit -a -m "в ковычках пишите сообщение что вы добавили в coomit"**
```
## 6.Просмотр истории комитов 
Для того что бы посмотреть историю всех коммитов в одной ветке введите команду:
```
git log
```
Так же вы можете вывести все коммиты через одну строчку, используя команду:
```
git log --oneline
```
## 7. Перемещение между коммитами
Для того что бы перейди из одной версии коммита в другую введите команду:
```
git checkout "первые 4-5 чисел номера коммита"
```
## 8. Игнорирование файлов
Для того, чтобы исключить из отслеживания в репозитории определенный файл или папки, необходимо создать там файл `.gitignore`
и записать в него их названия или шаблоны, соответсвущие таким файлам или папкам.

## 9. Создание веток в Git
По умолчанию, имя основной ветки в **Git - master.**
Создать ветку можно командой:

```
git branch "название для новой ветки"
```
Список веток в репозитории можно посмотреть с помощью команды:
```
git branch
```
Текущая ветка будет отмечена звездочкой: __* master__
Для создания новой ветки и автомотического переключения на нее используйте команду:
```
git checkout -b "название новой ветки"
```
## 10. Слияние веток и разрещение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить команду:
 ```
git merge "название выбранной ветки"
```
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт, который потребует участие пользователя. Vscode предлагает варианты разрешений конфликта.
Что бы разрешить конфликт, нужно выбрать один из вариантов, либо обьеденить содержимое по-своему.
После обьеденение веток выполнить коммит слияния 
Для того что бы посмотреть историю слияния веток, используйте команду 
```
git log --graph
```

## 11.Удаление веток
Для удаление не нужной ветки используйте команду:
```
git branch -d "название ветки"
```
Если вы хотите удалить ветку, в который были изменения, и эти изменения не внесены в основную ветку, то используйте команду:
```
git branch -D "название ветки"
```
