# git
git add . # 全部保存 .在linux 系统中表示本级目录 ..表示上级目录
# 部分add 
git add -p 
# s 切分开
# 尽量在一个提交里面只做一件事
# git diff --cached 比较stage和local repository
# git diff workspace 和 stage区
# 撤销 checkout 
# add以后要撤回 git reset 要撤销就再checkout
# commit 以后要回滚到上一版本 git reset -hard HEAD^ 指针会移动回上一个版本
# 以及push 以后要回滚 只能 git revert 这会创建一个新个commit
# glola
# git show 
# git reset --hard 954de520be2f
# git reflog 记录HEAD的变化
# git pull --rebase 手动解决conflict以后 git add 再用 git rebase continue
#  每天做的第一件事 是 git pull --rebase 
# push 之前再git pull --rebase

Ubuntu command line
=======
cp : copy testdir/testfile2   
mv testfie3  testdir/testfile3   
man ls  
ls --help  
ls | grep doc  
echo "hello world" | cat >> output.txt  
tail   
head  
alais showuser = 'echo $USER'  
ifconfig  
uname -aa  
blkid  
top  Windows的任务管理器
df disk free
lsusb 
apt-get  install/remove/update  
sudo shutdone 
Acronym vs abbreviation
Linux 
ls -lSrh # line sort reverse human readable
cp - r # recursive # 递归  
cp - n  no-clobber # 不被后来的替代  
cp - i  interactive  
su #  swtich user 默认切回root参数   
su -l # 连带环境一起切换



tlrd too long too read for help   
PATH="PATH:$PWD"   
when you assign value to variables this is no dollar sign  
when you use that variable, you need $sign  
note this is no breaks btween = and values when asign values  
#0 #1 # 2 # 3 #@ #*
#use double quots instead of single 
$(date "xxxxx") use $ to get the result of other command

# grep 行过滤  
grep -i 不区分大小写  
-v 反向选择  
-w 以单词匹配  
-o 打印匹配到的关键词  
-c 统计匹配到的次数  
-n 显示行号  
-r recursive 递归查找   
-A 前几行  
-B 后几行  
-C 前后几行  
-l 文件名  
-L 文件名反向选择  
-e 正则  
-E 扩展正则  
^key 以key开头  
key$ 以key结尾  
^$   匹配空行    
--color=auto 关键字显示颜色    

#  cut
cut -d' ' -2f xxxx 默认的分隔符为\t    
cut -c5-10    
cut -c5-     


# sort
sort -u unique  
sort -r reverse  
sort -o output  
sort -n number  
sort -n -t：-k3 以：分割的第3列按数字排序  

# echo

echo hello word | tee 1.txt  输出一份 存一份到文件  

#  unique
unique -i 忽略大小写  
unique -c 统计重复行次数 count  
unique -d 只显示重复行 duplicate  

# diff
diff -u file1 file2 第三种比较好用  
diff -q dir1 dir2 比较目录  

# 不同文件 打补丁     
diff -uN file1 file2 > file.patch    
patch file1 file.patch   
diff file1 file2     

# paste

paste file1 file2   行对行粘贴
paste -d: file1 file2   以：为分隔符行对行粘贴
paste -s file1 file2 串行 第一行全是file1的，第二行全是file2的 

# tr 字符的转换  
a-z或[:lower:]  [a-zA-Z0-9]
A-Z或[:upper:]  
0-9或[:digit:]  
[:alnum:] alpha + num  
[:alpha:] alpha  
[:blank:]  水平空白
[:punct:]  
[:space:]  
[:cntrl:]  

tr 'a-z' 'A-Z' <1.TXT 将小写变成大写  
tr '0-9' '@' <1.txt  
tr ':/' "#' <1.txt  w
tr -d 'a-z' <1.txt 删除’a-z‘  
tr -dc 'a-z' <1.txt 除了a-z的都删除 取反  
tr -s 将出现的重复字符压缩为1个  

# short cuts
^r 搜索历史命令
^a 光标移动到最前端
^e ....末端
^u 删除光标前所有
^k 删除光标后所有

# 通配符
>*0或多个任意字符  
？ 匹配任意的单个字符  
[]匹配list里的任意单个字符  
[！]匹配list里的任意单个字符 取反   
[1-13] 1-1|3  
{1..13} 1 到 13  

# shell
分类 :
/bin/sh
/bin/bash
/bin/dash

一个终端会打开一个shell

# 脚本的写法
#!/bin/bash or #!/bin/env bash
#Name Desc path usage update
chmod +x first_shell.sh 

bash -x first _shell.sh 打印一行，运行一行
bash -n first_shell.sh 检查是否有问题

# 变量名的规则
变量名严格区分大小写
A=123456
$A
${A} ${A:2:5} 从第三个字符开始截取5个字符
本地变量只针对当前进程生效

# read
read -p  "p;z input your name" name
read -n 5 -p "plz input <5"   限制输入长度
read -s -p 不显示输入
read -t  -n 限制输入时间 

从文件输入
read -n 5 -p "plz input <5" <1.txt

# declare 
-i 整数 
-r 只读变量  
-a array
-A   
-x declare -x AAA=123 = export AAA=123

#  环境变量
~/.bashrc 
争对当前进程有效，能被子进程调用  
env  查看环境变量    
set  查看环境变量 和 临时变量   

# 全局变量
/etc/bashrc bash info for all users   
/etc/profile 所有用户的全局环境变量  
$HOME/.bashrc 当前用户的bash信息 set alians umask function  
$HOME/.bash_profile env variables for current user, load when log in  
$HOME/.bash_logout load when log out  

# 系统变量

jobs  
sleep 500 &  后台进行 / ctrl a 后台挂起

# 四则运算
expr 1 + 1 记得加空格  
expr 10 \\*5  *要转义  
n=1; let n=n+1; echo $n  
let n+=2;  





