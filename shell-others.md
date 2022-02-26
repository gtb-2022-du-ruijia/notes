## random
$RANDOM 0-32767
set | grep RANDOM
$[ $RANDOM%2] 0-1之间的随机数
$[ $RANDOM%50+1 ]   1-50之间的随机数

## shift
shift 2 使位置参数向右移动  

```shell
sum=0
for i 
do
let sum=$sum+$i
done
echo sum=$sum
```

## 数组
``` shell
    array2=($(ls))
    echo ${array1[1]}
    declare -a
```

## case 
```shell
case $1 in
    start|S)
    echo "CASE 1"
    ;;
    stop|T)
    echo "CASE 2"
    ;;
    reload|R)
    echo "CASE 3"
    ;;
    *)
    echo "OTHER CASES"
    ;;
esac
```

## function

function()
{

}
