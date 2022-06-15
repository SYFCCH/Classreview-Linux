Shell程序就是包含一系列的linux命令和控制语句而已     

<https://blog.csdn.net/weixin_49343190/article/details/120983328>   

<https://blog.csdn.net/qq_36154886/article/details/94982168>    

# 习题  
1. 统计1-100的和     
![img_91.png](img_91.png)     

----


2.   
![img_92.png](img_92.png)     

3.      
![img_93.png](img_93.png)



4. 
    







# 实验的五题  
1. ![img_107.png](img_107.png)      

注意`` 和 '' 的区别
```shell
#!/bin/bash
if[ `id -u` -eq 0 ]
then 
  PS1='#'
else 
  PS1='$'
fi 
```

2.![img_108.png](img_108.png)    
```shell
#!/bin/bash 
file=/usr/local/123
if test -d $file
then
  cd $file
elif [ -f $file ]
then  
  rm $file
else
  mkdir $file
fi
```     

3.![img_109.png](img_109.png)    
```shell
#!/bin/bash   
case $1 in 
         [0-9]) echo "digital";;
         [a-z]) echo "lower char";;
         [A-Z]) echo "upper char";;
         "Good") echo "OK";;
         *) echo "other";;
esac  
```

4.![img_110.png](img_110.png)    
```shell
#!/bin/bash
for file in * 
do
  [ -f $file ] && mv $file $file.old
  [ -d $file ] && break
done
```


5.![img_111.png](img_111.png)    
```shell
#!/bin/bash 
total=1
for (( i=1; i<10; i++)) 
do
  [ $[ $i % 2] -eq  0 ] && continue
  total=$[$total * $i]
done
  echo $total
```

1. ![img_113.png](img_113.png)   
```shell
#!/bin/bash 
user=user
for i in {1..20} 
do 
  name="${user}${i}"
  useradd $name
done   
```


2. ![img_114.png](img_114.png)   
```shell 
#!/bin/bash
filename=$(ls -l /home | grep "^user" | awk '{print $9}')
for file in filename 
do
userdel -rf $file 
done  
```

3. ![img_115.png](img_115.png)   
```shell
#!/bin/bash
dir=$1
if [ -d $dir] 
then
  cd $dir
  for file in * 
  do
    if [-f $file] 
    then echo ${}

```




4. ![img_116.png](img_116.png)   
```shell


```


5. ![img_117.png](img_117.png)  
```shell

```


6. ![img_118.png](img_118.png)   
```shell




```