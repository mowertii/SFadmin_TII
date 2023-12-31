**Создать три новых виртуальных машины**: две на Ubuntu и одну на Red Hat.
Можно использовать один ключ для авторизации на всех трёх серверах.

***На 1-й сервер вам нужно установить Zabbix, Grafana, Ansible, filebeat, OpenVPN-server*** (учтите, чтобы избежать проблем с файроволами и политиками AWS, используется TCP).

Склонировать свой репозиторий Ansible с GitHub на 1-й сервер.

*Установка сервисов на остальные серверы должна производиться с помощью ролей и playbooks Ansible.*

Вам придётся писать свои новые роли Ansible для установки необходимых сервисов. Конечно, можно использовать и существующие (например, роли на GitHub), но лучше писать свои. Во-первых, для нарабатывания практики, во-вторых, несмотря на то, что готовых ролей на GitHub очень много, вам всё равно придётся их проверять, так как часть из них неактуальные, часть обладает сильно избыточным функционалом. Ну и стоит помнить, что проверка чужих программ и скриптов является хорошей практикой в тех случаях, когда это возможно.

*На двух оставшихся серверах вам нужно будет установить и настроить OpenVPN для подключения к 1-му серверу. Дальнейшую настройку нужно делать по VPN адресам.*

Если вы понимаете, что для каких-то ролей вы не будете использовать роли Ansible, запишите их в README.txt в корне вашего репозитория для того, чтобы ментору было проще проверять ваше задание.

***На второй установить nginx, Apache, PHP, Zabbix-agent, bind, mail, filebeat.***

***На третий сервер — PostgreSQL-12, Zabbix-agent, ELK.***

Все новые роли, которые написали или скачали себе, вам нужно будет выгрузить на GitHub. Постарайтесь без чувствительных данных.

***Сервисы zabbix-server, Kibana, Grafana, nginx должны быть доступны снаружи*** (не забудьте сменить пароли для сервисов).



**Обратите внимание!**

*Проверка ментором будет осуществляться в третьей части итогового проекта. Прежде чем переходить дальше, проверьте, что вы выполнили все задания этой части.*
