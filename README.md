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
CAIBakedNavmesh.asset  
MeshCompiler.asset  
NavmeshBuild.asset  
# 5 . 添加一个能生成地形寻路网格的Compiler，（CritterAI->Create NMGen Assets->Compiler : Terrain）
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/5.1.png)
我们还需要将我们之前创建的地形绑定到TerrainCompiler上。
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/5.2.png)
将TerrainCompiler绑定到NavmeshBuild上。
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/5.3.png)
# 6.	开始生成导航数据(生成过程中如果unity闪退，点击NavmeshBuild的Derive按钮，在生成应该就可以生成了)
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/6.1.png)
效果预览
![image](https://github.com/bluesky7290/NFrame_unity3d_nav/blob/master/Images/6.2.png)
# 7.  导出为文件，此时会出现2个文件，其中“srv_”开头的文件用于服务端寻路。拷贝到服务端\NFDataCfg\Ini\Navigation目录下，并且在Scene的excel配置下即可，至于怎么使用https://github.com/ketoo/NoahGameFrame的Tutorial6有详细教程。
# 8.  其他高级功能自己去玩吧
