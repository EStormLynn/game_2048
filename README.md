# C语言2048小游戏
## 涉及内容
* 屏幕绘制库`ncurese`的使用

ncurese库安装
`$ sudo apt-get install libncurses5-dev`

## 获取代码
```sh
$ git clone 
$ gcc game_2048.c -o 2048 -lcurses
$ ./2048
```

## 环境说明
* Linux Ubuntu
* Vim

## 效果图
![](http://oo8jzybo8.bkt.clouddn.com/2048.gif)

## 设计思路
2048游戏中关键的是消掉方块和在屏幕上输出数据，后者可以通过ncurses库实现。
2048的2个关键点：
* 1.满足条件消掉方块
* 2.移动方块，触发消掉或者移动数据

大体思路维护和地图相同大小的数组矩阵，玩家操作，改变数组数据，并绘制出来。

## 函数说明
```c
void draw();  // 用于绘制游戏界面
void play();  // 游戏运行的逻辑主体
void init();  // 初始化函数，用于完成一些必要的初始化操作
void draw_one(int y, int x);  // 绘制单个数字
void cnt_value(int *new_y, int *new_x);  // 
int game_over();  // 结束游戏
int cnt_one(int y, int x);  
```