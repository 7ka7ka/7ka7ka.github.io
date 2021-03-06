### 1.命名空间(namespace)       

php的命名空间可以解决以下两类问题:         
1. 编写的代码与php内部的类/函数/常量或第三方类/函数/常量之间的名字冲突。       
2. 为很长的标识符名称(通常是为了缓解第一类问题而定义的)创建一个别名(或简短)的名称，提高源代码的可读性。         
  ----------摘自php官网的namespace的解释        
  
  通俗的来说就是为了防止类/函数/常量的命名冲突而设立的关键字，每一个命名空间都是一个独立的空间，不会与其他命名空间里的类/函数/常量相冲突         
  
  注意点：          
  1. namespace必须声明在所有代码的最前面         
```php
<?php
    namespace foo;
    class xx
    {
        
    
    }
 ?>>
 ```
 
### 2. use关键字       

1. use关键字的目的是调用目标路径的文件并为其设置一个昵称，并在该文件里的代码调用可以直接写这个昵称来调用目标文件         
```php
<?php
    namespace foo;
    use src\a\b as b;
    class xx
    {
        
    }
?>
```

有些时候会看见后面没有‘as b’这样的写法，其实这是一种简写，use省略as以及后面的别名而直接把路径的最后一个节点名字当作别名           
```php
<?php
    namespace foo;
    use src\a\b;
    class xx
    {
        
    }
?>
```
