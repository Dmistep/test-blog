---
layout: post
#tags: []
categories: Microsoft
#date: 2022-07-03 20:02:13
#excerpt: 'Итак, если вы используете Firefox в качестве браузера, я рекомендую установить бинарную версию с веб-сайта Mozilla. Он будет работать немного быстрее и будет полностью интегрирован в ваш рабочий стол.'
#image: 'BASEURL/assets/blog/img/.png'
#description:
permalink: /service-hdd/
title: 'Обслуживание диска chkdsk'
---

*Пример команды которую необходимо ввести в Командную Строку выглядит следующим образом*:

`chkdsk [Drive:] [parameters]`

*В нашем случае это будет так*:

`chkdsk C: /f /r /x`

Для запуска Командной Строки от имени Администратора нажмите сочетание клавиш `Windows + X` и выберите необходимый пункт меню. Также, данное меню можно открыть, кликнув правой кнопкой мышки по меню Пуск.
В Командной Строке введите команду `chkdsk`, после этого букву диска, который необходимо проверить или восстановить.

*Пример:*

`chkdsk c: `

Обычный запуск команды `chkdsk` в Windows 10 просто покажет статус диска и не будет устранять никаких ошибок раздела. Для того чтобы команда исправляла ошибки на диске, необходимо задать параметры После буквы диска через пробел: `/f /r /x`

* `/f` даёт команду `chkdsk` исправлять все найденные ошибки; 
* `/r` – находить на диске битые (bad) сектора и восстанавливать читабельную информацию; 
* `/x` – останавливает диск до начала процесса. 

Для более специализированных заданий присутствуют также и дополнительные параметры.


[![Website](https://img.shields.io/website?style=for-the-badge&up_message=https%3A%2F%2Fshields.io%2Fcategory%2Fmonitoring&url=https%3A%2F%2Fshields.io%2Fcategory%2Fmonitoring)](https://shields.io/category/monitoring)

<a href="https://shields.io/category/monitoring"><img alt="Website" src="https://img.shields.io/website?style=for-the-badge&up_message=https%3A%2F%2Fshields.io%2Fcategory%2Fmonitoring&url=https%3A%2F%2Fshields.io%2Fcategory%2Fmonitoring"></a>



# diskpart
[![Website](https://img.shields.io/website?style=flat-square&up_color=blue&up_message=https%3A%2F%2Fwww.easeus.com%2Fpartition-master%2Fformat-hard-drive-using-command-prompt.html%231&url=https%3A%2F%2Fwww.easeus.com%2Fpartition-master%2Fformat-hard-drive-using-command-prompt.html%231)](https://www.easeus.com/partition-master/format-hard-drive-using-command-prompt.html#1)

[![Website](https://img.shields.io/website?style=flat-square&up_color=blue&up_message=https%3A%2F%2Fremontka.pro%2Fformat-disk-cmd%2F&url=https%3A%2F%2Fremontka.pro%2Fformat-disk-cmd%2F)](https://remontka.pro/format-disk-cmd/)

### Fully Clean,Format Disk and Create partition

*Пример команд которые необходимо ввести в Командную Строку выглядит следующим образом*:

- `list disk`
- `select disk 2` (Заменить 2 на номер выбираемого диска)
- `clean`
- `create partition primary`
- `format fs = ntfs quick`
- `assign` (назначь букву диска только что созданному разделу)

### Quick Format Disk Using DiskPart

- `list disk`
- `select disk 2` (Заменить 2 на номер выбираемого диска)
- `list volume`
- `select volume 10` (Заменить 10 номером тома раздела, который надо отформатировать)
- `format fs=ntfs quick` (если нужно отформатировать раздел жесткого диска в FAT32 или другие файловые системы, замени NTFS на FAT32 , exFAT и т. д.)

![Quick format hard drive with diskpart command.](https://www.easeus.com/images/en/screenshot/partition-manager/diskpart-quick-format-hard-drive.png)



###  Convert to GPT or MBR

При установке Windows (например, на этапе выбора разделов, но можно и в другом месте) нажмите клавиши **Shift + F10** на клавиатуре, откроется командная строка. Если то же самое вы делаете в ОС Windows, то командную строку нужно запускать от имени администратора.

- `diskpart`

- `list disk`

- `select disk N` (где N — номер диска, который нужно преобразовать)

- Теперь вы можете поступить двумя способами: ввести команду `clean`, чтобы очистить диск полностью (все разделы будут удалены), либо удалить разделы по одному вручную с помощью команд `detail disk`, `select volume` и `delete volume` (на скриншоте используется именно этот способ, но просто ввести clean будет быстрее).

- `convert gpt` (для того чтобы преобразовать диск в **GPT**. Или `convert mbr` чтобы преобразовать в **MBR**)

- `Exit`

После чего закройте командную строку и продолжайте установку Windows — теперь ошибка появляться не будет. Также вы можете создать разделы, нажав «Настроить диск» в окне выбора раздела для установки.

![Из GPT в MBR с помощью командной строки](https://remontka.pro/images/convert-gpt-mbr-command-line.png)



<style>
.img_link{
   width: 250px;
}

    </style>