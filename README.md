## **Создание репозитория в GitHub**
1. Создать директорию  
mkdir FirstProgect  
2. Создать файл внутри директории  
touch README.md  
3. Сделать директорию git репозиторием  
git init  
4. Добавить файл README.md для отслеживания состояния  
git add README.md  
5. Отредактировать файл README.md  
6. Закоммитить изменения  
git commit -m 'что сделано'  
7. Сгеренировать SSH ключ  
ssh-keygen -t ed25519 -c "email c GitHub"  
8. Проверить, что ключ создан  
ls -a~/.ssh  
9. Скопировать содержание публичного ключа в буфер обмена  
clip < ~/.ssh/id_25519.pub  
10. Добавить ключ  
git remote add origin https://github.com/Pooh1985/FirstProject.git (имя репозитория)  
11. Изменить url  
git remote set-url origin https://github.com/Pooh1985/FirstProject.git  
12. Сохранить изменения в файле  
13. Отправить изменения на удаленный репозиторий  
git push -u origin master  

## **Хеш коммита**  
Хеш уникален. Содержит информацию об авторе, дате и изменениях  
Команда **cat HEAD** покажет служебный файл  
Команда **cat имя служебного файла** покажет хеш последнего коммита  

## **Cтатусы файлов**  
1. **untracked** - Неотслеживаемый. GIT знает о нем, но не следит за изменениями  
2. **staget** - Подготовленный. Файл попадает в статус **staget** после команды **git add название файла**  
3. **tracked** - Отслеживаемый файл. В этот статус файл покадает после команд **git add** и **git commit** 
4. **modified** - Статус файла, в котором были добавлены изменения, но не были закоммичены.  

## **Откат назад**  
**git restore --staged <file>** переведёт файл из staged обратно в modified или untracked.  
**git reset --hard <commit hash>** «откатит» историю до коммита с хешем <hash>. Более поздние коммиты потеряются!  
**git restore <file>** «откатит» изменения в файле до последней сохранённой (в коммите или в staging) версии  

## **Просмотр изменений**  
**git diff** не покажет изменений после git add.  
**git diff --staged** покажет изменения в staged файлах
