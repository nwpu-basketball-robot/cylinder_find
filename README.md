## cylinder_find
#robot use which to find cylinder(opencv and laser)
#1.Cylinder_find 是用opencv识别一个蓝绿色的圆柱，返回角度；

#2.leg_detector 是用激光扫描类似于腿的物体，其中有一个分类器（参考机器学习相关知识），还有半径过滤等条件，返回数据是物体的角度和距离；

#3.思路是将两个角度进行匹配，如果两个角度相同，则认为这是圆柱，则认为激光返回的距离就是圆柱的距离

#4.目前的思路是两个程序分别返回数据，在状态机中进行数据的选择匹配。

#5.还可以把两个工程直接合成一个 ，但是要注意使用命名空间（std；cv）可能会造成冲突,注意消除冲突

#5.leg_detector这个工程的运行方法是先安装激光驱动，和一些依赖，然后用打开激光，最后用roslaunch运行leg_detector.launch

#6.注意事项：1.记得给激光加权限
	    2.使用之前先学习http://wiki.ros.org/hokuyo_node/Tutorials/UsingTheHokuyoNode
	    3.有问题参考http://wiki.ros.org/hokuyo_node/Troubleshooting
