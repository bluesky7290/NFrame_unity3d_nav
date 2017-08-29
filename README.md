# NFrame_unity3d_nav
# 1.	打开目录NFrame_unity3d_nav\source\build\unity下的cai-navigation-u3d.sln解决方案。
# 2.	打开后编译是编译不过的，有的项目需要依赖UnityEditor.dll，UnityEngine.dll这2个库，依赖配置好后就可以成功编译，编译成功后所有需要的dll都在NFrame_unity3d_nav\source\build\unity\bin\Release下
# 3.	拷贝对应的dll到需要生成导航数据的unity项目的CAI和Plugins下，如图
# CAI下
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/cai.png)
# Plugins下
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/plugins.png)
NFrame_unity3d_nav\unity5.3是5.3的版本，如果是5.3版本直接拷贝到unity项目的Assets下，其他版本需要自行编译，目录和文件结构可以参考unity5.3下的文件结构
# 4.	上述都准备好以后，打开unity项目，就可以生成导航数据了，使用方法参考
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/4.png)
在游戏项目菜单中选择（CritterAI->Create NMGen Assets->Navmesh Build : Standard）初始化，初始化完毕后
项目目录中将出现几个文件，他们如下:  
	CAIBakedNavmesh.asset＜/br＞  
	MeshCompiler.asset＜/br＞  
	NavmeshBuild.asset  
