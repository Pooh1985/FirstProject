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

