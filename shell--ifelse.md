# if
``` shell
if [ condition ]; then 
    command
    command
    else
    command
fi 
```

``` shell
if test condition;then  
    command
if
```
```shell
[ condition ] && command || command
 
```
```shell
# script
#!/bin/bash 
# 判断两台主机是否ping通

read -p "请输入要ping的ip" ip
ping -c1 $ip &>/dev/null
if [[ $? = 0 ]]; then
        echo "和$ip互通"
    else
        echo "不互通"
fi
````

```shell
# script
#!/bin/env bash
# 判断web服务器中的httpd进程是否存在

pgrep http &>/dev/null
if [[ $? = 0 ]]; then
        echo "存在"
    else
        echo "不存在"
fi
````

# wget

```shell
# script
#!/bin/env bash
# 判断网站是否能否正常访问

read -p 'inter the web addr' web
wget -P /shell/ $web &>/dev/null
[[ $? =0 ]] && echo "OK" && rm -f /shell/index.* || echo "not ok"
````
# curl www.baidu.com
# elinks -dump www.baidu.com