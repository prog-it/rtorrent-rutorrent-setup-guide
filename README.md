# rtorrent-rutorrent-setup-guide

Подробная справка по установке и настройке rTorrent + ruTorrent. Также пример конфигурации для nginx

- Cправка находится в файле ``setup-guide.txt``
- В файле ``.rtorrent.rc`` находится конфиг файл для rTorrent. Необходимы лишь минимальные правки
- В файле ``rtorrent`` находится init скрипт для запуска rTorrent

## Пояснения
- Конфиг файл для rTorrent последней версии из ветки [master](https://github.com/rakshasa/rtorrent)
- Демон rTorrent запускается от системного пользователя *rtorrent*
- В конфиг файле rTorrent настроено получение внешнего IP адреса с хоста ``externalip.example.com``, можно изменить или закомментировать соответствующие строки, если данный функционал не нужен. Это необходимо для тех, у кого динамический IP адрес
- В конфиг файле rTorrent по умолчанию включен DHT
- В конфиг файле rTorrent настроена автоподхватка торрент файлов из директории ``/home/torrents/.watch``. Торрент файл будет переименован, как описано в статье на [Хабрахабре](https://habrahabr.ru/post/238413/). Если необходимо изменить папку, то нужно исправить путь в двух местах
- Конфиг nginx приведен для хоста с root директорией в ``/var/www``
- Имя пользователя, который работает с ruTorrent: *username*. Можно изменить
