# seq

用来生成序列

```
NAME
       seq - print a sequence of numbers

SYNOPSIS
       seq [OPTION]... LAST
       seq [OPTION]... FIRST LAST
       seq [OPTION]... FIRST INCREMENT LAST
```



## 1、生成数据序列，正序，倒序，跳跃

正序 seq -w 2  5，默认步长为1

```
[postgres@wh-db-2 11:46:06 /home/postgres]
$seq -w 2  5
2
3
4
5
```

正序seq -w  1  2  10，调整步长为2

```
$seq -w 1 2 10
01
03
05
07
09
```

倒序方式， seq -w  10 -1 1

```
[postgres@wh-db-2 11:50:18 /home/postgres]
$seq -w  10 -1 1
10
09
08
07
06
05
04
03
02
01
```



## 2、-f选项指定格式

seq -f '%03g' 1 10, 其中的%03g标识宽度为3，不足采用0补充

```
[postgres@wh-db-2 11:52:26 /home/postgres]
$seq -f '%03g' 1 10
001
002
003
004
005
006
007
008
009
010
```

## 3、-s 可以指定分隔符

```
[postgres@wh-db-2 11:52:29 /home/postgres]
$seq -s ',' 1 10
1,2,3,4,5,6,7,8,9,10

[postgres@wh-db-2 11:54:14 /home/postgres]
$seq -s ' ' 1 10
1 2 3 4 5 6 7 8 9 10
```



