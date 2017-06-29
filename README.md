# github-command
<h4>Установка</h4>
Под <a href="https://git-scm.com/download/win">Windows</a> или под Linux:<br />
```bash<br />
sudo apt-get update<br />
sudo apt-get install git<br />
```

<h4>1 шаг: открываем терминал и устанавливаем первоначальные конфигурации</h4>
```bash
git config --global user.name 'имя_пользователя_github'<br />
git config --global user.email 'ваша_электронная_почта'<br /><br />
git config --global color.diff 'auto'<br />
git config --global color.status 'auto'<br />
git config --global color.branch 'auto'<br />
git config --global credential.helper store<br />
git config --global push.default simple<br />
git config --global core.autocrlf false<br /><br />
git config --global core.eol lf<br />
```

<h4>2 шаг: клонируем репозиторий</h4>
```bash<br />
mkdir C:/develop/ #cоздаем папку на диске C (если Windows)<br />
git clone https://github.com/user/titlerepository # копируем свой репозиторий на компьютер<br />
cd titlerepository/ #заходим в локальный репозиторий<br />
```<br />

<h4>3 шаг: обновляем изменения на гитхабе</h4>
```bash
# производим изменения<br />
# git отслеживает только изменения в файлах<br />
# (создание, удаление, редактирование)<br />
# git не видит созданную пустые директории<br />
# чтобы директории были сохранены на сервере<br />
# в пустых директориях необходимо присутствие<br />
# новых, созданных или перемещенных в них файлов<br />

git add . #производится индексирование файлов на предмет изменения в них<br />
git commit -m "update" #фиксируем публикацию, комментируем изменения<br />
git push -f #отправляем на сервер GitHub<br />
