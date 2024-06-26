# Шпаргалка по работе с Git  
чтобы было проще вспоминать в следующий раз <br>
 **команды в консоле** <br> 
 ( **~** ) 		- - - - - *домашний раздел* <br>
 ( **.** ) 		- - - - - *текущий раздел* <br>
 ( **..** ) 	- - - - - *родительский раздел* <br> 
 **$ cd ..**	- - - - - *переход в родительский раздел* <br>
 **$ cd /d/git/this**    - - - - - *переход на диск **D** в раздел **git** в раздел __this__* <br>
 **$ pwd**		         - - - - - *где я?* <br>
 **$ ls**                - - - - - *содержимое раздела* <br>
 **$ ls -a**             - - - - - **_всё_** *содержимое раздела* <br>
 **$ ls -la**            - - - - - *всё про* **_всё_** *содержимое раздела* <br>
 **$ touch text.txt** 	 - - - - -*создать файл text.txt* <br> 
 **$ mkdir a**           - - - - -*создать раздел a* <br>
 **$ rm -rf a**          - - - - -*удалить раздел a рекурсивно и без вопросов* <br>
 **$ mkdir -p b/1/2**    - - - - -*создать раздел a, в нём раздел 1, в нём раздел 2* <br>
 **$ cp test.txt a/1**   - - - - -*копировать файл test.txt в раздел a/1* <br>
 **$ cp test.txt a/1 && cd a/1 && ls**    - - - - -  *скопировать, перейти, посмотреть* <br>

### Git
**$git version**        - - - - - *версия GIT и проверка его наличия* <br>
**$git init**           - - - - - *создаем репозиторий в текущем разделе* <br>
для удаления репозитория достаточно удалить скрытый раздел .git<br>
**$rm -rf .git**  			- - - - - *удалили .git* <br>
**$git status**            	- - - - - *проверка состояния репозитория* <br>
**$git add file.txt**       - - - - - *подготовить к сохранению file.txt* <br>
**$git add .**              - - - - - *подготовить к сохранению в текущем разделе* <br>
**$git add --all**          - - - - - *подготовить **всё** к сохранению* <br>
**$git commit -m 'коментарий'** - - - - - *коммит/сохранение с коментарием* <br>
**$git log**  			- - - - - *посмотреть историю коммитов* <br>

### GitHub
для подключения к удалёному репозиторию необходимо сделать следующее:<br>
* используя web-интерфейс создать на GitHub репозиторий <br>
---
* проверить наличие SSH-ключа в домашней директории <br>
**$ ls -l ~/.ssh** <br>
* при отсутствии ключа - сгенирировать SSH-ключи  <br>
**ssh-keygen -t ed25519 -C "email"** <br>
если указать passphrase, то надо будет её постоянно вводить <br>
* проверить результат генерации ключей <br>
**$ ls -l ~/.ssh** <br>
* скопировать содержимое публичного ключа в буфер<br>
**$ pbcopy < ~/.ssh/ir_ed25519** <br>
* в web-интерфейсе GitHub зайти в Setting > SSH and GPG keys > New SSH key <br>
заполнить поля Title (условное имя), тип оставить - Authentication <br>
в поле Key вставить информацию из буфера <br>
* проверить правильность ключа  <br>
**$ ssh -T git@github.com** <br>
---
* связать локальный и удалённый репозитории<br>
**$git remote add origin git@github.com:логин:проект.git**<br>
* совершить первую отправку в удалённый репозитории<br>
**$git push -u origin master/main**<br>
**$git push**  			- - - - - *следующие отправки* <br>
<br>
<br>

*

**$git**  			- - - - - ** <br>
**$git**  			- - - - - ** <br>
   
   
   
