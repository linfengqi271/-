# SimuroSot-Middle
This is the source code of FIRA SimuroSot Middle League new platform.

1. Referee 
This is the computer referee module for judging the ongoing situations.
*判断当前情况的电脑裁判模块*

2. Strategy4Blue 
This is a template for developing Strategy4Blue, which holds all the needed files.
*开发蓝队策略的模板，有所有必须的文件*
3. Strategy4Yellow 
This is a template for developing Strategy4Yellow, which holds all the needed files.
*
4. Team1
This is the automatic referee and strategy agency of blue team for FIRA MiroSot/SimuroSot.
*蓝队的裁判和策略自动代理*
5. Team2
This is the automatic referee and strategy agency of yellow team for FIRA MiroSot/SimuroSot.



5.1 SetFormerRobots(PlayMode gameState, Robot robots[])
该函数在代理裁判需要拿到先摆方的球员位置数据时被调用，该函数会通过
参数gameState提供判罚系统的判罚结果，策略程序需要根据判罚结果（即开球、
争球、点球、门球）设置本方的五名球员的位置和朝向数据到robots数组。最终，
仿真平台根据robots数据自动摆放本方机器人。
5.2 SetLaterRobots(PlayMode gameState, Robot formerRobots[], 
Vector3D ball, Robot laterRobots[])
该函数在代理裁判需要拿到后摆方的球员位置数据时被调用，该函数会通过
参数gameState提供判罚系统的判罚结果，formaerRobots提供先摆方的球员位置
数据，ball提供球的位置数据，然后根据这些信息设置本方想要摆放的五名球员
的位置和朝向数据到laterRobots数组。最终，仿真平台根据laterRobots数据自动
摆放本方机器人。
5.3 SetBall(PlayMode gameState, Vector3D * pBall)
该函数在代理裁判需要拿到开门球方队伍想要摆放的球的位置数据时被调
用，该函数设置想要摆放的球的位置数据到pBall。最终，仿真平台根据pBall数
据自动摆放开门球方的门球位置。
5.4 RunStrategy(Environment *pEnv)
该函数在代理裁判模块确认当前周期场上没有任何判罚（开球、争球、门球、
点球等）产生时被调用，该函数提供当前仿真环境赛场数据pEnv，策略程序根据
赛场数据做出决策，设定相应的策略控制命令至pEnv（机器人控制命令）。
5.5 SetBlueTeamName(char* teamName)/ SetYellowTeamName(char* teamName)
该函数在代理裁判模块一开始比赛是调用，通过该函数来设定比赛的蓝队或
者黄队队伍名称。仿真平台根据此设定将队伍名称显示到平台控制部件的队伍名
称处，如果在仿真平台的控制部件处没有显示自己队伍的名字，说明自己的策略
没有正确连接到仿真平台。
%note

；2019/7/21 15:40:44

