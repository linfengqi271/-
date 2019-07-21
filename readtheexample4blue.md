#252行`STRATEGY4BLUE_API void RunStrategy(Environment *pEnv)`
调用了函数
1.Goalie（）265
2.Leftwing（）290
3.RightWing（）322
4.Center Defender（）354
5.CenterAttacker（）387
应该是用来调用策略（Strategy）的
# `Strategy4Blue.h`
##在`line:16  PLAYERS_PER_SIDE`一块
-定义了一些基础数据
-复制了'Referee.sln>>Referee.h>>line:35---line:91'
##包含了`Strategy4Blue.cpp`中函数的声明
# `dllmain.cpp`
复制了Referee中同名文件

#typedef `Environment`
定义在`Strategy4Blue.h line：52`
结构体
1.Bounds //边界（球及场地）
2.Robot
3.OpponentRobot //对方
4.Ball
包含了一些平台返回的比赛信息的内容的一个结构体
#问题
-enum什么意思？
-结构体
-`define REFEREE_API`
-`ifdef REFEREE_EXPORTS`

%readtheexample4blue

；2019/7/21 16:21:50

