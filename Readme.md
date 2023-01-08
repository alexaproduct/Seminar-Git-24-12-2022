# Инструкция по работе с Git

## Что такое Git?
Git - это наиболее популярная реализация распределенной системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/)

##  Подготовка репозитория
Для создания репозитория используется команда *git init*.Для этого необходимо в терминале перейти в пустую папку, где в будущем будет репозиторий. Затем в терминале с папкой написать команду *git init*.

## Создание коммитов

### Добавление файла к коммиту
Для добавления файла к текущему коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

### Создание коммита
Для создания коммита используется команда *git commit*. Для этого в терминале с папкой репозитория необходимо написать *git commit -m <Сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предыдущие коммиты используется команда *git checkout*. Для неоьходимо в журнале изменений, как показано в предыдущей части, нийти необходимый коммит и его номер. После чего в терминаое с папкой-репозиторием написать команду *git checkout <номер коммита>*. После применения этой команды Вы попадаете в состояние *Detached head*, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *git checkout master*.

## Ветки в Git

Для создания новой ветки используется команда *git branch*. Для этого необходимо в терминале с папкой-репозиторием написать команду *git branch <название ветки>*. После этого можно посмотреть список веток с новой созданной веткой, написав команду *git branch*. В данном списке активная ветка, в которой в настоящий момент вносятся все измениния, выделена заленым и звездочкой (*). Для перехода на новую ветку и начала работы и внесения изменений в ней необходимо написать команду *git checkout <название ветки>*. Ветки создаются из ветки *master*, однако при создании подразделов в существующих ветках документа подветка создается в одной из веток вышеуказанным способом.

## Слияние веток, разрешение конфликтов

### Слияние веток

Для слияния веток используется команда *git merge*. Для этого сначала необходимо перейти в ветку master с помощью команды *git checkout master*. После этого в терминале с папкой-репозиторием написать команду *git merge <название ветки, которую сливаем с master>*.

### Разрешение конфликтов

При возникновении конфликтов появится сообщение о конфликте в терминале, а в поле с текстом будут выделены версии из ветки master и сливаемой ветки разными цветами. Объединение возможно путем принятия ожного из варинтов, предлагаемого системой автоматически, так и вручную, удалив служебные выделения и обозначения. После разрешения конфликтов и создания финальной версии в master необходимо сохранить изменения и далее применить команды *git add <Название файла>* и *git commit -m <Сообщение к коммиту>*.

## Удаление веток
Для удаление веток используется команда *git branch -d <Название удаляемой ветки>*. Для этого в терминале папки-репозитория необходимо ввести вышеуказанную команду.