---
layout: post
#tags: []
categories: linux
#date: 2022-07-03 20:02:13
excerpt: 'Итак, если вы используете Firefox в качестве браузера, я рекомендую установить бинарную версию с веб-сайта Mozilla. Он будет работать немного быстрее и будет полностью интегрирован в ваш рабочий стол.'
#image: 'BASEURL/assets/blog/img/.png'
#description:
permalink: /install-favourite-browser/
title: 'Установка браузера в linux'
---
## Оригинальный Firefox

Firefox — это приложение в Ubuntu 22.04. К сожалению, он немного медленнее оригинального Firefox. Он также не полностью интегрирован в среду рабочего стола. Итак, если вы используете Firefox в качестве браузера, я рекомендую установить бинарную версию с веб-сайта Mozilla. Он будет работать немного быстрее и будет полностью интегрирован в ваш рабочий стол.

Эта установка будет иметь приоритет над версией Firefox, установленной посредством вашего менеджера пакетов.</mark> Чтобы запустить версию, установленную с помощью вашего менеджера пакетов, вам придётся запускать бинарник из терминала. Чтобы сделать это в большинстве дистрибутивов, откройте терминал и введите: <b>/usr/bin/firefox</b>.

Чтобы установить его, следуйте [инструкциям Mozilla](https://support.mozilla.org/ru/kb/ustanovka-firefox-na-linux#w_ustanovka-firefox-iz-bildov-mozilla-dlia-opytnykh-polzovatelei) :

* Скачать:

[страница загрузки Firefox ESR](https://www.mozilla.org/ru/firefox/all/#product-desktop-esr)

[страница загрузки Firefox](https://www.mozilla.org/ru/firefox/linux/?utm_medium=referral&utm_source=support.mozilla.org)

* Перейти в папку Download в терминале:

`cd ~/Downloads `

* Распакуйте архив:

`tar xjf firefox-*.tar.bz2 `

* Переместите файлы Firefox в /opt:

`mv firefox /opt `

* Создайте символическую ссылку на бинарный файл Firefox:

`ln -s /opt/firefox/firefox /usr/local/bin/firefox `

* Загрузите файл рабочего стола:

`wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications `

* Удалите снап-версию Firefox:

`sudo snap remove firefox `

или

`sudo snap disable firefox`

` sudo snap remove --purge firefox`

* Запустите новый Firefox, выполнив команду в терминале:

`/usr/local/bin/firefox `

Перейдите в Dock -> щелкните правой кнопкой мыши Firefox -> Добавить в избранное -> Переместите его наверх
<br>

## Yandex browser 

Сначала надо скачать клиент Яндекс Браузера на компьютер. После того как скачаете подходящий пакет, делаем следующее:

* Перейти в папку Download в терминале:

`cd ~/Downloads `

* Оказавшись в нужной папке, вводим команду 

`sudo dpkg -i yandex*.deb`

>Учтите, что терминал чувствителен к регистру, поэтому заранее убедитесь, что файл называется yandex, а не Yandex, например. Иначе ничего не сработает.

Файл начнет распаковываться, но процесс может завершится неудачно. И это нормально. Скорее всего, ошибка связана с тем, что системе не удалось разрешить зависимости.

Если ошибка не появилась и процесс завершился успешно, то для вас инструкция закончилась. 

Чтобы разрешить зависимости, после попытки распаковать браузер вводим в терминал команду :

`sudo apt-get Install -f`

Вводим пароль администратора.Потом вводим символ Y, чтобы подтвердить процесс загрузки зависимых компонентов для Яндекс.Браузера.

