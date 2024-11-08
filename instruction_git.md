# **Инструкция по работе с Git**

## Общая информация о Git

Git - одна из реализаций систем контроля версий, имеющая как локальную версионность, так и версионность на сервере. Git является самой популярной системой контроля версий на сегодняшний день.

## Создание нового репозитория

Для того, чтобы создать репозиторий в указанной папке, используется команда git init. Для этого достаточно написать команду git init в папке с будущем репозиторием.

        git init
## Проверка состояния репозитория
        git status - отображает состояние рабочего каталога и раздела проиндексированных файлов. С ее помощью можно проверить индексацию изменений и увидеть файлы, которые не отслеживаются git.
## Добавление изменений к индексу
        git add - один из способов добавить все измененные файлы в индекс репозитория git.
## Создание коммитов
        git commit - команда для создания новой фиксации. Команда пишет как: *git commit -m <сообщение к коммиту>*. Перед этим все файлы должны быть предварительно добавлены с помощью команды *git add*
 ## Перемещение между сохранениями
      Для перемещения между коммитами, необходимо использовать команду *git checkout*. Используется она следующем образом в папке с репозиторием: *git checkout <номер коммита>*.         
 ## Журнал изменений
       Для просмотра журнала изменений, необходимо использовать команду *git log*. Для этого нужно в папке с репозиторием напистаь *git log*. 
       ## Ветки в Git 

### Создание веток в Git

Для того, чтобы создать новую ветку, необходимо использовать команду *git branch*. Используется она следующим образом в папке с репозиторием: *git branch <название ветки>*.

### Просмотр списка веток

Для того, чтобы просмотреть список веток, необходимо использовать команду *git branch*. Для этогов папке с репозиторием надо набрать *git branch*.

### Переход между ветками

Для того, чтобы перейти на другую ветку, необходимо использовать команду *git checkout*. Используется она следующим образом в папке с репозиторием: *git checkout <название ветки>*.

## Слияние веток и разрешение конфликтов

### Слияние веток

Для слияния веток, необходимо использовать команду *git merge*. Используется она сдедующим образом: для начала ***ОБЯЗАТЕЛЬНО*** перейти на ветку, куда мы сливаем изменения, после чего надо воспользоваться командой *git merge <название сливаемой ветки>*. Слияние может произойти автоматически, а может возникнуть конфликт. Про разрешение конфликтов смотри дальше.

### Разрешение конфликтов

При выполнения слияние двух веток, может возникнуть конфликт. Для его разрешения необходимо выбрать один из четырех вариантов: оставить изменения текущей ветки, принять изменения сливаемой ветки, оставить оба изменения или отредактировать в ручную. После разрешения конфликта ***ОБЯЗАТЕЛЬНО*** сохранить файл и сделать его фиксацию.

## Удаление веток

Для удаление веток, необходимо воспользоваться командой *git branch -d <имя удаляемой ветки>*.

## Работа с удаленными репозиториями

### Создание связи VSC и GitHub

Для создания связи VSC и GitHub, необходимо в своем аккаунте зайти во вкладку *Your repositories*, нажать на кнопку *New*, задать имя репозитория и нужные настройки. После зайти в VSC, зайти в папку, с которой необхходимо создать связь и в терминале записать следующие команды:
>git remote add origin <ссылка на репозиторий> - создаем связь с репозиторием на GitHub  
>git branch -M master - принудительно перемещаем\переименовываем ветку на master   
>git push origin master - заливаем файлы в удаленный репозиторий (об этом ниже). 

### Получение данных с удаленнго репозитория

Для того, чтобы "стянуть" " изменения с удаленного репозитория, необходимо воспользовать командой *git pull origin master*. 

### Добавление изменений в удаленный репозиторий

Для того, чтобы "слить" данные в удаленный репозиторий, необходимо воспользоваться командой *git push origin master*. Если в удаленном репозитории произошли изменения, необходимо стянуть данные, разрешить все конфликты и затем вновь слить данные в удаленный репозиторий. 