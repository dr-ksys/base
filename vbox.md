
$ sudo pacman -S virtualbox virtualbox-guest-iso virtualbox-host-modules


Устанавливаем гостевые дополнения (Guest additions):

pacman -S virtualbox-guest-utils linux-headers
modprobe -a vboxguest vboxsf vboxvideo


Создаём virtualbox.conf в /etc/modules-load.d

vim /etc/modules-load.d/virtualbox.conf


Добавляем гостевые модули и видео в virtualbox.conf:

vboxguest
vboxsf
vboxvideo
