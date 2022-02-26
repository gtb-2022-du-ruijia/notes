# loop
```shell
for variable in {list}
    do
        command
        command
    done
```

```shell
for i in {0..50..2}
    do
        echo $i
    done
```


```shell
for variable in a b c
    do
        command
        command
    done
```
```shell
for i in a b c
    do
        echo $i
    done
```

```for i in {1..100..2}; do echo $i; done ```  
```for i in ${seq 10 -1}; do echo $i; done ```  
 seq 10 -2 0  will print 10 to 0 with a step of -2  

 ```shell
for i 
    do
        echo $i
    done
```
#### 不带列表 默认省略了in 后面的 $@ 可以用bash -x filename 来看


## expr1

 ```shell
for ((i=1;i<=5;i++))
    do
        echo $i
    done
```
# while
```shell

NTP=10.1.1.1
count = 0
while true
do 
    ntpdate $NTP &>/dev/null
    if [ $? -ne 0 ]; then
        echo "system date failed" | mail -s "check system date" email@.com
    else
        let count++
        if [ $count -eq 100 ]; then
        echo "system date success" | mail -s "check system date" email@.com && count=0
        fi
    fi

```

## until 
