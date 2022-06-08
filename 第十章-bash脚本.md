Shell程序就是包含一系列的linux命令和控制语句而已     


开头的#!/bin/bash表示这是注释行程序体   

程序体分为顺序结构，分支结构，循环结构  

顺序结构：   
分支结构： if else  fi   case  esac    
比如判断a和b是否相等    
```shell
#!/bin/bash
read a
read b
if (( $a == $b ))
then
    echo "a和b相等"
fi
```


循环结构： while...  for...   do...util   
 

注释程序体：   
```shell
#!/bin/bash    
cd /tmp 
rm -rf 1*a.txt .u*
echo "Whell Done!"   
```     


# 变量   
1. 普通变量
无类型、直接赋值   
$i  或者 ${i}   
2. 数组变量  
一维的:   系统变量名=(元素1元素2元素3...)

3. 特殊变量  