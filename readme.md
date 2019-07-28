# 1. Скачайте последнюю версию WebStorm

https://www.jetbrains.com/webstorm/download

# 2. Распакуйте дистрибутив при помощи архиватора 7zip

https://www.7-zip.org/

![Screenshot](img/12.JPG)

# 3. Заходим в полученную папку с программой

* Удалите папку **$PLUGINSDIR**

> эта папка бесполезна

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/0.JPG)

*  Перейдите в папку **bin** и найдите там файл конфигурации **idea.properties**

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/01.JPG)

* Откройте его с помощью Notepad и измените пути хранения настроек cо стандартных:

```
# idea.config.path=${user.home}/.WebStorm/config

# idea.system.path=${user.home}/.WebStorm/system
```

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/1.JPG)

на следующие:

```
idea.config.path=${idea.home}/config

idea.system.path=${idea.home}/system
```
> не забудьте раскомментировать эти строки (убрать # в начале строки)

* Вот что должно получиться: 

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/2.JPG)

# 4. Переносим настройки и плагины с ПК версии программы на портативную

* Заходим в копьютере на котором утановлен WebStorm в следующую директорию:
```
C:\Users\<USER ACCOUNT NAME>\.<PRODUCT><VERSION>
```

> \<USER ACCOUNT NAME\> - имя пользователя ПК

> .\<PRODUCT\>\<VERSION\> - папка WebStorm'а с пользовательскими настройками. С каждой новой версией её имя меняется. На текущий момент папка именуется как .WebStorm2019.2

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/3.JPG)

* Копируем папки **config** и **system** в корень папки портативной версии программы

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/4.JPG)

> Теперь все готово для копирования папки с программой на флешку

* Копируем папку с программой на флешку

# 5. Запуск WebStorm с флешки

* Чтобы запустить WebStorm нужно запустить файл **webstorm64.exe**, либо **webstorm.exe** (если у вас установлена 32-битная ОС), которые находятся в папке **bin**:

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/5.JPG)

# 6. Создаем ярлык для запуска WebStorm в корне флешки для простоты запуска портативной версии

> С помощью данного ярлыка вы сможете запускать WebStorm не смотря на то, какое имя диска будет дано вашему флешнакопителю при подключении к ПК

* Через Проводник Windows заходим на флешку и вызываем Мастер создания ярлыков

> Нажимаем правой кнопкой миши по пустой области в проводнике и выбираем пункт 'Cоздать' и 'Ярлык'

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/6.JPG)

* В открывшемся диалоговом окне, в строке 'Укажите расположение объекта' вводим:

```
%windir%\system32\cmd.exe /C start /B /D \WebStorm-2019.2 \WebStorm-2019.2\bin\webstorm64.exe
```

> %windir%\system32\cmd.exe /C start /B /D \\\*путь до папки с программой* \\\*путь до папки с программой*\\\*название файла.exe*

>если вы хотите разместить ярлыки в отдельной папке (например, в корне флешки создали дополнительную папку), то вам нужно указать командной строке, что она должна вернуться на папку назад. Для этого перед первым слешем в пути ставим точку '.'

> %windir%\system32\cmd.exe /C start /B /D .\\\*путь до папки с программой* .\\\*путь до папки с программой*\\\*название файла.exe*

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/7.JPG)

* Нажимаем 'Далее' и даем имя ярлыку (любое, на ваше усмотрение):

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/7-1.JPG)

* Нажимаем 'Готово' и у нас теперь появился ярлык для запуска WebStorm. Но это еще не все. Теперь заходим в 'Свойства' нашего ярлыка и удаляем содержимое поля 'Рабочая папка':

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/8.JPG)

* Для того, чтобы при запуске не отображалось окно командной строки, в поле 'Окно' выбираем 'Свернутое в значок':

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/9.JPG)

* Также здесь можем присвоить пиктограмму WebStorm'а нашему ярлыку:

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/10.JPG)

# 7. Портативная версия WebStorm готова!

![Screenshot](https://github.com/MaksimBorovik/Guide-How-to-create-WebStorm-Portable/blob/master/img/11.JPG)

> Скачав архив с данного репозитория вы можете найти в нем уже отредактированный файл **idea.properties**, готовый ярлык и папки **config** и **system** с моими конфигурациями и натройками WebStorm'а

> **Enjoy!**