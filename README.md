# group_gshadow_passwd_shadow_experiment_perfomance_boot_ubuntu_20.04
experiment perfomance boot ubuntu , group , gshadow, passwd

1) Сделайте бекап в какую либо папку на случай сбоя можно будет восстановить из оригинального бекапа командой: 

cd ~ && sudo XZ_OPT=-9 tar -Jcvf backup-etc.tar.xz /etc/group  /etc/gshadow /etc/passwd /etc/shadow /etc/subgid /etc/subuid


2) Не извлекая отредактируйте все фаилы прямо в архиве с помощью блокнота  изменив в каждом строку griggorii на своё имя оно же играет роль на домашнию директорию

Затем c помощью терминала заидите в супер пользователя обязательно потому что придётся повторить пароль который затрется ранее извлекаемыми фаилами и выполните команду:

tar xvpf etc.tar.xz -C / && passwd <my_login>

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Проблема черный экран загрузитесь с лайв сиди и восстановите копию

sudo mount /dev/sda2 /mnt                                      <-example-</dev/sda№ № №> 

sudo mount --bind /dev /mnt/dev 

sudo mount --bind /proc /mnt/proc 

sudo mount --bind /sys /mnt/sys 

sudo chroot /mnt

cd /home/<my_login>

tar xvpf backup-etc.tar.xz -C /

____________________________________________________________________________________________________________________________________________________________________


1) Make a backup to any folder in case of a failure, you can restore from the original backup with the command:

cd ~ && sudo XZ_OPT=-9 tar -Jcvf backup-etc.tar.xz /etc/group  /etc/gshadow /etc/passwd /etc/shadow /etc/subgid /etc/subuid

2) Without extracting, edit all the files directly in the archive using notepad, changing in each line griggorii to your name, it also plays a role in the home directory

Then, using the terminal, log into the super user, be sure to repeat the password that will be overwritten by the previously extracted files and run the command:

tar xvpf etc.tar.xz -C / && passwd <my_login>

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


Black screen problem boot from live sit and restore a copy

sudo mount /dev/sda2 /mnt                                      <-example-</dev/sda№ № №> 

sudo mount --bind /dev /mnt/dev 

sudo mount --bind /proc /mnt/proc 

sudo mount --bind /sys /mnt/sys 

sudo chroot /mnt

cd /home/<my_login>

tar xvpf backup-etc.tar.xz -C /

___________________________________________________________________________________________________________________________________________________________________

This experiment is carried out in order to check whether loading on ordinary hdd disks is accelerated or not.

Данный эксперимент проводится для того что бы проверить ускоряется загрузка на обычных hdd дисках или нет



