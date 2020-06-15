# Head First Java
1. Chapter1
2. Chapter2
3. Chapter3
4. Chapter4
5. Chapter5
6. Chapter6
7. Chapter7
8. Chapter8
9. Chapter9
10. Chapter10
11. Chapter11
12. Chapter12
13. [Chapter13 运用Swing](#chapter13-运用swing)
14. Chapter14
15. Chapter15
## Chapter13 运用Swing


### 1.布局管理器——Layout Manager

布局管理器是个与特定组件相关联的Java对象，可以将被关联的对象看作一个面板，这个面板上加载有一些组件，而布局管理器控制着这些组件的位置与大小。按钮没有布局管理器。

>Swing组件(component)就是会被放在GUI(框架或者面板）上的东西，有Text Field、button、scrollable list、radio button等。所有的组件都继承自java.swing.JComponent。组件分为交互组件和背景组件，但是背景组件也可用于交互，二者的区分不是十分明显。  
组件是可以嵌套的。

### 2.三种布局管理器

不同的布局管理器有不同的组件安置策略（例如对齐网格线、大小一致、垂直堆放等）。有些布局管理器会采用组件的大小设置等信息，但是有些会忽略这些信息。

下面是常用的三种布局管理器：

#### 2.1 BoderLayout


