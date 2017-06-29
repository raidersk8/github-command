# github-command
<h4>Установка</h4>
Под <a href="https://git-scm.com/download/win">Windows</a> или под Linux:
```bash
sudo apt-get update
sudo apt-get install git
```

<h4>1 шаг: открываем терминал и устанавливаем первоначальные конфигурации</h4>
```bash
git config --global user.name 'имя_пользователя_github'
git config --global user.email 'ваша_электронная_почта'
git config --global color.diff 'auto'
git config --global color.status 'auto'
git config --global color.branch 'auto'
git config --global credential.helper store
git config --global push.default simple
git config --global core.autocrlf false
git config --global core.eol lf
```

<h4>2 шаг: клонируем репозиторий</h4>
```bash
mkdir C:/develop/ #cоздаем папку на диске C (если Windows)
git clone https://github.com/user/titlerepository # копируем свой репозиторий на компьютер
cd titlerepository/ #заходим в локальный репозиторий
```

<h4>3 шаг: обновляем изменения на гитхабе</h4>
```bash
# производим изменения
# git отслеживает только изменения в файлах
# (создание, удаление, редактирование)
# git не видит созданную пустые директории
# чтобы директории были сохранены на сервере
# в пустых директориях необходимо присутствие
# новых, созданных или перемещенных в них файлов

git add . #производится индексирование файлов на предмет изменения в них
git commit -m "update" #фиксируем публикацию, комментируем изменения
git push -f #отправляем на сервер GitHub
