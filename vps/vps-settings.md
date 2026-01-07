Источник информации:
https://habr.com/ru/companies/lansoft_career/articles/956730/

Создать дополнительного пользователя, который может выполнять команды от root
Задать сложные пароли всем пользователям 
Сделать доступ по ключу для пользователя

Убрать root-доступ по ssh:
В /etc/ssh/sshd_config задать
PermitRootLogin no

Перенести ssh на порт, отличный от 22

Закрыть все порты, кроме необходимых

открыты порты:
unlimited-freedom@v517113:~$ sudo ufw status verbose