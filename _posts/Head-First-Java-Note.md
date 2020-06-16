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
这个管理器会把背景组件分割成5个区域（东南西北中）。每个区域只能放一个组件，该布局管理器通常不会让组件取得默认大小。这是框架（Frame）默认的布局管理器。
>放置在BorderLayout关联的背景组件的东西区域的组件的高度会强制限制成该管理器关联的背景组件高度，宽度不得超过背景组件宽度，超过则被限制为固定值。；放置在南北区域的组件的宽度会限制为背景组件的宽度，高度不得超过背景组件高度，超过则被限制为固定值。

* 使用示例

```java
package chap13;
import javax.swing.*;
import java.awt.*;//BorderLayout布局管理器所在的包

public class BorderlayoutExample {
    public static void main (String [] args){
        BorderlayoutExample gui = new BorderlayoutExample();
        gui.go();
    }

    public void go(){
        JFrame frame = new JFrame();

        JButton east = new JButton("east");
        JButton west = new JButton("west");
        JButton north = new JButton("north");
        JButton south = new JButton("south");
        JButton center = new JButton("center");

        frame.getContentPane().add(BorderLayout.EAST,east);
        frame.getContentPane().add(BorderLayout.WEST,west);
        frame.getContentPane().add(BorderLayout.NORTH,north);
        frame.getContentPane().add(BorderLayout.SOUTH,south);
        frame.getContentPane().add(BorderLayout.CENTER,center);

        frame.setSize(300,300);
        frame.setVisible(true);
    }

}
```
![](/styles/images/Chapter13/BorderLayout.png.jpg)







