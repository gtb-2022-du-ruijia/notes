# test

## file 
-e if file exists  

`[[ -e ./file1 ]]`  

`echo $?`

-f  exist and is a common file  

-d  if dir exists  

-L if link exist 

`ln -s file1 test1`  
`rm -f file1`
`[[ -L ./test1 ]]`  can not verify if the link has been removed  
`[[ ! -f ./file1 ]]` doesn't exist   

`[[ file1 -nt file2 ]]` new 
`[[ file1 -ot file2 ]]` old
`[[ file1 -ef file2 ]]` equal/ hard link / have same inode 

## number 
-eq -nq -gt -lt -ge -le   
equal not equal greater then less than  >= <=

## string 
-z if null  
`[[ -z "hello world "]]`  
-n if not null    
string1 = stirng2  if equal  
`[[ "hello" = "world" ]]`  
string1 !=stinrg2  if not equal  



