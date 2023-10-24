# Computer-networks-7
Компьютерные сети (семинары) Урок 7. NAT. GRE.

1. Настроить сеть согласно схеме в файле, где:<br>
— Office 1 — cеть 10.1.1.0/24<br>
— Office 2 — cеть 10.0.0.0/16<br>
— Office 3 — cеть 172.16.0.0/16<br>
— Office 4 — cеть 192.168.145.0/24<br>
— Где “Интернет” — там имитация Интернета с помощью OSPF, выберите сами публичные сети между роутерами.<br><br>
![network_all](img/network_all.jpg)<br><br>
Задача 1. Настроить на Port Forwarding на сервера в Office 2. Server0 должен предоставлять HTTP по 80му порту, а Server1 должен предоставлять HTTPS по 443 порту. Странички должны быть разные.<br><br>
![HTTP_HTTPS](img/HTTP_HTTPS.jpg)<br><br>
Задача 2. Настроить PAT в Office 3 для компьютеров, чтобы они выходили в интернет под одним публичным IP адресом на Router1.<br>
![NAT_translation](img/NAT_translation.jpg)
Предоставить скриншот открытых страниц по HTTP и HTTPS по публичному адресу Router3 в веб-браузере клиентов Office3 (с РС1 и РС0);
После чего предоставить вывод show ip nat translation c Router1.<br><br>

Задача 3. Связать сети Office 1 и Office 4 с помощью GRE. Предоставит трейс с Laptop0 до Server2.<br><br>
![tracert_by_tunnel](img/tracert_by_tunnel.jpg)
Задача 4. Доделать OpenVPN, если не успели. Предоставить скриншот публичного IP до и после подключения через VPN + скриншот вывода команды ip addr.
Учтите что в Yandex Cloud есть два нюанса:<br>
— если создавать прерываемую машину, то публичный адрес будет меняться после перезапуска;<br>
— на машине Yandex делает приватный IP, но одновременно в виртуализации создается Static NAT 1:1 в ваш публичный IP.<br>
![yandex_v](img/yandex_v.jpg)
![open_vpn](img/open_vpn.jpg)
