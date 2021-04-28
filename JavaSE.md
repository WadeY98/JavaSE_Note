# JavaSE

## 一、Dos命令

| 切换盘符                    | 盘符：                   |
| --------------------------- | ------------------------ |
| **切换当前盘符下某个目录:** | **cd 文件夹路径名**      |
| **返回上一级目录：**        | **cd..**                 |
| **返回根目录**：            | cd\                      |
| 查看目录：                  | dir 目录名（文件夹）     |
| 创建目录(文件夹)的命令:     | md 目录名                |
| 创建空文件:                 | type nul>文件名          |
| 创建不为空文件:             | echo 内容>文件名         |
| 删除空目录的命令:           | rd 目录                  |
| 删除文件:                   | del 路径名+文件名        |
| 复制：                      | copy 源文件路径 目标路径 |
| 清屏                        | cls                      |
| 退出dos系统                 | exit                     |

- 用javac命令编译java源生成.class文件(又名字节码文件):cmd->进入dos系统->进入java源文件所在文件夹中->输入 javac java源文件名.java->回车.
- 用java命令运行.class文件(又名字节码文件),结果输出内容:在上一步基础上直接输入命令java 字节码文件名->回车



## 二、Java概念

### 2.1 程序是什么？

- 为了模拟现实世界，解决现实问题而编写的一系列有序指令集合。



### 2.2 Java概述

- java是一种跨平台的,面向对象的,强类型的,编译解释型的语言。

- java优点:
  - 简单(有自动垃圾回收机制,有自动类型检查机制)
  - 跨平台(java程序可以在多个系统上运行)
  - 面向对象(贴合人类思维方式)
  - 安全性高(有强大自动类型检查机制)



### 2.3 Java执行机制

- 编译执行机制

  - 将源文件编译成平台可识别机器码文件执行.eg:c,c++

  - 特点:执行效率高,不可跨平台。



- 解释执行机制:
  - 将源文件交给不同平台独有解释器解释执行。
  - 特点:可以跨平台,执行效率低



- 编译解释机制
  - 将源文件先编译成平台中间文件(.class文件或字节码文件),然后再将中间文件交给不同平台jvm云解释执行
  - 优点:跨平台



### 2.4 Java体系:三大体系.
- JavaSE:java平台标准版,java核心语法.用来作面向桌面应用程序.
- JavaEE:java平台企业版,java企业级开发.用来作面向internet应用程序.
- JavaME:java平台微型版 ,嵌入式或移动手机端开发.用来作机顶盒或手机移动端开发.



###  2.5 Java应用

- 作面向桌面应用程序.
- 面向internet应用程序.
- 用来作机顶盒,或手机移动端开发.
- 为大型企业提供解决方案.
- 学习大数据基础.



### 2.6 Java的语言规范(java代码规范)

- java严格区分大小写.
- java只认英文标点符号.
- 代码要有层次缩进,里面的结构相对外面结果缩进一个tab键(一个制表符位置,即8个空格);
- 每个结构的大括号,开始的大括号在这一结构结尾,结束的大括号独占一行且与这一结构开头字母对齐.
- 一行只写一条语句,每条语句以分号结束.
- 用public修饰的类框架必须java源文件名同名,没用public修饰的类框架可以不与java源文件名同名(无特殊情况,类名要用public).一个java源文件中可以写多个类架构,最多只能有一个用public修饰.(无特殊情况,一个java源文件里面只写一个类框架)
- 一个类框架中最多只能有一个main方法(程序的入口方法);
- 一个类框架生成一个字节码文件.



### 2.7 Java运行原理

- java程序是在内存中运行的.
- Jdk的组成:编译器,jvm,jre等.
- jvm作用:跨平台(不同平台有不同jvm),自动垃圾回收机制.



## 三、Java基本语法



### 3.1 标识符

 标识符:自定义名称叫标识符

- 标识符由字母,数字,下划线,$组成.
- 标识符只能以字母,下划线,$开头.
- 标识符可以包含数字,但是不能以数字开头.
- 标识符除了_,$以外,不能包含任何特殊字符.
- 标识符要见名知义.
- 标识符不能用java中关键字.
  	帕斯卡命名法:标识符由一到多个单词组成,每个单词首字母大写,其他字母小写.
  	类名采用帕斯卡命名法.eg:HelloWorld
  	驼峰式命名法:标识符由一到多个单词组成,第一个单词首字母小写,其他单词首字母大写,其他字母小写.变量名和方法名采用驼峰式命   名法.eg:helloWorld



### 3.2 关键字

关键字：被Java赋予特定含义的单词.



### 3.3 变量

变量:在计算机内存中开辟一块空间存数据叫变量.

- 变量的组成:变量名,变量数据类型,变量值.
- 变量名自定义,采用驼峰式命名法.
- 变量必须先声明,再赋值,最后才能使用.
- =：赋值号,将等于号右边的值赋给左边.
- 变量声明和赋值的语法:
  - 先声明变量,再给变量赋值.
  -  声明变量的语法: 数据类型 变量名;
  -  给变量赋值的语法: 变量名=值;

```java
//声明变量
String name;
//给变量赋值
name="张三";

```

- 声明变量的同时给变量赋值的语法:数据类型 变量名=值;

  ```java
  public class Variable { 
      public static void main(String[] args){ 
          //定义字节型变量 
          byte b = 100; 
          System.out.println(b); 
          //定义短整型变量 
          short s = 1000; 
          System.out.println(s);
          //定义整型变量 
          int i = 123456; 
          System.out.println(i); 
          //定义长整型变量 
          long l = 12345678900L; 
          System.out.println(l); 
          //定义单精度浮点型变量 
          float f = 5.5F; 
          System.out.println(f); 
          //定义双精度浮点型变量 
          double d = 8.5; 
          System.out.println(d); 
          //定义布尔型变量 
          boolean bool = false; 
          System.out.println(bool); 
          //定义字符型变量 
          char c = 'A'; 
          System.out.println(c); 
      } 
  }
  
  ```

  >long类型：建议数据后加L表示。 
  >
  >float类型：建议数据后加F表示。 

  

- 同时声明多个相同类型的变量,给部分变量赋值:数据类型 变量名1,变量名2=值,变量名3;

  ```java
  int girlFriendAge1,girlFriendAge2=18,girlFriendAge3,girlFriendAge4;
  ```

- 变量分类

  - 按数据类型分
    - 基本数据类型的变量:变量的数据类型是基本数据类型.
    - 引用数据类型的变量:变量的数据类型是引用数据类型.

  - 按变量声明位置分
    - 局部变量:在方法中声明的变量叫局部变量,局部变量的作用范围仅在声明它的大括号中有用.局部变量不赋值就没有值.
    - 成员变量:在类中方法外面声明的变量叫成员变量,成员变量的作用范围有修饰符决定.成员变量不赋值,系统会默认给它分配一个初值.

- 在同一个作用范围内,不能声明相同的变量名.

### 3.4 常量

- 常量:常量一生只赋一次值,赋值后不可更改.常量名全大写.

| **类型**   | 含义                                   | **数据举例**                |
| ---------- | -------------------------------------- | --------------------------- |
| 整数常量   | 所有的整数                             | 0，1， 567， -9             |
| 小数常量   | 所有的小数                             | 0.0， -0.1， 2.55           |
| 字符常量   | 单引号引起来,只能写一个字符,必须有内容 | 'a' ， ' '， '好'           |
| 字符串常量 | 双引号引起来,可以写多个字符,也可以不写 | "A" ，"Hello" ，"你好" ，"" |
| 布尔常量   | 只有两个值                             | true ， false               |
| 空常量     | 只有一个值                             | null                        |

- 输出各种类型的常量。

```java
public class ConstantDemo { 
    public static void main(String[] args){ 
        //输出整数常量 
        System.out.println(123); 
        //输出小数常量 
        System.out.println(0.125); 
        //输出字符常量 
        System.out.println('A'); 
        //输出布尔常量 
        System.out.println(true); 
        //输出字符串常量 
        System.out.println("你好Java"); 
    }
```



### 3.5 数据类型

**Java的数据类型分为两大类：** 

- **基本数据类型**：包括 整数 、 浮点数 、 字符 、 布尔 。 

- **引用数据类型**：包括 String、数组、类、接口。

四类八种基本数据类型： 

| **数据类型** | 关键字         | **内存占用** | **取值范围**           |
| ------------ | -------------- | ------------ | ---------------------- |
| 字节型       | byte           | 1个字节      | -128~127               |
| 短整型       | short          | 2个字节      | -32768~32767           |
| 整型         | int（默认）    | 4个字节      | -2的31次方~2的31次方-1 |
| 长整型       | long           | 8个字节      | -2的63次方~2的63次方-1 |
| 单精度浮点数 | float          | 4个字节      | 1.4013E-45~3.4028E+38  |
| 双精度浮点数 | double（默认） | 8个字节      | 4.9E-324~1.7977E+308   |
| 字符型       | char           | 2个字节      | 0-65535                |
| 布尔类型     | boolean        | 1个字节      | true，false            |

>Java中的默认类型：整数类型是 int 、浮点类型是 double 。 



### 3.6 转义字符

- 转义字符:所有转义字符必须全定在""中

![image-20210414164838352](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210414164838352.png)

### 3.7 **数据类型转换**

Java程序中要求参与的计算的数据，必须要保证数据类型的一致性，如果数据类型不一致将发生类型的转换。 

#### 3.7.1 **自动转换**

- **自动转换**：将 `取值范围小的类型` 自动提升为 `取值范围大的类型` 。

```java
public static void main(String[] args) { 
    int i = 1; 
    byte b = 2; 
    // byte x = b + i; // 报错 
    //int类型和byte类型运算，结果是int类型 
    int j = b + i; 
    System.out.println(j);
}
```

- **转换原理图解** :
  - byte 类型内存占有1个字节，在和 int 类型运算时会提升为 int 类型 ，自动补充3个字节，因此计算后的结果还是 int 类 型。

![image-20210331151319453](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210331151319453.png)

同样道理，当一个 int 类型变量和一个 double 变量运算时， int 类型将会自动提升为 double 类型进行运算。 

```java
public static void main(String[] args) { 
    int i = 1; 
    double d = 2.5; 
    //int类型和double类型运算，结果是double类型 
    //int类型会提升为double类型 
    double e = d+i; 
    System.out.println(e); 
}
```

- **转换规则**

范围小的类型向范围大的类型提升， byte、short、char 运算时直接提升为 int 。 

```java
byte、short、char‐‐>int‐‐>long‐‐>float‐‐>double
```



#### 3.7.2 强制类型转换

- 1、特点：代码需要进行特殊的格式处理，不能自动完成。

- 2、格式：范围小的类型，范围小的变量名 = （范围小的类型）原本范围大的数据。

代码演示：

```java
public class DataType {
    public static void main(String[] args) {
        //左边是int类型，右边是long类型，不一样
        //long --> int，不是从小到大
        //不能发生自动类型转换！
        //格式：范围小的类型，范围小的变量名 = （范围小的类型）原本范围大的数据；
        int num = (int)100L;
        System.out.println(num);

        //long强制转换为int类型
        int num2 = (int) 6000000000L;
        System.out.println(num2); //1705032704

        //double --> int 强制类型转换
        int num3 = (int)3.99;
        System.out.println(num3);//3 //这并不是四舍五入，所有的小数位都会被舍弃掉

        char zifu1 = 'A';//这是一个字符型变量，里面是大写字母A
        System.out.println(zifu1+1);//66 //一旦char类型进行了数学运算，那么字符就好按照一定的规则翻译成为一个数字

        byte num4 = 40;//注意！右侧的数值大小不能超过左侧的类型范围
        byte num5 = 50;
        //byte + byte -->int + int -->int
        int result1 = num4 + num5;
        System.out.println(result1);//90

        short num6 = 60;
        //int强制转换为short：注意必须保证逻辑上真实大小本来就没有超过short范围，否则会发生数据溢出
        short result2 = (short)(num4 + num6);
        System.out.println(result2);//100

    }
}

```

> 注意事项：
>
> 1、强制类型转换一般不推荐使用，因为有可能发生精度损失、数据溢出。
>
> 2、byte/short/char这三种类型都可以发生数学运算，例如加法“+”。
>
> 3、byte/short/char这三种类型在运算的时候，都会被首先提升成为int类型，然后再计算。
>
> 4、boolean类型不能发生数据类型转换。



#### 3.7.3 ASCll编码表

![image-20210331191317058](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210331191317058.png)



### 3.8 运算符

#### 3.8.1 算数运算符

| **算数运算符包括：** |                              |
| -------------------- | ---------------------------- |
| +                    | 加法运算，字符串连接运算     |
| -                    | 减法运算                     |
| *                    | 乘法运算                     |
| /                    | 除法运算                     |
| %                    | 取模运算，两个数字相除取余数 |
| ++、--               | 自增自减运算                 |

- 除法运算与取模运算：

```java
public class quMo {
    public static void main(String[] args) {
        System.out.println(chuFa(10,3));//3
        System.out.println(printMo(10,3)); //1
    }

    //除法运算
    public static int chuFa(int a,int b){
        int result = a / b;
        return result;
    }

    //取模运算
    public static int printMo(int a ,int b){
        int result = a % b;
        return result;
    }
}
```

> 除法运算得到的值是商，而取模运算得到值的是余数



- 自增与自减

  - ++ **运算，变量自己增长**1。反之， -- 运算，变量自己减少1，用法与 ++ 一致
  - 独立运算：
    - 变量在独立运算时， 前++ 和 后++ 没有区别 。 
    - 变量 前++ ：例如 ++i 。 
    - 变量 后++ ：例如 i++ 。 

  - 混合运算： 

    - 和其他变量放在一起， 前++ 和 后++ 就产生了不同。 
    - 变量 前++ ：变量a自己加1，将加1后的结果赋值给b，也就是说a先计算。a和b的结果都是2。

    ```java
    public class zizhengyuzijian {
        public static void main(String[] args) {
            int a = 1;
            int b = ++a;
            System.out.println(a);//2
            System.out.println(b);//2
        }
    }
    
    ```

    - 变量 后++ ：变量a先把自己的值1，赋值给变量b，此时变量b的值就是1，变量a自己再加1。a的结果是2，b 

      的结果是1。 

      ```java
      public class zizhengyuzijian {
          public static void main(String[] args) {
              int a = 1;
              int b = a++;
              System.out.println(a);//2
              System.out.println(b);//1
          }
      }
      ```

- \+ 符号在字符串中的操作： 

  + 符号在遇到字符串的时候，表示**连接、拼接**的含义。 

  - "a"+"b"的结果是“ab”，连接含义 

  ```java
  public static void main(String[] args){ 
      System.out.println("5+5="+5+5);//输出5+5=55 
  }
  ```



#### 3.8.2 **赋值运算符** 

| **赋值运算符包括：** |          |
| -------------------- | -------- |
| =                    | 等于号   |
| +=                   | 加等于   |
| -=                   | 减等于   |
| *=                   | 乘等于   |
| /=                   | 除等于   |
| %=                   | 取模等于 |

> 赋值运算符，就是将符号右边的值，赋给左边的变量。

```java
public static void main(String[] args){ 
    int i = 5; 
    i+=5;//计算方式 i=i+5 变量i先加5，再赋值变量i 
    System.out.println(i); //输出结果是10 
}
```



#### 3.8.3  **比较运算符**

| **比较运算符包括：** |                                                              |
| -------------------- | ------------------------------------------------------------ |
| ==                   | 比较符号两边数据是否相等，相等结果是true。                   |
| <                    | 比较符号左边的数据是否小于右边的数据，如果小于结果是true。   |
| >                    | 比较符号左边的数据是否大于右边的数据，如果大于结果是true。   |
| <=                   | 比较符号左边的数据是否小于或者等于右边的数据，如果小于结果是true。 |
| >=                   | 比较符号左边的数据是否大于或者等于右边的数据，如果小于结果是true。 |
| !=                   | 不等于符号 ，如果符号两边的数据不相等，结果是true。          |

- 比较运算符，是两个数据之间进行比较的运算，运算结果都是布尔值 true或者 false 。

```java
public static void main(String[] args) { 
    System.out.println(1==1);//true 
    System.out.println(1<2);//true 
    System.out.println(3>4);//false 
    System.out.println(3<=4);//true 
    System.out.println(3>=4);//false 
    System.out.println(3!=4);//true 
}
```



#### 3.8.4  **逻辑运算符**

| **逻辑运算符包括：** |                                                              |
| -------------------- | ------------------------------------------------------------ |
| && : 短路与          | 1、两边都是true，结果是true   2、一边是false，结果是false  3、短路特点：符号左边是false，右边就不再计算 |
| \|\|: 短路或         | 1、两边都是false，结果是false  2、一边是true，结果是true  3、短路特点：符号左边是true，右边不再计算 |
| ！：取反             | 1、！true的结果是false  2、！false的结果是true               |

- 逻辑运算符，是用来连接两个布尔类型结果的运算符，运算结果都是布尔值 true 或者 false

```java
public static void main(String[] args) { 
    System.out.println(true && true);//true 
    System.out.println(true && false);//false 
    System.out.println(false && true);//false，右边不计算 
    System.out.println(false || false);//falase 
    System.out.println(false || true);//true 
    System.out.println(true || false);//true，右边不计算 
    System.out.println(!false);//true 
}
```



#### 3.8.5 **三元运算符**

- 三元运算符格式： 

```java
数据类型 变量名 = 布尔类型表达式？结果1：结果2
```

- 三元运算符计算方式： 

  - 布尔类型表达式结果是true，三元运算符整体结果为结果1，赋值给变量。 

  - 布尔类型表达式结果是false，三元运算符整体结果为结果2，赋值给变量。

```java
public static void main(String[] args) { 
    int i = (1==2 ? 100 : 200); 
    System.out.println(i);//200 
    int j = (3<=4 ? 500 : 600); 
    System.out.println(j);//500 
}
```



### 3.9 Scanner

控制台输入(从键盘上接收数据):三步

- 1、导包

  import java.util.Scanner; 

- 获得具有从键盘上接收数据的能力
  Scanner input=new Scanner(System.in);

- 接收数据

  - 注意:不能直接从键盘上接收char类型的数据.想接收单个字符可以用String接收.
  - 接收int类型:input.nextInt();
  - 接收double类型:input.nextDouble();
  - 接收String类型:input.next();

- 代码演示：

  ```java
  public class ScannerTest1{
  	
  	/**
  	*程序入口方法
  	*/
  	public static void main(String[] args){
  		//第二步:获得具有从键盘上接收数据的能力
  		Scanner input=new Scanner(System.in);
  		
  		System.out.println("请输入你的年龄:");
  		//将从键盘上接收的整数存在变量中
  		int age=input.nextInt();
  		
  		System.out.println("请输入你的身高(米):");
  		//将从键盘上接收的小数存在变量中
  		double height=input.nextDouble();
  		
  		System.out.println("请输入你的姓名:");
  		//将从键盘上接收的String类型的数据存在变量中
  		String name=input.next();
  		
  		System.out.println("请输入你的性别:");
  		//将从键盘上接收的String类型的数据存在变量中
  		String sex=input.next();
  		
  		System.out.println("年龄为:"+age+",身高为:"+height+",姓名为:"+name+",性别:"+sex);
  	}
  }
  
  ```

  

## 四、流程控制

### 4.1 顺序结构

```java
public static void main(String[] args){ 
    //顺序执行，根据编写的顺序，从上到下运行 
    System.out.println(1); 
    System.out.println(2); 
    System.out.println(3); 
}
```

### 4.2 **判断语句**1--if

- **if**语句第一种格式： if

  ```java
  if(关系表达式)｛ 
      语句体; 
  ｝
  ```


- 执行流程

  - 首先判断关系表达式看其结果是true还是false 
  - 如果是true就执行语句体 
  - 如果是false就不执行语句体

- 代码演示：

  ```java
  public class IfPrint {
      public static void main(String[] args) {
          System.out.println("开始");
          //定义两个变量
          int a = 10;
          int b = 20;
          //变量使用if判断
          if(a == b){
              System.out.println("a等于b");
          }
          int c = 10;
          if (a == c){
              System.out.println("a等于c");
          }
          System.out.println("结束");
      }
  }
  
  ```



### 4.3 **判断语句**2--if...else

- **if****语句第二种格式：** if...else 

```java
if(关系表达式) { 
    语句体1; 
}else { 
    语句体2; 
}
```

- 执行流程
  - 首先判断关系表达式看其结果是true还是false 
  - 如果是true就执行语句体1 
  - 如果是false就执行语句体2

- 代码演示：

```java
public class IfElsePrint {
    public static void main(String[] args) {
        System.out.println("开始");
        //定义两个变量
        int a = 10;
        int b = 20;
        //变量使用if判断
        if (a > b){
            System.out.println("a大于b");
        }else{
            System.out.println("a小于b");
        }
        System.out.println("结束");
    }
}
```



### 4.4 **判断语句**3--if..else if...else

- **if**语句第三种格式：if...else if ...else

```java
if (判断条件1) { 
    执行语句1; 
} else if (判断条件2) { 
    执行语句2; 
}
... 
}else if (判断条件n) { 
    执行语句n; 
} else { 
    执行语句n+1; 
}
```

- **执行流程**
  - 首先判断关系表达式1看其结果是true还是false 
  - 如果是true就执行语句体1 
  - 如果是false就继续判断关系表达式2看其结果是true还是false 
  - 如果是true就执行语句体2 
  - 如果是false就继续判断关系表达式…看其结果是true还是false 
  - …
  - 如果没有任何关系表达式为true，就执行语句体n+1。

- 代码演示：

```java
public class IfElseifElsePrint {
    public static void main(String[] args) {
        // x和y的关系满足如下：
        // x>=3 y = 2x + 1;
        // ‐1<=x<3 y = 2x;
        // x<=‐1 y = 2x – 1;
        // 根据给定的x的值，计算出y的值并输出。
        // 定义变量
        int x = 5;
        int y;
        if (x >= 3){
            y = 2*x+1;
        }else if (x >= -1 && x < 3){
            y = 2*x;
        }else {
            y = 2*x-1;
        }
        System.out.println("y的值是："+y);
    }
}
```

### 4.5 **if**语句和三元运算符的互换

在某些简单的应用中，if语句是可以和三元运算符互换使用的。 

```java
public static void main(String[] args) { 
    int a = 10; 
    int b = 20; 
    //定义变量，保存a和b的较大值 
    int c; 
    if(a > b) { 
        c = a; 
    } else { 
        c = b; 
    }
    //可以上述功能改写为三元运算符形式 
    c = a > b ? a:b; 
}
```

### 4.5 选择语句--switch

- **switch**语句格式：

  ```java
  switch(表达式) { 
      case 常量值1: 
          语句体1; 
          break; 
      case 常量值2: 
          语句体2; 
          break; 
          ... 
          default: 
          语句体n+1; 
          break; 
  }
  ```

- 图解

![image-20210401212624081](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210401212624081.png)

- **执行流程**

  - 首先计算出表达式的值 

  - 其次，和case依次比较，一旦有对应的值，就会执行相应的语句，在执行的过程中，遇到break就会结束。

  - 最后，如果所有的case都和表达式的值不匹配，就会执行default语句体部分，然后程序结束掉。



- 代码演示：

```java
public static void main(String[] args) { 
	//定义变量，判断是星期几 
    int weekday = 6; 
    //switch语句实现选择 
    switch(weekday) { 
        case 1: 
            System.out.println("星期一"); 
            break; 
        case 2: 
            System.out.println("星期二"); 
            break; 
        case 3:
            System.out.println("星期三"); 
            break; 
        case 4: 
            System.out.println("星期四"); 
            break; 
        case 5: 
            System.out.println("星期五"); 
            break; 
        case 6: 
            System.out.println("星期六"); 
            break; 
        case 7: 
            System.out.println("星期日"); 
            break; 
        default: 
            System.out.println("你输入的数字有误"); 
            break; 
    } 
}
```

#### 4.5.1 **case**的穿透性

在switch语句中，如果case的后面不写break，将出现穿透现象，也就是不会在判断下一个case的值，直接向后运 

行，直到遇到break，或者整体switch结束。 

```java
public static void main(String[] args) { 
    int i = 5; 
    switch (i){ 
        case 0: 
            system.out.println("执行case0"); 
            break; 
        case 5: 
            System.out.println("执行case5"); 
        case 10: 
            System.out.println("执行case10"); 
        default: 
            System.out.println("执行default"); 
    } 
}
```

上述程序中，执行case5后，由于没有break语句，程序会一直向后走，不会在判断case，也不会理会break，直接 

运行完整体switch。 



### 4.6 **循环语句**

循环语句可以在满足循环条件的情况下，反复执行某一段代码，这段被重复执行的代码被称为循环体语句，当反复 

执行这个循环体时，需要在合适的时候把循环判断条件修改为false，从而结束循环，否则循环将一直执行下去，形 

成死循环。 

#### 4.6.1 **循环语句**1--for

- **for**循环语句格式：

  ```java
  for(初始化表达式①; 布尔表达式②; 步进表达式④){ 
      循环体③ 
  }
  ```

- **执行流程**

  - 执行顺序：①②③④>②③④>②③④…②不满足为止。 

  - ①负责完成循环变量初始化 

  - ②负责判断是否满足循环条件，不满足则跳出循环 

  - ③具体执行的语句 

  - ④循环后，循环条件所涉及变量的变化情况 

- 代码演示：

```java
public static void main(String[] args) { 
    //控制台输出10次HelloWorld，不使用循环 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld");
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("HelloWorld"); 
    System.out.println("‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐"); 
    //用循环改进，循环10次 //定义变量从0开始，循环条件为<10 
    for(int x = 0; x < 10; x++) { 
        System.out.println("HelloWorld"+x); 
    } 
}
```

- 循环练习：使用循环，计算1-100之间的偶数和

```java
public static void main(String[] args) { 
    //1.定义一个初始化变量,记录累加求和,初始值为0 
    int sum = 0;
    //2.利用for循环获取1‐100之间的数字
    for (int i = 1; i <= 100; i++) { 
    //3.判断获取的数组是奇数还是偶数 
        if(i % 2==0){ 
    //4.如果是偶数就累加求和 
            sum += i; 
        } 
    } 
   //5.循环结束之后,打印累加结果 
    System.out.println("sum:"+sum); 
}
```



#### 4.6.2 **循环语句**2--while

- **while**循环语句格式：

```java
初始化表达式① 
    while(布尔表达式②){ 
		循环体③ 
        步进表达式④ 
    }
```

- **执行流程**

  - 执行顺序：①②③④>②③④>②③④…②不满足为止。 

  - ①负责完成循环变量初始化。 
  - ②负责判断是否满足循环条件，不满足则跳出循环。 
  - ③具体执行的语句。 
  - ④循环后，循环变量的变化情况。 


- 代码演示

  - while循环输出10次HelloWorld 

  ```java
  public class whilePrint {
      public static void main(String[] args) {
          //while循环实现打印10次HelloWorld
          // 定义初始化变量
          int i = 1;
          //循环条件<=10
          while (i <= 10){
              System.out.println("HelloWorld-"+i);
              //步进
              i++;
          }
      }
  }
  ```

  - while循环计算1-100之间的和

  ```java
  public static void main(String[] args) {
          //使用while循环实现
          // 定义一个变量,记录累加求和
          int sum = 0;
          //定义初始化表达式
          int i = 1;
          //使用while循环让初始化表达式的值变化
          while (i <= 100){
              //累加求和
              sum += i;
              //步进表达式改变变量的值
              i++;
          }
          //打印求和的变量
          System.out.println("1-100的和为："+sum);
      }
  ```

  

#### 4.6.3 **循环语句**3--do...while

- **do...while**循环格式

```java
初始化表达式① 
    do{ 
        循环体③ 
        步进表达式④ 
    }while(布尔表达式②);
```

- **执行流程**

  - 执行顺序：①③④>②③④>②③④…②不满足为止。 

  - ①负责完成循环变量初始化。 

  - ②负责判断是否满足循环条件，不满足则跳出循环。 

  - ③具体执行的语句 

  - ④循环后，循环变量的变化情况 

- 图解：

![image-20210402150424115](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210402150424115.png)

- 代码演示

```java
 public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println("HelloWorld!"); //输出了一次
        }while (i > 3);
    }
```

- do...while循环的特点：无条件执行一次循环体，即使我们将循环条件直接写成false，也依然会循环一次。



#### 4.6.4 **循环语句的区别** 

- for和while的小区别：

  - 控制条件语句所控制的那个变量，在for循环结束后，就不能再被访问到了，而while循环结束还可以继 

    续使用，如果你想继续使用，就用while，否则推荐使用for。原因是for循环结束，该变量就从内存中消 

    失，能够提高内存的使用效率。 

  - 在已知循环次数的时候使用推荐使用for，循环次数未知的时推荐使用while。 



### 4.7 **跳出语句**

#### 4.7.1 break

- **使用场景：终止switch或者循环**

  - 在选择结构switch语句中 

  - 在循环语句中 

  - 离开使用场景的存在是没有意义的 

```java
public static void main(String[] args) { 
    for (int i = 1; i<=10; i++) { 
        //需求:打印完两次HelloWorld之后结束循环 
        if(i == 3){ 
            break; 
        }
        System.out.println("HelloWorld"+i); 
    } 
}
```

#### 4.7.2 **continue** 

- **使用场景：结束本次循环，继续下一次的循环**

```java
public static void main(String[] args) { 
    for (int i = 1; i <= 10; i++) { 
        //需求:不打印第三次HelloWorld 
        if(i == 3){ 
            continue; 
        }
        System.out.println("HelloWorld"+i); 
    } 
}
```



### 4.8 死循环

- **死循环：**也就是循环中的条件永远为true，死循环的是永不结束的循环。

- 代码演示：

```java
 public static void main(String[] args) {
        int i = 1;
        while (true){
            System.out.println("HelloWorld");
            i++;
        }
    }
```



### 4.9 嵌套循环

- **所谓嵌套循环**，是指一个循环的循环体是另一个循环。比如for循环里面还有一个for循环，就是嵌套循环。总 

共的循环次数=外循环次数*内循环次数 

- **嵌套循环格式：** 

```java
for(初始化表达式①; 循环条件②; 步进表达式⑦) { 
    for(初始化表达式③; 循环条件④; 步进表达式⑥) { 
        执行语句⑤; 
    } 
}
```

- **嵌套循环执行流程：** 

  - 执行顺序：①②③④⑤⑥>④⑤⑥>⑦②③④⑤⑥>④⑤⑥ 

  - 外循环一次，内循环多次。 

  - 比如跳绳：一共跳5组，每组跳10个。5组就是外循环，10个就是内循环。 

- 代码演示：打印5*8的矩形

```java
 public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 8; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
```



## 五、方法

### 5.1 方法的定义

- 方法的定义格式：

```java
public static void 方法名称(){
    方法体;
}
```

案例：

```java
package com.itcast.Demo01;

public class Demo01Method {
    public static void main(String[] args) {
        
    }

    public static void printMethod(){
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 20; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}

```

>注意事项：
>
>1、方法定义的先后顺序是无所谓的。
>
>2、方法定义必须是挨着的，不能在一个方法的内部定义另一个方法。
>
>3、方法定义之后，自己是不会执行的；如果希望执行，一定要进行方法的调用。



### 5.2 **定义方法的格式详解** 

- 方法声明的语法：

```java
访问修饰符 [static/final/abstract] 方法的返回值类型 方法名(参数类型1 参数名1,
			参数类型2 参数名2,...){
			代码块;
			[return 结果;]
		}

```

- 访问修饰符:表示使用权限,访问修饰符有public,protected,default(不写),private四种.一般用public修饰符.
- 方法的返回值类型:表示执行完功能返回的结果的类型,如果功能执行完不想返回任何结果就用void,如果功能执行完想返回结果,可以用java中任意数据类型,一般返回类型与大括号中return 结果;一起用,且结果的数据类型与方法的返回值类型要一致.
- 方法名:自定义,采用驼峰式命名法.
- 参数:执行功能所需要数据.一个方法可以有0个到多个参数,参数间用逗号分隔.
  		在方法中将参数当作已知变量来用.
- return:可以用在方法的任何地方.有两种用途.
  			  第一种:直接用ruturn;表示结束当前方法.
        			  第二种:用return 结果; 表示结束当前方法同时,返回一个结果,它必须配合方法的返回值类型一起用,要求结果的数据类型与方法的返回值类型一致.
- 声明方法只表示具有某种功能,方法不调用永远不执行.
- 方法与方法之间是平级关系,不能嵌套.
- 方法间可以相互调用.
- 同一个类中可以声明多个方法,但是不能有相同的方法.

### 5.3 方法的调用

- 方法的调用:从调用方法位置执行,跳转到方法声明的大括号去执行方法体,执行完方法体后又跳转到方法调用位置接着后面执行.
- 无返回值方法的调用语法:方法名([参数]);
- 有返回值方法的调用语法:数据类型 变量名=方法名([参数]);
- 注意:如果调用有返回值的方法时,不需要结果,可以不声明变量接收结果.



案例：

```java
public class Demo01Method {
    public static void main(String[] args) {
        //调用方法
        printMethod();
    }

    public static void printMethod(){
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 20; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}

```



### 5.4 方法练习

- 1、定义一个方法，用来判断两个数字是否相等

```java
package com.itcast.Demo02;

public class Demo01MethodSame {
    public static void main(String[] args) {
        System.out.println(isSame(10,20));
        System.out.println(isSame(20,20));
    }

    public static boolean isSame(int a,int b){
        return a == b;
    }
}

```

- 2、定义一个方法，用来计算1-100之间的和值

```java
package com.itcast.Demo02;

public class Demo02MethodSame {
    public static void main(String[] args) {
        System.out.println("结果是："+num());
    }

    public static int num(){
        int sum = 0;
        for (int i = 1; i <= 100; i++) {
            sum+=i;
        }
        return sum;
    }
}

```

- 3、定义一个方法，用来指定打印次数的HelloWorld

```java
package com.itcast.Demo02;

public class Demo03MethodPrint {
    public static void main(String[] args) {
        printCount(5);
    }

    public static void printCount(int num){
        for (int i = 1; i <= num; i++) {
            System.out.println("HelloWorld-"+i);
        }
    }
}

```

>注意事项：
>
>1、方法应该是定义在类当中，但是不能在方法当中再定义方法。方法不能嵌套。
>
>2、方法定义的前后顺序无所谓。
>
>3、方法定义之后不会执行，如果希望执行，一定要调用：单独调用，打印调用，赋值调用。
>
>4、如果方法有返回值，那么必须写上`return返回值;`不能没有。
>
>5、return后面的返回值数据，必须和方法的返回值类型，对应起来。
>
>6、对于一个void没有返回值的方法，不能写`return返回值;`，只能return自己，但一般省略不写。
>
>7、对于void方法当中最后一行的return可以省略不写。
>
>8、一个方法当中可以有多个return语句，但是必须保证同时只有一个会被执行到，两个return不能连写。



### 5.5 方法的参数

- 形参:方法声明时小括号中参数叫形参,形参前面一定要写数据类型.

- 实参:方法调用时小括号中参数叫实参,实参前面一定不要写数据类型.

- 注意:对于同一个方法,它的实参与形参的个数,类型,顺序要匹配.

- 传参:将实参的值传递给形参变量,这个过程叫传参.

  

### 5.6 方法的重载

- 1、方法的重载（overload）：指在同一个类中，允许存在一个以上的同名方法，只要它们的参数列表不同即可，与修饰符和返 

  回值类型无关。 

- 2、重载的好处：只需要记住唯一一个方法的名称，就可以实现类似的多个功能。 
- 3、参数列表：个数不同，数据类型不同，顺序不同。 
- 4、重载方法调用：JVM通过方法的参数列表，调用不同的方法。 

3、代码演示：

```java
package com.itcast.Demo03;

public class MethodOverload {
    public static void main(String[] args) {
        System.out.println(sum(10,20));
        System.out.println(sum(10,20,30));
        System.out.println(sum(10,20,30,40));
    }

    public static int sum(int a,int b){
        System.out.println("有2个参数的方法执行");
        return a + b;
    }

    public static int sum(int a,int b,int c){
        System.out.println("有3个参数的方法执行");
        return a + b + c;
    }

    public static int sum(int a,int b,int c,int d){
        System.out.println("有4个参数的方法执行");
        return a + b + c + d;
    }
}

```

- 方法重载与下列因素相关：
  - 1、参数个数不同
  - 2、参数类型不同
  - 3、参数的多类型顺序不同

- 方法重载与下列因素无关：
  - 1、与参数的名称无关
  - 2、与方法的修饰符无关
  - 2、与方法的返回值类型无关

### 5.7 方法重载练习

1、判断哪些方法是重载关系。 

```java
 	1.public static void open(){} //正确重载
    2.public static void open(int a){} //正确重载
    3.static void open(int a,int b){} //跟第八行冲突，方法的重载跟参数名称没有关系
    4.public static void open(double a,int b){} //正确重载
    5.public static void open(int a,double b){} //跟第六行冲突，方法的重载跟参数名称没有关系
    6.public void open(int i,double d){} //跟第五行冲突，方法的重载跟参数名称没有关系
    7.public static void OPEN(){} //正确的方法，但名称不一样。java是严格区分大小写的
    8.public static void open(int i,int j){}//跟第三行冲突，方法的重载跟参数名称没有关系
```



### 5.8 递归

- 递归:方法自身调用自身.

![image-20210414171356152](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210414171356152.png)



- 使用递归和条件:

  - 将原问题拆分为若干个子问题,子问题的解决方法与原问题一样.

  - 原问题的解决依赖于所有子问题解决.

  - 递归一定要有出口.

    

- 代码演示：

  ```java
  /**
   * 递归的引入
   * @author sx
   * @version 2021年4月13日
   */
  public class DiguiTest1 {
  
  	public static void main(String[] args) {
  		//获得具有从键盘上接收数据的能力
  		Scanner input=new Scanner(System.in);
  		System.out.println("请输入一个整数:");
  		//将从键盘上接收的数存在变量中
  		int num=input.nextInt();
  		//调用方法计算阶乘并得到结果
  		int result=digui(num);
  		System.out.println(num+"的阶乘递归结果为:"+result);
  	}
  	
  	/**
  	 * 计算一个数递归
  	 * @param n
  	 * @return int
  	 */
  	public static int digui(int n) {//n=1
  		if (n==1) {
  			return 1;
  		} else {
  			return n*digui(n-1);
  			//5*digui(4)
  			//5*4*digui(3);
  			//5*4*3*digui(2);
  			//5*4*3*2*digui(1)
  			//5*4*3*2*1
  		}
  	}
  	
  	
  	
  //	/**
  //	 * 计算5的递归
  //	 * @param n
  //	 */
  //	public static int digui5(int n) {//n=5
  //		return n*digui4(n-1);
  //	}
  //	
  //	/**
  //	 * 计算4的递归
  //	 * @param n
  //	 */
  //	public static int digui4(int n) {//n=4
  //		return n*digui3(n-1);
  //	}
  //	
  //	/**
  //	 * 计算3的递归
  //	 * @param n
  //	 */
  //	public static int digui3(int n) {//n=3
  //		return n*digui2(n-1);
  //	}
  //	
  //	/**
  //	 * 计算2的递归
  //	 * @param n
  //	 */
  //	public static int digui2(int n) {//n=2
  //		return n*digui1(n-1);
  //	}
  //	
  //	/**
  //	 * 计算1的递归
  //	 * @param n
  //	 */
  //	public static int digui1(int n) {//n=1
  //		return n;
  //	}
  
  ```

  

## 六、数组

### 6.1 数组的概念

- **数组概念：** 数组就是存储数据长度固定的容器，保证多个数据的数据类型要一致。



### 6.2 一维数组的定义

**方式一：**

- 格式：

```
数组存储的数据类型[] 数组名字 = new 数组存储的数据类型[长度];
```

- 数组定义格式详解： 

  - 数组存储的数据类型： 创建的数组容器可以存储什么数据类型。 

  - [] : 表示数组。 

  - 数组名字：为定义的数组起个变量名，满足标识符规范，可以使用名字操作数组。 

  - new：关键字，创建数组使用的关键字。 

  - 数组存储的数据类型： 创建的数组容器可以存储什么数据类型。 

  - [长度]：数组的长度，表示数组容器中可以存储多少个元素。 
  - **注意：数组有定长特性，长度一旦指定，不可更改**

- 举例：定义可以存储3个整数的数组容器

```java
int[] arr = new int[3];
```



**方式二:**

- 格式：

```java
数据类型[] 数组名 = new 数据类型[]{元素1,元素2,元素3...};
```

- 举例：定义存储1，2，3，4，5整数的数组容器。

```java
int[] arr = new int[]{1,2,3,4,5};
```



**方式三：**

- 格式：

```java
数据类型[] 数组名 = {元素1,元素2,元素3...};
```

- 举例：定义存储1，2，3，4，5整数的数组容器 

```java
int[] arr = {1,2,3,4,5};
```



### 6.3 一维**数组的访问** 

- **索引：** 每一个存储到数组的元素，都会自动的拥有一个编号，从0开始，这个自动编号称为**数组索引** 

  **(index)**，可以通过数组的索引访问到数组中的元素。

- 格式：

```java
数组名[索引]
```

- **数组的长度属性：** 每个数组都具有长度，而且是固定的，Java中赋予了数组的一个属性，可以获取到数组的 

  长度，语句为： 数组名.length ，属性length的执行结果是数组的长度，int类型结果。由次可以推断出，数 

  组的最大索引值为 数组名.length-1 。 

```java
public static void main(String[] args) { 
    int[] arr = new int[]{1,2,3,4,5}; 
    //打印数组的属性，输出结果是5 
    System.out.println(arr.length); 
}
```

- **索引访问数组中的元素：** 

  - 数组名[索引]=数值，为数组中的元素赋值 

  - 变量=数组名[索引]，获取出数组中的元素 

```java
public static void main(String[] args) { 
    //定义存储int类型数组，赋值元素1，2，3，4，5 
    int[] arr = {1,2,3,4,5};
    //为0索引元素赋值为6 
    arr[0] = 6; 
    //获取数组0索引上的元素 
    int i = arr[0]; 
    System.out.println(i); 
    //直接输出数组0索引元素 
    System.out.println(arr[0]); 
}
```



### 6.4 一维数组在内存中的存储

**一个数组内存图** 

```java
public static void main(String[] args) { 
    int[] arr = new int[3]; 
    System.out.println(arr);//[I@5f150435 
}
```

[I@5f150435这个是数组在内存中的地址。new出来的内容，都是在堆 

内存中存储的，而方法中的变量arr保存的是数组的地址。 

**输出**arr[0]，就会输出**arr**保存的内存地址中数组中**0**索引上的元素

![image-20210402172345420](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210402172345420.png)

**两个变量指向一个数组** 

```java
public static void main(String[] args) { 
    // 定义数组，存储3个元素 
    int[] arr = new int[3]; 
    //数组索引进行赋值 
    arr[0] = 5; 
    arr[1] = 6;
    arr[2] = 7; 
    //输出3个索引上的元素值 
    System.out.println(arr[0]); 
    System.out.println(arr[1]); 
    System.out.println(arr[2]); 
    //定义数组变量arr2，将arr的地址赋值给arr2 
    int[] arr2 = arr; 
    arr2[1] = 9;
    System.out.println(arr[1]); 
}
```

![image-20210403155123336](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210403155123336.png)

### 6.5 一维**数组的常见操作** 

#### 6.5.1 **数组越界异常**

```java
public static void main(String[] args) { 
    int[] arr = {1,2,3}; 
    System.out.println(arr[3]); 
}
```

创建数组，赋值3个元素，数组的索引就是0，1，2，没有3索引，因此我们不能访问数组中不存在的索引，程序运 

行后，将会抛出 `ArrayIndexOutOfBoundsException` 数组越界异常。在开发中，数组的越界异常是**不能出现**的，一 

旦出现了，就必须要修改我们编写的代码。 



#### 6.5.2 **数组空指针异常** 

```java
public static void main(String[] args) { 
    int[] arr = {1,2,3}; 
    arr = null; 
    System.out.println(arr[0]); 
 ｝
```

`arr = null` 这行代码，意味着变量arr将不会在保存数组的内存地址，也就不允许再操作数组了，因此运行的时候 

会抛出 `NullPointerException` 空指针异常。在开发中，数组的越界异常是**不能出现**的，一旦出现了，就必须要修 

改我们编写的代码



#### 6.5.3 数组的遍历

- **数组遍历：** 就是将数组中的每个元素分别获取出来，就是遍历。遍历也是数组操作中的基石。 

- 方法一：

```java
public static void main(String[] args) { 
    int[] arr = { 1, 2, 3, 4, 5 }; 
    System.out.println(arr[0]); 
    System.out.println(arr[1]); 
    System.out.println(arr[2]); 
    System.out.println(arr[3]); 
    System.out.println(arr[4]); 
}
```

- 方法二：

```java
public static void main(String[] args) {
       int[] arr = {1,2,3,4,5};
       for (int i = 0; i < arr.length; i++) {
           System.out.println(arr[i]);
        }
    }
```



#### 6.5.4  **数组获取最大值元素**	

- **最大值获取：**从数组的所有元素中找出最大值。 

- **实现思路：** 

  - 定义变量，保存数组0索引上的元素 

  - 遍历数组，获取出数组中的每个元素 

  - 将遍历到的元素和保存数组0索引上值的变量进行比较 

  - 如果数组元素的值大于了变量的值，变量记录住新的值 

  - 数组循环遍历结束，变量保存的就是数组中的最大值 

- 代码演示：

```java
public static void main(String[] args) {
       int[] arr = {2,20,200,2000,20000};
       int max = arr[0];
        for (int i = 0; i <arr.length ; i++) {
            if (arr[i] > max){
                max = arr[i];
            }
        }
        System.out.println("max:"+max);
    }
```



#### 6.5.5 数组反转

- **数组的反转：** 数组中的元素颠倒顺序，例如原始数组为1,2,3,4,5，反转后的数组为5,4,3,2,1 

- **实现思想：**数组最远端的元素互换位置。 

  - 实现反转，就需要将数组最远端元素位置交换 

  - 定义两个变量，保存数组的最小索引和最大索引 

  - 两个索引上的元素交换位置 

  - 最小索引++，最大索引--，再次交换位置 

  - 最小索引超过了最大索引，数组反转操作结束 

- 图解：

![image-20210404101912494](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404101912494.png)



- 代码演示：（方式一）

```java
 public static void main(String[] args) {
        int[] arr = {10,20,30,40,50};
        for (int min = 0, max = arr.length-1;min<=max;min++,max--){
            int temp = arr[min];
            arr[min] = arr[max];
            arr[max] = temp;
        }
        for (int i = 0; i <arr.length ; i++) {
            System.out.println(arr[i]);
        }
    }
```



- 方式二

  ```java
  public static void main(String[] args) {
      String[] arr = new String[]{"KK","JJ","HH","GG","FF","DD","SS","AA"};
          for (int i = 0, j = arr.length-1; i < j ;i++,j--) {
              String temp = arr[i];
              arr[i] = arr[j];
              arr[j] = temp;
          }
  
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i]+"\t");
          }
          System.out.println();
      }
  }
  
  ```



#### 6.5.6 数组的复制

```java
 public static void main(String[] args) {
        String[] arr = new String[]{"KK","JJ","HH","GG","FF","DD","SS","AA"};

        //数组的复制
        String[] arr1 = new String[arr.length];
        for (int i = 0; i < arr1.length; i++) {
            arr1[i]=arr[i];
        }

        //遍历
        for (int i = 0; i < arr1.length; i++) {
            System.out.print(arr1[i]+"\t");
        }
        System.out.println();
     }
}
```



#### 6.5.7 线性查找

```java
public class ArrayTest03 {
    public static void main(String[] args) {
        String[] arr = new String[]{"KK","JJ","HH","GG","FF","DD","SS","AA"};

        //线性查找
        String dest = "GG";
        Boolean flag = true;
        for (int i = 0; i < arr.length; i++) {
            if (dest.equals(arr[i])){
                System.out.println("找到了指定的元素，位置在："+i);
                flag = false;
                break;
            }
        }
        if (flag){
            System.out.println("抱歉，没有找到！");
        }
    }
}
```



#### 6.5.8 二分法查找

- 注意：所要查找的数组必须是有序的。

```java
public class ArrayTest04 {
    public static void main(String[] args) {
        int[] arr = new int[]{-98,-45,-23,-5,0,23,28,45,57,98,125};

        int dest = 2;
        int head = 0;
        int end = arr.length-1;
        boolean flag = true;

        while (head <= end){
            int middle = (head+end)/2;

            if (dest == arr[middle]){
                System.out.println("恭喜你，找到了，位置在："+middle);
                flag = false;
                break;
            }else if (dest < arr[middle]){
                end = middle - 1;
            }else{
                head = middle + 1;
            }
        }
        if (flag){
            System.out.println("很遗憾，没有找到哦！");
        }
    }
}
```



#### 6.5.9 冒泡排序

```java
public class ArrayTest05 {
    public static void main(String[] args) {
        int[] arr = new int[]{5,2,7,4,9,0,-2,12,3};

        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = 0; j < arr.length-1-i; j++) {
                if (arr[j] > arr[j+1]){
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }

        //遍历
        for (int n: arr) {
            System.out.print(n+"\t");
        }
    }
}

```



#### 6.5.10 选择排序

- 选择排序:第一轮将这列数的第一个数取出,依次与后面每个数一一比较,互换位置,比完后,第一个数就是最小值或最大值,这个值不参与后面的比较;第二轮将剩下数中第一个数取出,依次与后面每个数一一比较,互换位置,比完后,第一个数就是最小值或最大值这个值不参与后面的比较;后面依次类推.
- 图解

![image-20210414202523542](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210414202523542.png)

```java
public static void main(String[] args) {
		//准备一个数组
		int[] nums= {5,8,1,7,6,3};
		
		/*选择排序*/
		//外层循环控制比较轮数
		for (int i = 0; i < nums.length-1; i++) {
			//内层循环控制比较每个数索引(次数)
			for (int j = i+1; j < nums.length; j++) {
				if (nums[i]>nums[j]) {
					int temp=nums[i];
					nums[i]=nums[j];
					nums[j]=temp;
				}
			}
		}
		
		//输出排序后的结果
		for (int i : nums) {
			System.out.print(i+"\t");
		}
	}
```



### 6.6  **数组作为方法参数和返回值**

- **任何数据类型都能作为方法的参数类型，或者返回值类型**

#### 6.6.1 **数组作为方法参数**

- **数组作为方法参数传递，传递的参数是数组内存的地址。** 

```java
public static void main(String[] args) {
        int[] array = {10,20,30};
        ArrayMethod(array);
        System.out.println("=====AA=====");
        ArrayMethod(array);
    }

    public static void ArrayMethod(int[] array){
        for (int i = 0; i < array.length; i++){
            System.out.println(array[i]);
        }
    }
```

- 图解：

![image-20210404102641383](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404102641383.png)



#### 6.6.2 **数组作为方法返回值**

- **数组作为方法的返回值，返回的是数组的内存地址** 

```java
 public static void main(String[] args) {
        //调用方法，接收数组的返回值
        // 接收到的是数组的内存地址
        int[] a = getArray();
        for (int i = 0;i < a.length;i++){
            System.out.println(a[i]);
        }
    }
    /*
    创建方法，返回值是数组类型 return返回数组的地址
     */
    public static int[] getArray(){
        //返回数组的地址，返回到调用者
        int[] arr = {1,2,3,4,5};
        return arr;
    }
```

- 图解

![image-20210404103740899](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404103740899.png)

> 总结: 
>
> **方法的参数为基本类型时**,**传递的是数据值**. **方法的参数为引用类型时**,**传递的是地址值**.



### 6.7 Arrays：数组的工具类

- 将数组转换为字符串:Arrays.toString(数组名); 
- 对数组进行排序(默认升序):Arrays.sort(数组名); 
- 对已经排安序的数组用二分查找法查找指定元素:Arrays.binarySearch(数组名, 要查找的元素); 
- 将原数组中指定长度复制到新数组中:Arrays.copyOf(原数组, 长度) 
- 将原数组中指定索引范围内元素复制到新数组中:copyOfRange(原数组, 起始索引, 终止索引) 



### 6.8 动态参数(可变个数参数)

- 动态参数(可变个数参数):由0到多个相同类型参数组成.语法:数据类型...参数名
- 动态参数的实参可以传递0到多个值.
- 动态参数在方法中当作已知的数组来使用.
- 动态参数在实参传递时可以直接传递一个数组,只要数组的数据类型与动态参数的类型兼容.
- 因为动态参数必须是方法的最后一个参数,所以一个方法最多只能有一个动态参数.
- 动态参数与普通参数可以一起使用作为方法的形参,只是动态参数必须作为最后一个参数.



### 6.9 二维数组

- 二维数组:在内存中开辟一段连续的空间,每个空间存一个一维数组.

- 二维数组的特征:

  - 二维数组是一种引用数据类型的变量.
  - 二维数组的组成:数组名,数组数据类型,元素(每个空间是一维数组),索引(二维数组的索引,一维数组索引).
  - 二维数组的长度:数组名.length
  - 二维数组中每个空间一维数组长度:数组名[二维数组的索引].length
  - 二维数组的索引范围:[0,数组名.length-1]	
  - 二维数组的索引超过范围会报异常ArrayIndexOutOfBoundsException
  - 二维数组的每个空间的访问:数组名[二维数组索引]
  - 二维数组的每个空间的一维数组的元素访问:数组名[二维数组索引] [一维数组索引]
  - 同一个数组,每个元素的数据类型相同;不同的数组数据类型可以不同.

  - 二维数组一但分配了空间,它的长度是固定.
  - 二维数组一但分配了空间就有默认值,二维数组每个空间的默认值为null 
  - 二维数组的每个空间的一维数组分配空间,就有默认值
    	String类型数组,每个空间默认值为null
    	char类型数组,每个空间默认值为\u0000(空格)
    	int类型数组,每个空间默认值为0
    	double类型数组,每个空间默认值为0.0
    	boolean类型数组,每个空间默认值为false
  - 二维数组一但分配了空间,就可以使用.
  - 二维数组直接输出,输出的是内存地址.

- 二维数组的使用
  二维数组的声明的语法:
  		数据类型[][] 数组名; (推荐)
  		数据类型 数组名[][];

  ```java
  //声明二维数组
  String[][] stuNames1;
  int stuAges1[][];
  ```

- 二维数组分配空间

  给已经声明二维数组分配空间,且给每个空间的一维数组空间相同的语法:
  			数组名=new 数据类型[二维数组长度] [一维数组的长度];

  ```java
  //给二维数组分配空间且每个空间一维数组空间相同
  stuNames1=new String[3][2];
  
  ```

  给已经声明二维数组分配空间,且给每个空间的一维数组空间不同的语法:
  			数组名=new 数据类型[二维数组长度] [];
  			//给每个空间的一维数组单独分配空间
  			数组名[二维索引]=new 数据类型[一维数组长度];

  ```java
  //给二维数组分配空间且每个空间一维数组空间不相同
  stuAges1=new int[3][];
  //单独给二维数组每个空间的一维数组分配空间
  stuAges1[0]=new int[3];
  stuAges1[1]=new int[1];
  stuAges1[2]=new int[2];
  
  ```

  在声明数组的同时给二维数组分配空间,且每个空间的一维数组空间相同的语法
  			数据类型[][] 数组名=new 数据类型[二维数组长度] [一维数组的长度];

  ```java
  数据类型[][] stuNames1=new String[3][2];
  ```

  在声明数组的同时给二维数组分配空间,且每个空间的一维数组空间不相同的语法
  			数据类型[][] 数组名=new 数据类型[二维数组长度] [];
  			//给每个空间的一维数组单独分配空间
  			数组名[二维索引]=new 数据类型[一维数组长度];

  

- 二维数组赋值

  - 动态赋值:给二维数组中每个空间一维数组的每个空间一一赋值.
    			 适用场景:任何情况.
          			 语法: 二维数组名[二维数组索引] [一维数组索引]=值;

  ```java
  //动态赋值
  stuNames1[0][0]="张一";
  stuNames1[0][1]="张二";
  		
  stuNames1[1][0]="李一";
  stuNames1[1][1]="李二";
  		
  stuNames1[2][0]="王一";
  stuNames1[2][1]="王二";
  
  ```

  - 静态赋值:将声明数组,分配空间及赋值合三为一.
    			  适用场景:对数组中元素已知
          			 语法一:数据类型[][] 数组名=new 数据类型[][]{{值11,值12...},

    ```java
    //第一种:静态赋值
    	String[][] hobbys1=new String[][] {{"play games","basketball"},												{"sleep","study","music"}};
    
    ```

    ​			 语法二:数据类型[][] 数组名={{值11,值12...},{值21,值22}...};

    ```java
    //第二种:静态赋值
    double[][] scores1= {{99.5,59.5},{59,99,100,60}};
    
    ```



- 二维数组遍历

  ```java
  		/*第一种:for-for遍历二维数组*/
  		//外层循环遍历二维数组每个空间,i二维数组索引
  		for (int i = 0; i < stuNames1.length; i++) {
  			System.out.println("二维数组的每个空间:"+stuAges1[i]);
  			//内层循环遍历二维数组每个空间的一维数组,一维数组的索引
  			for (int j = 0; j <stuNames1[i].length;j++) {
  				System.out.print(stuNames1[i][j]+"\t");
  			}
  			//换行
  			System.out.println();
  		}
  		
  		System.out.println("$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$");
  		/*第二种:foreach-foreach遍历二维数组*/
  		for (String[] hh : hobbys1) {
  			System.out.println("二维数组的每个空间:"+hh);
  			for (String h : hh) {
  				System.out.print(h+"\t");
  			}
  			System.out.println();
  		}
  		
  		System.out.println("&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&");
  		/*第三种:遍历二维数组*/
  		for (double[] ds : scores1) {
  			System.out.println(Arrays.toString(ds));
  	    }
  
  ```

  

## 七、**面向对象思想**

### 7.1 **类和对象** 

**什么是类** 

- **类**：是一组相关**属性**和**行为**的集合。可以看成是一类事物的模板，使用事物的属性特征和行为特征来描述该 

  类事物。 

现实中，描述一类事物： 

- **属性**：就是该事物的状态信息。 

- **行为**：就是该事物能够做什么。 

举例：小猫。 

属性：名字、体重、年龄、颜色。 

行为：走、跑、叫。 



**什么是对象** 

- **对象**：是一类事物的具体体现。对象是类的一个**实例**（对象并不是找个女朋友），必然具备该类事物的属性 

和行为。 

现实中，一类事物的一个实例：一只小猫。 

举例：一只小猫。 

属性：tom、5kg、2 years、yellow。 

行为：溜墙根走、蹦跶的跑、喵喵叫。 



**类与对象的关系** 

- 类是对一类事物的描述，是**抽象的**。 

- 对象是一类事物的实例，是**具体的**。 

- **类是对象的模板，对象是类的实体**。



### 7.2 **类的定义** 

**类的定义语法** 

```java
访问修饰符 class 类名{
	访问修饰符 数据类型 变量名;//成员变量或属性
		...
				
	访问修饰符 返回值类型 方法名(参数类型1 参数名1,参数类型2 参数名2..){
		代码块;
		[return 结果;]
	}
	...
} 

```

- 声明类的关键字:class
- 声明类的访问修饰符只能是public或默认(不写),不能用其他访问修饰符.
- 类名采用帕斯卡命名法,变量名和方法名采用驼峰式命名法.
- 一个类可以有0到多个属性,也可以有0到多个方法.
- 在声明类时,我们只写与研究问题相关的属性和方法.



类的定义格式举例：

```java
public class Student { 
    //成员变量 
    String name；//姓名 
    int age；//年龄
        
    //成员方法 
   //学习的方法 
   public void study() { 
        System.out.println("好好学习，天天向上"); 
    }
    //吃饭的方法 
    public void eat() { 
        System.out.println("学习饿了要吃饭"); 
    } 
}
```



### 7.3 **对象的使用** 

**对象的使用格式** :

创建对象： 

注意:类中成员变量和方法属于对象,每个对象独有一份类中成员变量和方法.

```java
类名 对象名 = new 类名();
```

理解:由类生成对象;
		类是一种引用数据类型,对象就是变量名(所以对象名采用驼峰式命名法).
		调用构造方法创建对应类的对象.

使用对象访问类中的成员: 	

```java
对象名.成员变量； 
对象名.成员方法()；
```

对象的使用格式举例: 

```java
public class Test01_Student { 
    public static void main(String[] args) { 
    //创建对象格式：类名 对象名 = new 类名(); 
    Student s = new Student(); 
    //直接输出成员变量值 
    System.out.println("姓名："+s.name); //null 
    System.out.println("年龄："+s.age); //0 
    System.out.println("‐‐‐‐‐‐‐‐‐‐"); 
    //给成员变量赋值 
    s.name = "赵丽颖"; 
    s.age = 18; 
    //再次输出成员变量的值 
    System.out.println("姓名："+s.name); //赵丽颖 
    System.out.println("年龄："+s.age); //18 
    System.out.println("‐‐‐‐‐‐‐‐‐‐"); 
    //调用成员方法 
    s.study(); // "好好学习，天天向上" 
    s.eat(); // "学习饿了要吃饭" 
   }
}
```

**成员变量的默认值**:

|          | **数据类型**                   | **默认值** |
| -------- | ------------------------------ | ---------- |
| 基本类型 | 整数（byte，short，int，long） | 0          |
|          | 浮点数（float，double）        | 0.0        |
|          | 字符（char）                   | '\u0000'   |
|          | 布尔（boolean）                | false      |
| 引用类型 | 数组，类，接口                 | null       |



### 7.4 **类与对象的练习** 

定义手机类： 

```java
public class Phone {
    //成员变量
    String brand; //品牌
    int price; //价格
    String color; //颜色

    //成员方法
    //打电话
    public void call(String name){
        System.out.println("给"+name+"打电话");
    }

    //发短信
    public void sendMessage(){
        System.out.println("群发信息");
    }
}
```

定义测试类： 

```java
public class Test01Phone {
    public static void main(String[] args) {
        //创建对象
        Phone P = new Phone();

        //输出成员变量值
        System.out.println("品牌："+P.brand); //null
        System.out.println("价格："+P.price); //0
        System.out.println("颜色："+P.color); //null

        System.out.println("===============");

        //给成员变量赋值
        P.brand="苹果";
        P.price=7399;
        P.color="白色";

        //再次输出成员变量值
        System.out.println("品牌："+P.brand); //苹果
        System.out.println("价格："+P.price); //7399
        System.out.println("颜色："+P.color); //白色

        //调用成员方法
        P.call("小明");
        P.sendMessage();
    }
}

```



### 7.5  **对象内存图** 

**一个对象，调用一个方法内存图** 

![image-20210404144122795](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404144122795.png)

> 通过上图，我们可以理解，在栈内存中运行的方法，遵循"先进后出，后进先出"的原则。变量p指向堆内存中 
>
> 的空间，寻找方法信息，去执行该方法。 



**两个对象，调用同一方法内存图** 

![image-20210404144232658](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404144232658.png)

> 对象调用方法时，根据对象中方法标记（地址值），去类中寻找方法信息。这样哪怕是多个对象，方法信息 
>
> 只保存一份，节约内存空间。



**一个引用，作为参数传递到方法中内存图** 

![image-20210404144453707](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210404144453707.png)

> 引用类型作为参数，传递的是地址值。 



### 7.6 属性(**成员变量)和局部变量区别** 

- 1.相同点：

  - 定义变量的格式：数据类型  变量名 = 变量值；
  - 先声明，后使用
  - 变量都有其对应的作用域


- 2.不同点

  - 声明位置不同:成员变量在类中方法外面声明的变量叫成员变量;
    						局部变量在方法中声明的变量叫局部变量;

  - 内存分配不同:成员变量存在内存的堆中;局部变量存在内存的栈中.

  - 作用范围不同:成员变量的作用范围由访问修饰符决定;
    				        局部变量的作用范围仅在声明它的大括号中有用.

  - 生命周期不同:成员变量的生命周期与对象同生共死(成员变量属于对象).
    				        局部变量的生命周期仅在声明时产生,在声明的大括号执行完就销毁.

  - 初始值不同:成员变量不赋值,系统会给成员变量赋默认值,
    				int类型成员变量,默认值是0
          				double类型成员变量,默认值是0.0
          				char类型成员变量,默认值是\u0000;
          				boolean类型成员变量,默认值是false
          				String类型成员变量,默认值是null
          				引用类型成员变量,默认值是null
          			  局部变量不赋值,没有值,系统不会给局部变量赋默认值.
  - 访问修饰符不同:成员变量一定会有访问修饰符;局部不能用访问修饰符.
  - 优先级不同:当成员变量和局部变量同名时,局部变量的优先级更高.



### 7.7 构造方法

- 声明的语法:访问修饰符 方法名(数据类型1 参数1,数据类型2 参数2...){

  }

- 构造方法没有方法的返回值,连void都没有;
- 构造方法名与类名相同.
- 构造方法作用:创建对象;创建对象同时给对象的属性赋值.
- 构造方法在创建对象时调用.
- 一个java类无论如何都有构造方法,如果我们没有给Java类声明构造方法,系统会给这个类默认分配一个无参无返回值的构造方法;如果我们给Java类分配构造方法,系统就不会再给这个Java类分配默认构造方法了.
- 构造的使用场景:如果只是想创建对象,用系统默认分配构造方法就可以了,不用自己给类写构造方法;如果想在创建对象的同时给对象的属性赋值,就需要自己给类写构造方法,一般情况下给类写构造方法时,习惯性写一个无参构造方法,使你创建对象的灵活性更高.



### 7.8 **方法参数的值传递机制**

- 形参是基本数据类型：将实参基本数据类型变量的“数据值”传递给形参

- 形参是引用数据类型：将实参引用数据类型变量的“地址值”传递给形参



## 八、Java的三大特征

### 8.1 封装

- 隐藏事物内部细节,提供对外访问方法.作用:实现代码复用;保护数据安全.
- 对功能封装:将功能封装成一个方法.作用:实现代码复用.
- 对属性的封装:私有化属性,给属性提供公有获得属性设值属性的get和set方法供外界使用.



### 8.2 继承

- 继承：满足is-a关系用继承;为了功能方便使用,用继承;

- 继承关键字:extends
  - 被继承的类:父类,基类,超类
  - 继承的类:子类,衍生类,派生类
- 子类可以继承父类用public或protected修饰的属性和方法
- 子类不可以继承父类构造方法,不能继承父类私有的属性和方法.
- 创建子类对象时,我们在子类中没有写代码调用父类构造,系统默认先调用父类的无参构造,再调用子类指定构造方法;如果写代码调用父类指定构造,系统不会默认调用,按照我们写的调用父类指定构造,再调用子类指定构造.
- 继承的特性:
  - 单根性:一个Java类只能有一个直接父类.
  - 传递性:A类继承B类,B类继承C类,那么A类间接继承C类.	



### 8.3 访问修饰符

![image-20210419210455455](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210419210455455.png)



### 8.4 方法的重写

- 方法重写:一定是发生在有继承关系的子类中.
- 适用场景:当子类继承父类的方法后,这个方法无法满足子类的需求,这时就需要在子类用方法重写.
- 方法重写的条件:
  - 发生在有继承关系的子类中.
  - 重写的方法与被重写方法的方法名和参数列表要一致.
  - 重写的方法与被重写方法的返回值类型相同或兼容.
  - 重写的方法的访问修饰符与被重写方法的访问修饰符相同或访问范围更大.
  - 在重写的方法前面加@Override,系统会自动判断当前方法是否是重写父类的方法.

```java
/**
 * 宠物类
 * @author sx
 * @version 2021年4月19日
 */

public class Pet {
	/**
	 * 昵称属性
	 */
	public String nickName;
	/**
	 * 品种属性
	 */
	public String breed;
	
	public void eat() {
		System.out.println("宠物在吃");
	}
	
	public void cry() {
		System.out.println("宠物在叫");
	}
}

/**
 * 狗类,继承宠物类
 * @author sx
 * @version 2021年4月19日
 */
public class Dog extends Pet{
	/**
	 * 重写父类叫的方法
	 */
	@Override
	public void cry() {
		System.out.println("狗在旺旺的叫");
	}
	
	/**
	 * 重写父类吃的方法
	 */
	@Override
	public void eat() {
		System.out.println("狗在吃狗粮");
	}
}

```



### 8.5 方法重写 VS 方法重载
- 作用不同:方法重写一般用在当子类继承父类的方法后,这个方法无法满足子类需求才用方法重写,所以方法重写覆盖父类继承过来的方法满足子类需求。方法重载是为了解决在同一个类中功能相同的方法的命名和调用问题.
- 条件不同:方法重写一定发生在有继承关系的子类中,且重写的方法与父类被重写方法的方法名和参数列表相同,返回值相同或兼容,访问修饰符相同或更大。方法重载发生在同一个类中,方法名相同,参数列表不同,与访问修饰符和返回值类型无关.
- 检查不同:方法重写可以用@Override注解自动判断;方法重载只能开发人员自己判断.

### 8.6 super

- super:指代父类对象的引用.
- 调用父类属性:super.属性名;
- 调用父类的方法:super.方法名([实参列表]);
- 调用父类的构造方法:super([实参列表]),构造方法的调用必须写在方法体的第一句.

```java
public class SuperTest {
    public static void main(String[] args) {
        B b = new B();
        b.upload();
    }
}

class A{
    public void upload(){
        System.out.println("哈哈哈");
    }
}

class B extends A{
    @Override
    public void upload() {
        super.upload();
        System.out.println("嘿嘿嘿");
    }
}
```



- super()：表示调用父类`无参构造`方法。如果没有书写构造方法，系统会默认分配一个无参的构造方法。

```java
public class SuperTest02 {
    public static void main(String[] args) {
        new c();
    }
}

class a{

    public a() {
        System.out.println("A()");
    }
}

class b extends a{
    public b(){
        super();
        System.out.println("B()");
    }
}

class c extends b{
    public c(){
        super();
        System.out.println("C()");
    }
}
```



- super(实参)：表示调用父类有参构造方法

```java
public class SuperTest03 {
    public static void main(String[] args) {
        new p();
        new p(1);
    }
}

class q{
    public q(){
        System.out.println("q()");
    }

    public q(int n){
        System.out.println("q()");
    }
}

class p extends q{
    public p(){
        super();
        System.out.println("p()");
    }

    public p(int n){
        super(n);
        System.out.println("p()");
    }
}
```



### 8.7 this vs super
- 作用范围不同:this指代当前类的对象的引用,在当前类中可用;
  						super指代父类的对象的引用,在所有子类中可用;
- 使用不同:this在方法形参与属性名一致时,且要将形参赋值给属性时,必须使用;
  				super都可以不使用.
- 用this或super调用构造方法时,必须写在构造方法的第一句.





### 8.8 多态

- 多态:一定是发生在有继承关系的基础.

- 概念:
  		生活中多态:同一种事物,由于外界条件不同,产生不同结果.
    		程序中多态:用父类或父接口作为类型,创建不同子类对象,调用同一种方法,执行的是不同操作.

- 多态应用:
  		多态的第一种应用:用父类作为数据类型,创建不同子类,调用同一个方法,执行不同的操作.

  ```java
  public static void main(String[] args) {
  		//多态第一种应用:用父类作为数据类型,创建不同子类对象,调用同一种方法,执行不同操作
  		Pet p1=new Cat();
  		Pet p2=new Dog();
  		
  		p1.eat();
  		p2.eat();
  }
  
  ```



- 多态的第二种应用:用父类或父接口作为方法形参,实参传不同子类对象,调用同一种方法,执行不同操作.

  ```java
  /**
   * 主人类
   * @author sx
   * @version 2021年4月19日
   */
  public class Master {
  	/**
  	 * 主人给宠物喂食
  	 * 多态第二种应用:用父类作为方法形参,实参传任何一个子类对象都可
  	 * @param p
  	 */
  	public void feedPet(Pet p) {
  		System.out.println("主人在喂食");
  		p.eat();
  	}
  	
  }
  
  public static void main(String[] args) {
  		/*多态第二种应用:用父类作为方法形参,实参传不同子类对象,调用同一种方法,执行不同操作*/
  		//创建对象
  		Master m=new Master();
  		//创建对象的同时,将对象作为方法实参
  		m.feedPet(new Cat());
  		m.feedPet(new Dog());
  }
  
  ```

  

- 多态的第三种应用:用父类作为方法返回值类型,实际返回任意一个子类对象,调用同一种方法,执行不同操作.

  ```java
  /**
   * 主人类
   * @author sx
   * @version 2021年4月19日
   */
  public class Master {
  	
  	/**
  	 * 主人获得宠物,查看一下的方法
  	 * 多态第三种应用:用父类作为方法返回值类型,实际任意一个子类对象
  	 * @param s 
  	 * @return Pet 用自定义的类作为方法返回值类型
  	 */
  	public Pet lookPet(String s) {
  		//声明一个对象
  		Pet p=null;
  		if (s.equals("猫")) {
  			p=new Cat();
  		}else if (s.equals("狗")) {
  			p=new Dog();
  		}
  		return p;
  	}
  }
  
  public static void main(String[] args) {
  		
  		/*多态第三种应用:用父类作为方法返回值类型,实际任意一个子类对象*/
  		//创建对象
  		Master m2=new Master();
  		//用对象调用方法
  		Pet p= m2.lookPet("猫");
  		p.cry();
  		
  		Pet p2= m2.lookPet("狗");
  		p2.cry();
  		
  	}
  
  ```

  

- 多态的作用:增强程序可维护性;增加程序可扩展性.



### 8.9 向上向下转型

- 向上转型(装箱):将子类对象存在父类或父接口的类型中,叫向上转型.向上转型是自动转换
  		适用场景:所有多态使用地方.		
    		语法: 父类型/父接口 对象名=子类对象.

  ```java
  public static void main(String[] args) {
  		//多态第一种应用:用父类作为数据类型,创建不同子类对象,调用同一种方法,执行不同操作
  		  Pet p1=new Cat();
  		  Pet p2=new Dog();
  		
  		 p1.eat();
  		 p2.eat();
  }
  ```

  

- 向下转型(拆箱):将父类型的对象转换为原本的子类对象,叫向下转型.向下转型有风险的.
  - 适用场景:当用父类作为数据类型创建子类对象,想调用子类独有的方法或属性时,就可以使用向下转型.
  - 语法:子类型 对象名=(子类型)父类型对象;
  - 因为向下转型有风险,是将父类型的对象转换为原来子类对象,如果我们不是很清楚这个父类型的对象原本是什么类型,不方便转换,这时就需要用到类型判断
    - 类型判断的语法:boolean result=对象名 instanceof 子类类型;

```java
public static void main(String[] args) {
		//创建对象,向上转型
		Animal a1=new Rabbit();
		Animal a2=new Tigger();
		
		//用对象调用方法
		//用父类作为数据类型创建的对象,只能调出从父类继承的属性和方法或重写的方法,不能调出子类独有属性和方法
		a1.eat();
		a2.eat();
		
		//因为向下转换,是将父类型的对象转换为原来子类对象,如果我们不是很清楚这个父类型的对象原本是什么类型,
		//不方便转换,这时就需要用到类型判断
		if (a1 instanceof Rabbit) {
			Rabbit r1=(Rabbit)a1;
			r1.jump();
		}else if (a1 instanceof Tigger) {
			Tigger r1=(Tigger)a1;
			r1.climbTree();
		}
	}

```

> 总结：如果一个对象创建后,是用来调用从父类继承的属性或方法,那么这个对象用父类作为数据类型(多态应用);如果一个对象创建后,是用来调用子类独有的方法或属性,那么这个对象用自己的类作为数据类型;如果一个对象创建后,既要调用从父类继承过来的属性和方法,又要调用自己类的属性或方法,那么用父类作数据类型,结合向下转型调用自己类独有的方法.



### 8.10 异常总结

8.10.1:空指针异常(NullPointerException)
         原因:变量值为null,而null调不出任意属性和方法,所以会报NullPointerException
		解决:找出为null值的变量,将变量正常赋值.

8.10.2:类型转换异常(ClassCastException)
	原因:引用类型的变量转换为其他类型时,类型转换有误ClassCastException
	解决:判断变量原本类型,再转换就可.

8.10.3:输入不匹配异常(InputMismatchException)
	原因:从键盘上想接收的数据类型与输入的数据类型不一致,导致InputMismatchException
	解决:接收类型与输入类型一致.

8.10.4:算术异常/0
	原因:除数为0了,违反数学规范.会报ArithmeticException: / by zero
	解决:更改除数不为0;



### 8.11 生成随机数

总语法://生成[min,max]范围内的随机整数

```java
	int result=(int)(Math.random()*(max-min+1)+min);
```

- 案例：

  ```java
  public static void main(String[] args) {
  		//生成[0,1)的随机数
  		double num1=Math.random();
  		 
  		//生成[1,10]的随机整数
  		int num2=(int)(Math.random()*10+1);
  		
  		//生成随机两位整数[10,99],  
  		int num3=(int)(Math.random()*90+10);
  		
  		//生成[min,max]范围内的随机整数
  		//int result=(int)(Math.random()*(max-min+1)+min);
  		
  		//生成[1000,9999]范围内的随机整数
  		int num4=(int)(Math.random()*9000+1000);
  		
  		System.out.print(num4+"\t");
  		
  	}
  
  ```

  

## 九、Java的三大特性

### 9.1 abstract

- abstract：扩展修饰符，抽象的，可以修饰类和方法。

- 抽象类：用abstract修饰的类叫抽象类。

  - 抽象类使用场景：
    - 当一个类创建对象没有任何意义，这个类就可以声明为抽象类；
    - 当一个类中的方法无法确定具体实现时，这个方法就可以定位抽象方法，但是这个类必须为抽象类。

  - 抽象类的特征：
    - 抽象类不能实例化（不能创建对象），但是抽象类有构造方法，其作用是供子类调用。
    - 抽象类中可以有0到多个抽象方法，也可以有0到多个普通方法。
    - 抽象类也可以作为数据类型，指向子类对象。
  - 抽象类的作用：
    - 让子类继承，从而实现代码复用；规定子类必须拥有的行为。

- 抽象方法：用abstract修饰的方法叫抽象方法。

  - 抽象方法应用场景：当一个方法无法确实方法具体体现，这个方法声明为抽象方法
  - 抽象方法的特征：
    - 抽象方法没有方法体，连大括号都没有
    - 抽象方法必须写在抽象类中
    - 抽象方法必须被子类重写，除非子类也是抽象的，就让孙子类去重写
    - 抽象方法不能用private修饰
  - 抽象方法的作用：规定子类必须拥有的行为。



### 9.2 static

- static:扩展修饰符,静态的.用来修饰属性和方法的.

- 静态变量:用static修饰的属性叫静态属性.

  - 静态变量的特征:静态变量属于类,与类共存亡。当前类的所有对象共享这个类的静态变量.
  - 静态变量的优点:可以让这个类的所有对象共享同一个数据.
  - 静态变量的缺点:耗内存.
  - 静态变量的使用语法:
    - 在同一个类中:静态变量名
    - 在不同的类中:类名.静态变量名(推荐) 或 对象名.静态变量名

  - 静态变量的适用场景:当一个类中属性值,需要多个对象共享时,这个属性就可以定为静态变量.

- 静态方法:用static修饰的方法叫静态方法.

  - 静态方法的特征:静态方法属于类.
    - 静态方法中只能直接调用静态的属性和方法,不能直接调用非静态的属性和方法,如果在静态方法中想调用非静态的属性和方法,可以通过对象调用.
    - 在非静态的方法中可以直接调用静态属性和方法,也可以直接调用非静态属性和方法.

  - 静态方法的优点:调用方便(用类名调用方法).
  - 静态方法的缺点:使用受限(静态方法中只能直接调用静态的属性和方法,不能直接调用非静态的属性和方法).
  - 静态方法的使用语法:
    - 在同一个类中:静态方法名([实参列表]);
    - 在不同的类名:类名.静态方法名([实参列表]);  (推荐) 或   对象名.静态方法名([实参列表]);

  - 静态方法的适用场景:当一个类为工具类,那么这个类中方法为了调用方便,全部声明为静态方法.

- 静态代码块:在类加载时执行,一生只执行一次

  - 作用:在类加载时初始化静态变量.

  - 语法:static {

    }

  - 适用场景:如果静态属性在项目运行过程中使用频繁,就可用静态代码块初始化.

- 动态代码块:在类加载时加载,一生只执行一次.

  - 适用场景:任何情况下可用.
  - 语法:{
    	
    }

  - 作用:在类加载时初始化变量.能用动态代码块解决的问题都可以用构造方法解决.

- 类的加载顺序:类加载时,先加载静态属性,再加载静态代码块,再加载成员变量,再加载动态代码块,再加载构造方法.

- 学生类：

```java
public class Student {
	/**
	 * 成员变量
	 */
	public String sname="aa1";
	/**
	 * 静态变量
	 */
	public static String school="千锋1";
	
	/**
	 * 静态代码块
	 */
	static {
		//静态块中只能直接调用静态的属性和方法,不能直接调用非静态属性和方法
		//sname="";
		school="千锋2";
		//show3();
		//show4();
	}
	
	/**
	 * 动态代码块
	 */
	{
		sname="aa2";
		school="千锋3";
	}
	
	/**
	 * 普通方法
	 */
	public void show1() {
		//在普通方法中既可以调用成员变量,也可以调用静态变量
		System.out.println("静态变量:"+school);
		System.out.println("普通变量:"+sname);
		//在普通方法中既可以调用成员方法,也可以调用静态方法
		show3();
		show4();
	}
	
	/**
	 * 静态方法
	 */
	public static void show2() {
		/*在静态方法中只能直接调用静态变量,不能直接调用非静态变量*/
		System.out.println("静态变量:"+school);
		//System.out.println("普通变量:"+sname);
		
		/*在静态方法中只能直接调用静态方法,不能直接调用非静态方法*/
		//show3();
		show4();
		
		/*在静态方法可以通过对象调用非静态的属性和方法*/
		//创建对象
		Student stu1=new Student();
		System.out.println(stu1.sname);
		stu1.show3();
	}
	
	/**
	 * 普通方法
	 */
	public void show3() {
		System.out.println("这是一个普通方法");
	}
	
	/**
	 * 静态方法
	 */
	public static void show4() {
		System.out.println("这是一个静态方法");
	}
}

```

- 测试类：

```java
public class Test2 {

	public static void main(String[] args) {
		
		//创建对象
//		Student stu1=new Student();
//		//用对象调用属性
//		stu1.sname="小明";
//		//静态属性既可以用对象调用,也可以用类名调用
//		//stu1.school="千锋";
//		Student.school="千锋";
//		
//		//静态方法既可以用类名调用,也可以用对象名调用
//		Student.show2();
		//stu1.show2();
		
		//创建对象
		Student stu2=new Student();
//		System.out.println("姓名为:"+stu1.sname+",学校为:"+stu1.school);
		System.out.println("姓名为:"+stu2.sname+",学校为:"+stu2.school);
	}

}

```



### 9.3 final

- final:扩展修饰符,最终的.用来修饰类,变量,方法.
- 最终类:用final修饰的类叫最终类,不能被继承.
- 最终方法:用final修饰的方法叫最终方法,不能被重写.
- 常量:用final修饰的变量叫常量.常量一生只可以赋一次值,一但赋值不可更改.
  - 成员常量:在类中直接声明常量叫成员常量.成员常量可以在声明时赋值,或在构造方法中赋值或动态代码块中赋值.
  - 局部常量:在方法中直接声明常量叫局部常量. 局部常量可以在声明时给值,也可以先声明再赋值.



### 9.4 总结

static，final，abstract总结 ：

- static和final可以同时用来修饰属性和方法.
- static和abstract不能同时使用.
- final和abstract不能同时使用.

![image-20210420174611641](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210420174611641.png)



## 十、接口

### 10.1 接口的概念

接口:是一种特殊抽象类

- 接口定义:表示一种扩展功能,一种约定,一种规范.

- 声明接口关键字:interface

- 实现接口关键字:implements

- 接口特点:

  - 接口中方法默认全是抽象方法，所以接口中的方法默认系统会加public abstract修饰
  - 接口中的变量全是静态变量，所以接口中变量默认系统会加public static final
  - 接口不能实例化，接口中没有构造方法
  - 接口中抽象方法必须被子类实现（重写），除非子类也是抽象的，让孙子类去实现
  - 类与类之间是继承的关系，类与接口之间是实现的关系,接口与接口之间是继承的关系.一个类只能直接继承一个父类,一个类可以实现多个接口,一个接口可以继承多个接口.
  - 一个类只能直接继承一个父类,但是一个类可以实现多个接口,所以从某种程序上来说,接口弥补Java单继承的缺陷.
  - 接口中默认的方法全是抽象方法,但在jdk1.8之后,接口中还可以有静态方法和扩展方法.接口中静态方法供子类调用,不能继承或重写.接口中扩展方法,可以被子类继承或重写.
  - 接口是一种引用数据类型,与类同级别.

  ```java
  /**
  	 * 接口中可以声明静态方法
  	 */
  	public static void show1() {
  		System.out.println("这是游泳接口中静态方法");
  	}
  	
  	/**
  	 * 接口中扩展方法
  	 */
  	default void show2() {
  		System.out.println("这是游泳接口中扩展方法");
  	}
  
  ```

- 接口作用:提高程序可扩展性和维护性.



### 10.2 接口的分类

- 普通接口:接口可以声明抽象方法或静态常量.
- 常量群接口:接口中全是静态常量.
- 标志性接口:接口中没有任何东西,实现这种就表示具备某种功能.eg:Serializable  



### 10.3 抽象类 VS 接口

- 相同点
  - 都不能实例化（创建对象）
  - 都可以声明抽象方法和静态常量
  - 都是一种引用数据类型
  - 它们的抽象方法都必须别重写，除非子类也是抽象的，被孙子类重写
  - 都可以编译之后生成.class文件
  - 都与自己同类型之间是继承关系



- 不同点
  - 作用不同:抽象类的作用让子类去继承,从而实现代码复用及规定子类必须拥有的行为;接口作用提高程序可扩展性和可维护性.
  - 构造不同:抽象类中有构造方法,它的构造方法供子类调用;接口中没有构造方法.
  - 方法不同:抽象类中可以有任何方法;接口中默认全是抽象方法,在jdk1.8后接口中还可有扩展方法和静态方法.
  - 静态常量不同:抽象类中可以有成员变量,静态常量,静态变量;接口中只能有静态常量.
  - 继承和实现不同:一个类只能继承一个抽象类,一个类可以实现多个接口,一个接口也可以继承多个接口.
  - 修饰符不同:抽象类中抽象方法必须用abstract修饰;接口中抽象方法可以不用abstract修饰,系统默认用public abstract修饰.
  - 代码块不同:抽象类中可以用静态代码块和动态代码块;接口不可用静态代码块和动态代码块



### 10.4 (扩展)JDK1.8后

- JDK1.8后,接口中可以静态方法和扩展(默认)方法.
- 接口静态方法只能调用不能继承,提高接口使用灵活性.
- 接口扩展方法可以让子类继承,提高程序可扩展性.
- 当一个类的父类与父接口具有相同的方法时,子类继承的父类的方法(类优先于接口)
- 当一个类的两个父接口中具有相同的方法时,子类实现这两个父接口后会报错,让子类重写这个相同的方法就可解决冲突.



## 十一、内存分析

### 11.1 内存划分

- Java中内存划分:
  - 栈:存放局部变量和栈帧(main()),使用效率最高
  - 堆:存放数组或对象等.
  - 方法区:存放.class文件,静态变量,常量池.使用效率最低.  



### 11.2 一个对象内存分析:

```java
public static void main(String[] args) {
		//创建对象
		Student stu1=new Student();
		//用对象调用方法给属性赋值
		stu1.setSage(11);
		stu1.setSname("小花");
		
		System.out.println("姓名为:"+stu1.getSname()+",年龄为:"+stu1.getSage());
}
```



![image-20210421203045246](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210421203045246.png)



### 11.3 多个对象内存分析

```java
public static void main(String[] args) {
		//创建对象
		Teacher t1=new Teacher();
		//用对象调用方法给属性赋值
		t1.setTname("安静");
		t1.setTage(20);
		
		System.out.println("姓名为:"+t1.getTname()+",年龄为:"+t1.getTage());
		
		//创建对象
		Teacher t2=new Teacher();
		//用对象调用方法给属性赋值
		t2.setTname("张宇延");
		t2.setTage(25);
		System.out.println("姓名为:"+t2.getTname()+",年龄为:"+t2.getTage());
	}

```

![image-20210422195708567](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210422195708567.png)



### 11.4 值传递与引用传递

- 值传递:方法的形参是基本数据类型叫值传递.值传递传的是参数的值,在方法中对值作更改,方法中的值确实改变,但方法执行完后,原参数的值是不变.

  ```java
  public class Change {
  	/**
  	 * 实现两个数互换
  	 * @param num1
  	 * @param num2
  	 */
  	public void changeNum(int num1,int num2) {//num1=a,num2=b
  		int temp=num1;
  		num1=num2;
  		num2=temp;
  		System.out.println("交换中,num1="+num1+",num2="+num2);
  	}
  }  
  
  		public static void main(String[] args) {
  		//声明两个变量
  		int a=10;
  		int b=8;
  		System.out.println("交换前,a="+a+",b="+b);
  		
  		//创建对象
  		Change c=new Change();
  		//用对象调用方法实现两个变量相互交换
  		c.changeNum(a, b);
  		System.out.println("交换后,a="+a+",b="+b);
  	}
  
  ```

  

![image-20210422200036465](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210422200036465.png)



- 引用传递:方法的参数是引用数据类型叫引用传递.引用传递传的是参数的内存地址,在方法中和方法执行完后,参数的值确实改变.

  ```java
  public class Change {	
  	/**
  	 * 改变对象的属性值
  	 * @param t
  	 */
  	public void changeTeacher(Teacher t) {//t=t1
  		t.setTname("bb");
  		t.setTage(66);
  		System.out.println("改变中,姓名为:"+t.getTname()+",年龄为:"+t.getTage());
  	}
  }
  
  public static void main(String[] args) {
  		//声明对象
  		Teacher t1=new Teacher();
  		//调用对象的方法赋值
  		t1.setTname("aa");
  		t1.setTage(18);
  		
  		System.out.println("改变前,姓名为:"+t1.getTname()+",年龄为:"+t1.getTage());
  		
  		//创建对象
  		Change c=new Change();
  		//调用方法改变变量的值
  		c.changeTeacher(t1);
  		System.out.println("改变后,姓名为:"+t1.getTname()+",年龄为:"+t1.getTage());
  }
  
  
  ```

  

![image-20210422200310378](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210422200310378.png)



### 11.5 对象数组

- 对象数组:本质还是一维数组.数组的每个空间存对象(对象内存地址).
- 注意:对象数组使用时遵循两套原则,整体是一个一维数组遵循数组使用原则;对象数组每个空间存对象,所以遵循对象使用原则.

```java
public static void main(String[] args) {
		//声明对象数组:整体是一个一维数组,每个空间存的是一个对象.整体使用遵循数组的使用原则,数组的每个空间是一个对象,遵循对象使用原则
		//int[] nums1=new int[3]; 
		SuperStar[] star3=new SuperStar[3];
		
		//给对象数组动态赋值,数组的每个空间是一个对象,遵循对象使用原则
		//第一种:先用无参构造给对象数组的每个空间初始化,再用对象调用属性存值
		star3[0]=new SuperStar();
		star3[0].name="张一";
		star3[0].age=18;
		
		//第二种:用全参构造对对象数组的每个空间初始化时,顺便给属性赋值
		star3[1]=new SuperStar("热巴", 30);
		
		star3[2]=new SuperStar("肉丝", 23);
		
		//遍历对象数组
		for (int i = 0; i < star3.length; i++) {
			System.out.println(star3[i].name+","+star3[i].age);
		}
	}

```

![image-20210422200730802](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210422200730802.png)



## 十二、常用类

### 12.1 内部类

- 内部类:在一个类的大括号里面再声明的类叫内部类。

- 内部类的分类：成员实例内部类,成员静态内部类,局部内部类.

  注意：成员实例内部类和成员静态内部类必须用访问修饰符,局部内部类不可以用访问修饰符.



#### 12.1.1 成员实例内部类

- 成员实例内部类：
  - 在成员实例内部类中可以直接使用外部类的属性,方法.
  - 外部类不能直接调用内部类属性和方法,但是可以通过内部类的对象调用
  - 当外部类与成员实例内部的属性同名时,在内部类中输出内部类中同名属性.
     在内部类中调用外部类中同名属性,用外部类的对象.属性名;

```java
public class Outer1 {
	/**
	 * 外部类成员变量
	 */
	public int a=1;
	
	/**
	 * 外部类方法
	 * @param num1
	 * @param num2
	 * @return double
	 */
	public double add1(double num1,double num2) {
		//外部类不能直接调用内部类属性和方法,但是可以通过内部类的对象调用
		Inner1 in1=new Inner1();
		System.out.println(in1.b);
		double result=in1.add2(num1,num2);
		return result;
	}
	
	public void show1() {
		System.out.println("这是外部类的普通方法");
	}
	
	/**
	 * 成员实例内部类
	 * @author sx
	 * @version 2021年4月22日
	 */
	public class Inner1{
		/**
		 * 内部类属性
		 */
		public int b;
		public int a=2;
		
		/**
		 * 内部类的方法
		 * @param num1
		 * @param num2
		 * @return double
		 */
		public double add2(double num1,double num2) {
			return num1+num2;
		}
		
		/**
		 * 内部类的方法
		 */
		public void show3() {
			//在成员实例内部类中可以直接使用外部类的属性,方法
//			System.out.println(a);
//			show1();
			
			//当外部类与成员实例内部的属性同名时,在内部类中输出内部类中同名属性.
			System.out.println(a);//2
			//当外部类与成员实例内部的属性同名时,在内部类中调用外部类中同名属性
			System.out.println(Outer1.this.a);//1
			System.out.println(new Outer1().a);//1
		}
	}
}

public static void main(String[] args) {
		//创建外部类对象
		Outer1 out1=new Outer1();
		//double result= out1.add1(11, 22);
		//System.out.println("两数之和为:"+result);
		
		//创建成员实例内部类对象
		//Outer1.Inner1 in1=new Outer1().new Inner1();
		Outer1.Inner1 in1=out1.new Inner1();
		
		//用对象调用属性或方法
//		System.out.println(in1.b);
//		double result2= in1.add2(33, 44);
//		System.out.println("计算之和为:"+result2);
		
		in1.show3();
	}


```



#### 12.1.2 成员静态内部类

- 成员静态内部类：
  - 在成员静态内部类中只能直接调用外部类的静态属性和方法,不能直接调用外部类的非静态属性和方法,如果想调用可以用对象调用.
  - 在外部类中可以用类名直接调用成员静态内部类中静态属性和方法,不能调用非静态属性和方法,如果想调用可以用对象调用

```java
public class Outer2 {
	public int a;
	public static int b;
	
	public void show1() {
		System.out.println("这是外部类的实例方法");
		
		//在外部类中可以用类名直接调用成员静态内部类中静态属性和方法,不能调用非静态属性和方法,如果想调用可以用对象调用
		//System.out.println(new Inner2().c);
		System.out.println(Inner2.d);
		//new Inner2().show3();
		Inner2.show4();
		
	}
	public static void show2() {
		System.out.println("这是外部类的静态方法");
	}
	
	/**
	 * 成员静态内部类
	 * @author sx
	 * @version 2021年4月22日
	 */
	public static class Inner2{
		public int c;
		public static int d;
		
		public void show3() {
			System.out.println("这是内部类的实例方法");
			//在成员静态内部类中只能直接调用外部类的静态属性和方法,不能直接调用外部类的非静态属性和方法,如果想调用可以用对象调用
			//System.out.println("a="+a);
			System.out.println("b="+b);
			//show1();
			show2();
		}
		public static void show4() {
			System.out.println("这是内部类的静态方法");
			//System.out.println("a="+a);
			System.out.println("b="+b);
			//show1();
			show2();
		}
	}
}
	
	public static void main(String[] args) {
		//创建外部类对象
		Outer2 out2=new Outer2();
		//out2.show1();
		
		//创建成员静态内部类对象
		Outer2.Inner2 in2=new Outer2.Inner2();
		//用对象调用属性或方法
		System.out.println(in2.c);
		System.out.println(in2.d);
		in2.show3();
		in2.show4();
	}

```



#### 12.1.3 局部内部类

##### 12.1.3.1 普通局部内部类

- 普通局部内部类（一般很少用）:在类中的方法里面声明的类.

```java
/**
	 * 外部类的方法
	 */
	public void show1() {
		/**
		 * 局部内部类
		 * @author sx
		 * @version 2021年4月22日
		 */
		class Inner3{
			public int b;
			public void show2() {
				System.out.println("这是局部内部类的方法");
			}
		}
		
		//创建局部内部类对象
		Inner3 in3=new Inner3();
		//用对象调用属性和方法
		System.out.println(in3.b);
		in3.show2();
	}

```



##### 12.1.3.2 匿名内部类

- 匿名内部类：在方法中声明的类，且这个类没有类名叫匿名内部类。

- 适用场景：在一个类一生只需要一个对象，且这个对象一生只使用一次就可以使用匿名内部类。

- 使用语法：父接口或父抽象类 对象名  = new  父接口或父抽象类(){

  访问修饰符 数据类型 变量名1;
  					访问修饰符 数据类型 变量名2;
  					...
  					访问修饰符 返回值类型 方法名1(形参列表){

  ​					}

  ​					...

  }

> 注意:匿名内部类一定要有父接口或父抽象类.

```java
public interface Iswimming {
	/**
	 * 抽象游泳的方法
	 */
	public void swimming();
}

public static void main(String[] args) {
		/*第一种:先创建匿名内部类对象,再使用*/
		//创建匿名内部类对象
		//{}部分就是匿名内部类,因为匿名内部类一生只有一个对象,所以只能在声明同时创建对象new 类名(),
		//又因为匿名内部类没有类名,所以用父接口或父抽象类作为数据类型创建对象 new 父接口(){匿名内部类的类体}
		Iswimming stu1=new Iswimming(){
			
							/**
							 * 实现父接口中游泳的方法
							 */
							@Override
							public void swimming() {
								System.out.println("学生在知识海洋里游泳");
							}

						};
		//用匿名内部类对象调用方法
		stu1.swimming();
		System.out.println("----------------------------");
		
		/*第二种:创建匿名内部类的对象的同时使用调用方法*/
		new Iswimming(){
			
			/**
			 * 实现父接口中游泳的方法
			 */
			@Override
			public void swimming() {
				System.out.println("学生在知识海洋里游泳");
			}

		}.swimming();
	}

```

> 一个Java类对应一个.class字节码文件：
> 	成员内部类命名：外部类名$内部类名.class
> 	局部内部类命名：外部类名$编号内部类名.class
> 	匿名内部类命名：外部类名$编号.class



### 12.2 object类

- Object类:是所有Java类的根类,基类,超类.所有Java类都直接或间接继承Object类.

  - finalize():标记对象为垃圾对象,让垃圾对象在回收队列进行排队等待回收.
  - getClass():获得当前对象的.class文件对象,一个类只有一个.class文件对象.
    				 注意:用它可以实现判断两个对象是否同一个类型的.	

  - hashCode():如果对象所在的类中没有重写hashCode(),通过对象的内存地址经过一系列运算得到哈希码值,如果对象内存地址不同,得到哈希码值不同,如果对象内存地址相同,得到哈希码值相同;如果对象所在的类中重写hashCode(),根据对象的值计算哈希码值,这时只要对象内存地址相同或值相同得到哈希码值相同.

  - toString():如果当前对象是直接继承Object类的toString(),自己没有重写,那么得到的是对象内存地址字符串形式;如果当前对象所在的类中重写Object类的toString(),那么调用toString()输出对象的属性值.
    注意:System.out.print()和System.out.println()输出的变量是引用数据类型会自动调用变量的toString();

  ```java
  public static void main(String[] args) {
  		//创建对象
  		Student stu1=new Student("aa", 11);
  		Student stu2=new Student();
  		Student stu3=stu1;
  		
  		//判断两个对象是否同一个类的对象
  		System.out.println(stu1.getClass()==stu2.getClass());//true
  		
  		//同一个内存地址得到哈希码值相同,不同内存地址得到哈希码值不同
  		System.out.println(stu1.hashCode()==stu2.hashCode());//false
  		System.out.println(stu1.hashCode()==stu3.hashCode());//true
  		
  		System.out.println(stu1.toString());
  		System.out.println(stu1);
  		
  	}
  
  ```

  

- == VS equals()都可以比较变量

  - ==:==左右两边如果是基本数据类型,比较的是变量值;==左右两边如果是引用数据类型,比较的是变量的内存地址.

  - equals():如果equals()左右两边变量所在的类中,没有重写Object继承过来的equals(),比较是变量内存地址(效果等同于==);如果equals()左右两边变量所在的类中,重写Object继承过来的equals(),比较的是变量值.	

  - 注意:因为String类底层重写equals(),所以String类型的变量调用equals()比的是值.

    ```java
    public static void main(String[] args) {
    		Student stu1=new Student("张三", 18);
    		Student stu2=new Student("张三", 18);
    		int num1=11;
    		int num2=11;
    		//因为==左右是基本数据类型,比值
    		System.out.println(num1==num2);//true
    		//因为==左右是引用数据类型,比地址
    		System.out.println(stu1==stu2);//false
    		//如果stu1和stu2所在类Student中没有重写equals(),比地址,重写了就比值
    		System.out.println(stu1.equals(stu2));
    	}
    
    ```

    

### 12.3 包装类

- 八种基本数据类型违反了Java是一种纯面向对象的语言.所以Java为了保证自己是一种纯面向对象的语言给八种基本数据类型提供包装类.

  包装类:将基本数据类型封装成类,叫包装类.
  		基本数据类型     包装类
  			byte			java.lang.Byte 
  			short		java.lang.Short 
  			int			java.lang.Integer
  			long			java.lang.Long
  			float		java.lang.Float
  			double       java.lang.Double       
  			char			java.lang.Character 
  			boolean       java.lang.Boolean

- 八种基本数据类型的包装类都是引用数据类型.
- 以后成员变量的数据类型建议用包装类作为数据类型,原因是包装类型的变量的默认值为null,方便判断变量;包装类型变量可以调用其他方法,方便后续处理.

- 基本数据类型和包装类的相互转换
  - 装箱:将基本数据类型转换包装类
  - 拆箱:将包装类转换为基本数据类型
  - 在jdk1.5之后,Java支持自动装箱拆箱.

```java
public static void main(String[] args) {
		int num1=11;
		Integer num2=new Integer(22);
		//拆箱:将integer转换为int
		int num3=num2.intValue();
		
		//装箱:将int转换为integer
		Integer num4=Integer.valueOf(num1);

		/*在jdk1.5之后,Java支持自动装箱拆箱.*/
		//自动装箱
		Integer num5=33;
		//自动拆箱
		int num6=num2;
		
		System.out.println(num3+","+num4);
}
```

- Integer整数缓冲区:Integer类中封装了一个私有的静态内部类IntegerCache，该类中又定义了一个Integer cache[]的缓冲区，大小其实就是区间[-128, 127]的大小，该区间内的数已经通过实例化操作将各自对应的Integer对象封装在了数组cache中，
  即Integer cache[0] = new Integer(-128);依次初始化到数字127结束。
  (设置整数缓冲区的原因,主要是因为缓冲区的数据在平时是最常用的,多次使用相同的底层对象可以有助于提高底层的优化)
  注意:==左右两边有一边为基本数据类型,另一边引用类型的变量会自动调用方法转换为基本数据类型,比值.

![image-20210423190902499](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210423190902499.png)

```java
public static void main(String[] args) {
		Integer num1=new Integer(100);
		Integer num2=new Integer(100);
		Integer num3=100;
		Integer num4=100;
		int num5=100;
		int num6=100;
		
		//比地址
		System.out.println(num1==num2);//false
		//比地址
		System.out.println(num3==num4);//true
		//比值
		System.out.println(num5==num6);//true
		//比地址
		System.out.println(num1==num3);//false
		//==左右有一边为基本数据类型,比值
		//(==左右有一边为基本数据类型,另一边引用数据会自动调用方法转换基本数据类型)
		System.out.println(num1==num5);//true
		
		
		System.out.println("---------------------------");
		Integer num11=new Integer(200);
		Integer num12=new Integer(200);
		Integer num13=200;
		Integer num14=200;
		int num15=200;
		int num16=200;
		//比地址
		System.out.println(num11==num12);//false
		//比地址
		System.out.println(num13==num14);//false
		//比值
		System.out.println(num15==num16);//true
		//比地址
		System.out.println(num11==num13);//false
		//==左右两边有一边基本数据类型,比值
		System.out.println(num11==num15);//true
	}


```



### 12.4 String类

- String类:是最终的类,一但赋值不可更改.

  注意:String有个常量池,	常量池中值不可重复.常量指的就是固定值.

  - 因为String类底层重写equals(),所以String调用equals()永远比较是值.又因为String类调用==,比较内存地址.  

    ```java
    public static void main(String[] args) {
    		String s1=new String("abc");
    		String s2=new String("abc");
    		String s3="abc";
    		String s4="abc";
    		//下面全部比内存地址
    		System.out.println(s1==s2);//false
    		System.out.println(s3==s4);//true
    		System.out.println(s1==s3);//false
    	}
    ```




- String字符串的拼接

  - 常量与常量的拼接结果在常量池。且常量池中不会存在相同内容的常量。
  - 只要其中有一个是变量，结果就会在堆中。
  - 如果拼接的结果调用intern()方法，返回值就在常量池中。

  ```java
  public class StringTest03 {
      public static void main(String[] args) {
          String s1 = "JavaEEhadoop";
          String s2 = "JavaEE";
          String s3 = s2+"hadoop";
          System.out.println(s1 == s3);
  
          final String s4 = "JavaEE";//final是常量
          String s5 = s4+"hadoop";
          System.out.println(s1 == s5);
      }
  }
  ```



![image-20210423191106676](C:\Users\51739\AppData\Roaming\Typora\typora-user-images\image-20210423191106676.png)



- 其他数据类型转换为String的方法
  - 其他数据类型的变量+"",将其他类型转换为String
  - String.valueOf(Object obj) ,将其他类型转换为String
  - 其他数据类型的对象.toString(),将其他类型转换为String
  - Arrays.toString(一维数组名),将数组转换为String
  - String类的构造方法可以将byte[],char[],StringBuffer,StringBuilder转换为String类型

```java
public static void main(String[] args) {
		//1.其他数据类型的变量+"",将其他类型转换为String
		String s1=true+"";
		
		//2.String.valueOf(Object obj) ,将其他类型转换为String
		String s2=String.valueOf(3.14);
		
		//3.其他数据类型的对象.toString(),将其他类型转换为String
		Integer num1=11;
		String s3=num1.toString();
		
		//4.Arrays.toString(一维数组名),将数组转换为String
		int[] nums= {1,2,3,4,5};
		String s4=Arrays.toString(nums);
		
		//5.String类的构造方法可以将byte[],char[],StringBuffer,StringBuilder转换为String类型
		char[] cs= {'又','高','又','帅'};
		String s5=new String(cs);
		
		System.out.println(s5);
	}

```



- String类型转换为其他数据类型,注意转换有风险.
  - 用其他类型构造方法将String类型转换其他类型,除了Character类型
  - 其他类型.valueOf(String s),除了Character类型
  - 其他类型.parse数据类型(String s),除了Character类型

```java
public static void main(String[] args) {		
		//2.1:用其他类型构造方法,将字符串转换为其他类型
		String s6="11";
		Integer num2=new Integer(s6);
		
		//2.2:其他类型.valueOf(String s),除了Character类型
		Integer num3=Integer.valueOf(s6);
		
		//2.3:其他类型.parse数据类型(String s),除了Character类型
		Integer num4=Integer.parseInt(s6);
		System.out.println(num4);
    
    	//String转char[]
    	String str1 = "abc123"; 
    	char[] charArray = str1.toCharArray();
    	for(int i = 0;i < charArray.length;i++){
            System.out.println(charArray[i]);
        }
    
		//String转byte[]
    	String str1 = "abc123中国";
        byte[] bytes = str1.getBytes();//使用默认的字符集，进行编码
        System.out.println(Arrays.toString(bytes));
    
    	String str2 = new String(bytes);//使用默认的字符集，进行解码。
    	System.out.println(str2);
    	
}
```



- "" VS null:""表示开辟空间,空间没存值;null表示没有开辟空间.

  ```java
  //声明变量,开辟空间,只是空间上没存值.
  		String s7="";
  		//声明变量,没有开辟空间
  		String s8=null;
  ```



- String类的常用方法:

  ```java
  public static void main(String[] args) {
  		//声明一个字符串
  		String s1="我是千锋人,我爱千锋";
  		
  		//1.charAt(int index)返回指定索引处的字符值。 
  		char c1=s1.charAt(4);
  		
  		//2.compareTo(String anotherString) 按字典顺序比较两个字符串。如果字符串在参数字符串前面返回负数,在后面返回正数,相同返回0
  		int num1="F".compareTo("f");
  		
  		//3.compareToIgnoreCase(String str) 按字典顺序比较两个字符串，忽略大小写.
  		int num2="F".compareToIgnoreCase("f");
  		
  		//4.concat(String str) 将指定的字符串连接到该字符串的末尾,产生新的字符串。 
  		String s2=s1.concat("i like china");
  		
  		//5.contains(CharSequence s) 当且仅当此字符串包含指定的char值序列时才返回true。
  		boolean result1=s1.contains("千锋");
  		
  		//6.endsWith(String suffix) 测试此字符串是否以指定的后缀结尾。
  		boolean result2="hello.java".endsWith(".java");
  		
  		//7.startsWith(String prefix) 测试此字符串是否以指定的前缀开头。
  		boolean result3="42112145454545545".startsWith("42");
  		
  		//8.equals(Object anObject) 将此字符串与指定对象进行比较。
  		//9.equalsIgnoreCase(String anotherString) 将此 String与其他 String比较，忽略大小写。
  		boolean result4="abEK".equalsIgnoreCase("abek");	
  		
  		//10.format(String format, Object... args) 使用指定的格式字符串和参数返回格式化的字符串。
  		String s3=String.format("%.2f+%.2f=%.2f", 3.14232323,4.12434343,(3.14232323+4.12434343));
  		String s4=String.format("%.2f", 3.23232323232);
  		
  		//11.indexOf(String str) 返回指定子字符串第一次出现的字符串内的索引。 
  		int index1=s1.indexOf("千锋");
  		
  		//12.lastIndexOf(String str) 返回指定子字符串最后一次出现的字符串中的索引。
  		int index2=s1.lastIndexOf("千锋");
  		
  		//13.join(String 分隔符, CharSequence... elements) 将多个字符串按照指定分隔符拼接成一个新的字符串
  		String s5=String.join("-","哈哈", "呵呵呵","嘻嘻");
  		
  		//14.length() 返回此字符串的长度。 
  		int num3=s1.length();
  		
  		//15.matches(String regex) 告诉这个字符串是否匹配给定的 regular expression 
  		boolean reuslt5="abc".matches("abc");//true
  		
  		//16.replace(String oldChar, String newChar) 返回从替换所有出现的导致一个字符串 oldChar在此字符串 newChar 。
  		String s6="这是一本暴力的小说".replace("暴力", "**");
  		
  		//17.split(String regex) 将此字符串分割为给定的 regular expression的匹配
  		String[] s7="1,2,3,4,5".split(",");
  		
  //		for (String s : s7) {
  //			System.out.println(s);
  //		}
  		
  		//18.substring(int beginIndex, int endIndex) 返回一个字符串，该字符串是此字符串的子字符串。包头不包尾
  		String s8=s1.substring(2, 5);
  		
  		//19.toLowerCase() 将所有在此字符 String使用默认语言环境的规则，以小写。 
  		String s9="abdCDEfere".toLowerCase();
  		
  		//20.toUpperCase() 将所有在此字符 String使用默认语言环境的规则大写。 
  		String s10="abdCDEfere".toUpperCase();
  		
  		//21.trim() 返回一个字符串，其值为此字符串，并删除任何前导和尾随空格。 
  		String s11="  abcd def   ".trim();
  		
  		System.out.println(s11);
  	}
  
  ```

  

### 12.5 StringBuffer、StringBuilder

- StringBuffer：是最终的，线程安全，可变字符序列
- StringBuilder：是最终的，在单线程中使用效率高，多线程中不安全的可变字符序列

> 注意：StringBuffer和StringBuilder它们常用方法相同。

```java
public static void main(String[] args) {
		//创建一个StringBuilder对象
		StringBuilder sb1=new StringBuilder();
		
		//1.append(Object obj) 追加 Object参数的字符串 Object形式
		sb1.append("我是中国人");
		sb1.append("我爱中国");
		
		//2.charAt(int index) 返回 char在指定索引在这个序列值。 
		char c2=sb1.charAt(4);
		
		//3.delete(int start, int end) 删除此序列的子字符串中的字符。 
		sb1.delete(2, 5);
		
		//4.insert(int offset, Object obj) 将 Object参数的字符串表示插入到此字符序列中。 
		sb1.insert(2, "千锋人");
		
		//5.replace(int start, int end, String str) 用指定的String中的字符替换此序列的子字符串中的 String 。 
		sb1.replace(2, 5, "中国人");
		
		//6.reverse() 导致该字符序列被序列的相反代替。
		sb1.reverse();
		
		//7.substring(int start, int end) 返回一个新的 String ，其中包含此序列中当前包含的字符的子序列。 
		String sb2=sb1.substring(4, 5);
		
		//8.toString() 返回表示此顺序中的数据的字符串。 
		String sb3=sb1.toString();
		
		
		System.out.println(sb3);
	}

```



### 12.6 String VS StringBuffer VS StringBuilder

相同点:
		3.1.1:都是最终类.
		3.1.2:都是引用数据类型.
		3.1.3:都可以存字符串.
		3.1.4:底层都是用char[]存值.

不同点:
		String是不可变的最终类,一但赋值,空间不可更改.
		StringBuffer是可变的最终类,在多线程中使用安全,在单线程中效率低.
		StringBuilder是可变的最终类,在多线程中使用不安全,在单线程中效率高.



### 12.7 BigDecimal

- BigDecimal类:精确计算浮点数.
- 为什么要用BigDecimal，因为使用double进行运算，结果不精确。

```java
public static void main(String[] args) {
		double num1=1.0;
		double num2=0.9;
		double result1=num1-num2;
		System.out.println(result1);
	}
```



- BigDecimal类的常用方法

```java
public static void main(String[] args) {
		BigDecimal num1=new BigDecimal(10.0);
		BigDecimal num2=new BigDecimal(3.0);
		//计算两数之和
		BigDecimal result1=num1.add(num2);
		//计算两数之差
		BigDecimal result2=num1.subtract(num2);
		//计算两数之积
		BigDecimal result3=num1.multiply(num2);
		//计算两数之商,BigDecimal如果除不断会报错
		//BigDecimal result4=num1.divide(num2);
		//第一个参数是除数,第二个参数是保留的小数位数,第三个参数是取舍模式(舍入模式向零舍入)
		BigDecimal result4=num1.divide(num2,2,BigDecimal.ROUND_DOWN);
		
		System.out.println("两数之和为:"+result1);
		System.out.println("两数之差为:"+result2);
		System.out.println("两数之积为:"+result3);
		System.out.println("两数之和商:"+result4);
	}
```



### 12.8 Date、SimpleDateFormat

- java.util.Date类:日期类

```java
public static void main(String[] args) {
		//获得当前系统日期
		Date today=new Date();
		System.out.println("当前系统日期为:"+today);
		System.out.println("获得当前系统时间毫秒数:"+today.getTime());
		
		//获得其他日期
		Date d2=new Date(1000);
		System.out.println("时间2为:"+d2);
		
		//比较两个日期,日期在参数日期之前返回负数,之后返回正数,相等返回0
		int result1=d2.compareTo(today);
		System.out.println(result1);
	}

```



- java.text.SimpleDateFormat:将日期与String之间进行相互转换工具类.
  - 将日期转换为字符串:format(Date date) 
  - 将字符串转换日期:parse(String source) 

```java
public static void main(String[] args) throws ParseException {
		//获得当前系统日期
		Date today=new Date();
		System.out.println("当前系统日期为:"+today);
				
		//创建日期格式化对象
		SimpleDateFormat sdf=new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
		//将系统日期转换为指定格式字符串
		String s1=sdf.format(today);
		System.out.println("当前系统日期格式化为:"+s1);
		
		//将字符串转换为日期,有风险,字符串必须符合格式化对象中指定格式
		Date d3=sdf.parse("2021-04-25 11:10:19");
		System.out.println("d3为:"+d3);
	}
```



### 12.9 Calendar

- java.util.Calendar:日期类.

```java
public static void main(String[] args) {
		//用父抽象类作为数据类型,调用静态方法得到子类对象
		Calendar c1=Calendar.getInstance();
		System.out.println(c1);
		System.out.println("年:"+c1.get(Calendar.YEAR));
		//设置月份
		//c1.set(Calendar.MONTH, 4);
		System.out.println("月:"+(c1.get(Calendar.MONTH)+1));
		System.out.println("日:"+c1.get(Calendar.DAY_OF_MONTH));
		System.out.println("时:"+c1.get(Calendar.HOUR));
		System.out.println("分:"+c1.get(Calendar.MINUTE));
		System.out.println("秒:"+c1.get(Calendar.SECOND));
		
		//当前月中最大日
		System.out.println(c1.getActualMaximum(Calendar.DAY_OF_MONTH));
		//当前月中最小日
		System.out.println(c1.getActualMinimum(Calendar.DAY_OF_MONTH));
		//所有月中最大日
		System.out.println(c1.getMaximum(Calendar.DAY_OF_MONTH));
		//所有月中最小日
		System.out.println(c1.getMinimum(Calendar.DAY_OF_MONTH));
	}

```



### 12.10 System

- java.lang.System:系统类

```java
public static void main(String[] args) {
		Scanner input=new Scanner(System.in);
		
		System.out.println("我是千锋人");
		System.err.println("错误输出");
		
		//退出jvm
		System.exit(0);
		
		System.out.println("系统时间毫秒数:"+System.currentTimeMillis());
		System.out.println("系统时间纳秒数:"+System.nanoTime());
		System.out.println("系统配置:"+System.getProperties());
		System.out.println("Java安装目录:"+System.getProperty("java.home"));
	}
```



### 12.11 Math、Random

- java.lang.Math类:对数字作处理工具类.

```java
public static void main(String[] args) {
		//声明一个变量
		double num1=25.5;
		
		//向上取整
		double num2=Math.ceil(num1);
		//向下取整
		double num3=Math.floor(num1);
		//四舍五入
		double num4=Math.round(num1);
		//求一个数几次方,求2的三次方
		double num5=Math.pow(2, 3);
		//求[min,max]范围随机整数 int result=(int)(Math.random()*(max-min+1)+min);
		//[16,25]
		int result1=(int)(Math.random()*10+16);
	}
```



- java.util.Random:生成随机数的类

```java
public static void main(String[] args) {
		//创建随机数对象
		Random r=new Random();
		//调用方法生成随机数[10,99]
		int result2=r.nextInt(90)+10;
		//生成[min,max]范围内随机整数int result=r.nextInt(max-min+1)+min;
		
		System.out.println(result2);
	}
```



## 十三、集合

 ### 13.1 集合概念

- 集合:存储多个引用数据类型的容器.(动态数组,可以存储多个数据,且长度可变).
- 集合中常用概念:
  - 有序:按添加顺序来排列叫有序.
  - 可排序:按一定顺序(数字由小到大,由大到小,或按字母表顺序,逆序)排列叫可排序.
  - 唯一性:不可重复.

- 集合家族系谱图:

![image-20210428215644295](E:\qianfengJava2103\资料\笔记\笔记图片\集合家族系谱图.png)

- Collection接口:存储无序的,可重复的单一对象.
  - List接口:存储有序的,可重复的单一对象.
    - ArrayList类:存储有序的,可重复的单一对象.底层采用Object[]结构存值.
    - LinkedList类:存储有序的,可重复的单一对象.底层采用双向链表结构存值.
  - Set接口:存储无序的,唯一的单一对象.
    - HashSet类:存储无序的,唯一的单一对象.底层采用HashMap的Key存值.
    - TreeSet类:存储无序的,可排序的,唯一的单一对象.底层采用TreeMap的Key存值.

- Map接口:按key-value对方式存值.
  - HashMap类:按key-value对方式存值,它的key无序的,唯一的单一对象.底层采用数组+链表结构存值.
  - TreeMap类:按key-value对方式存值,它的key无序的,可排序的,唯一的单一对象.底层采用二叉树结构存值.



### 13.2 ArrayList

- ArrayList：存储有序的,可重复的单一对象.底层采用Object[]结构存值.默认按照1.5倍扩容.
  优点:按顺序添加效率高，遍历和修改集合中元素效率高
  缺点:删除和按指定索引添加效率低．

```java
public static void main(String[] args) {
		//创建集合对象
		ArrayList arr1=new ArrayList();
		
		//向集合添加元素对象
		arr1.add(66);
		arr1.add(11);
		arr1.add(44);
		arr1.add(66);
		
		//向指定索引位置添加元素,添加索引范围[0,size()]
		arr1.add(0, 55);
		
		//遍历集合
		for (int i = 0; i < arr1.size(); i++) {
			//遍历集合中元素,访问索引范围[0,size()-1]
			System.out.println(arr1.get(i));
		}
		System.out.println("---------------------------");
		
		//修改集合中元素,修改索引范围[0,size()-1]
		arr1.set(1, 33);
		
		//遍历集合
		for (Object ob : arr1) {
			System.out.println(ob);
		}
		System.out.println("**************************");

		//删除集合中指定索引位置的元素,删除索引范围[0,size()-1]
		arr1.remove(1);
		
		//删除集合中元素
		//如果集合中有多个一样的元素,删除时永远删除第一个元素.
		arr1.remove((Object)11);
		
		//遍历集合
		for (int i = 0; i < arr1.size(); i++) {
			//遍历集合中元素
			System.out.println(arr1.get(i));
		}
		System.out.println("$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$");
		
		//清空集合
		arr1.clear();
		
		//遍历集合
		for (int i = 0; i < arr1.size(); i++) {
			//遍历集合中元素
			System.out.println(arr1.get(i));
		}
}
```



### 13.3 过滤器(filter)

- 过滤器(filter):将需要的数据留下,不需要的数据过滤器.

```java
public static void main(String[] args) {
		//创建集合
		List alist2=new ArrayList();
		
		//向集合中添加元素
		alist2.add(66);
		alist2.add(67);
		alist2.add(68);
		alist2.add(47);
		alist2.add(57);
		
		//遍历集合
		for (Object ob : alist2) {
			System.out.println(ob);
		}
		System.out.println("-------------------------");
		
		//用过滤器对象删除集合中元素,方法参数用匿名内部类过滤器对象
		alist2.removeIf(new Predicate() {
			/**
			 * 过滤方法
			 * @param t 集合中每个元素
			 */
			@Override
			public boolean test(Object t) {
				if (t.toString().startsWith("6")) {
					return true;//满足条件,删除
				} else {
					return false;//不满足条件,留下 
				}
				
			}
		});
		
		//遍历集合
		for (Object ob : alist2) {
			System.out.println(ob);
		}
	}

```



### 13.4 LinkedList

- LinkedList:存储有序的,可重复单一对象.底层采用双向链表结构存值.
  - 优点:添加和删除效率高
  - 缺点:遍历和修改效率低
  - 源码分析时:用了变量追踪法.

![image-20210428215548774](E:\qianfengJava2103\资料\笔记\笔记图片\LinkedList1.png)

```java
public static void main(String[] args) {
		//创建集合对象
		LinkedList list3=new LinkedList();
		
		//向集合中添加元素
		list3.add(99);
		list3.add(55);
		
		//向集合中指定索引位置添加元素,添加索引范围[0,size()]
		list3.add(2, 44);
		
		//向集合中添加第一个元素
		list3.addFirst(22);
		
		//向集合中添加最后一个元素
		list3.addLast(66);
		
		//遍历集合
		for (int i = 0; i < list3.size(); i++) {
			System.out.println(list3.get(i));
		}
		System.out.println("------------------------");
		
		//修改集合中元素,修改索引范围[0,size()-1]
		list3.set(3, 66);
		
		//遍历集合
		for (Object ob : list3) {
			System.out.println(ob);
		}
		System.out.println("**************************");
		
		//删除元素
		list3.remove((Object)66);
		
		//根据指定索引删除,删除索引范围[0,size()-1]
		list3.remove(3);
		
		//删除集合中第一个元素
		list3.removeFirst();
		
		//删除集合中最后一个元素
		list3.removeLast();
		
		//遍历集合
		for (Object ob : list3) {
			System.out.println(ob);
		}
		System.out.println("$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$");
		
		//清空集合
		list3.clear();
	}

```



### 13.5 ArrayList VS Vector(面试)

- 相同点
  - 都是存储有序的,可重复的单一对象.底层都是采用Object[]结构存值.

- 不同点:
  - 推出的时间不同:Vector在jdk1.0时就推出;ArrayList在jdk1.2时推出集合框架时才推出.
  - 扩容不同:Vector默认按原来2倍扩容;ArrayList默认按原来1.5倍.安全性不同:Vector线程安全,效率低;ArrayList效率高,但是在多线程中使用不安全.
  - ArrayList拥有的所有的方法Vector都有,Vector还有自己独有的方法.

### 13.6 迭代器(Iterator)

- 迭代器(Iterator):专门用来遍历集合的工具.
  - hasNext():判断迭代器容器后面是否有元素可迭代
  - next(): 返回迭代中的下一个元素。每个元素只能迭代一次

![image-20210428215411708](E:\qianfengJava2103\资料\笔记\笔记图片\迭代器1.png)



```java
public static void main(String[] args) {
		//创建集合
		List list4=new ArrayList();
		//向集合中添加元素
		list4.add(new Student("张三1", 50));
		list4.add(new Student("张三6", 20));
		list4.add(new Student("张三3", 18));
		list4.add(new Student("张三4", 90));
		list4.add(new Student("张三2", 30));
		
		//获得集合迭代器容器,用父接口作为数据类型,指向子类对象
		Iterator it1=list4.iterator();
		
		/*每判断一次就迭代一次*/
		//判断迭代器后面是否有元素可迭代
		while (it1.hasNext()) {
			//获得迭代元素,一个元素只能调用一次next()
			Student ob=(Student) it1.next();
			System.out.println(ob.sname+","+ob.sage);
		}
	}

```



- Collections:collection集合家族工具类.

- 泛型:将引用数据类型参数化.(将引用数据类型作为参数传递).语法:<数据类型>
- 泛型集合:一个集合中只能存泛型指定的数据类型的数据叫泛型集合.
  - 为什么要用泛型集合:因为普通集合存数据时要频繁进行数据类型转换,遍历集合中数据时,又要频繁转换为原来的类型,使用不太方便且浪费运行内存,所以用泛型集合.
  - 泛型集合优点:避免频繁类型转换.声明时进行类型检查.
  - 泛型集合语法:集合类型<数据类型> 集合名=new 集合类型[<数据类型>]();
    		

```java
public static void main(String[] args) {
		//创建泛型集合对象
		List<Teacher> list5=new ArrayList();
		//向集合中存引用数据类型
		list5.add(new Teacher("孙星", 18));
		list5.add(new Teacher("安静", 18));
		list5.add(new Teacher("张宇延", 18));
		for (Teacher t : list5) {
		System.out.println(t.tname+","+t.tage);
	}		
}
```


### 13.7 泛型

#### 13.7.1 泛型迭代器

- 泛型迭代器:指定迭代器迭代每个元素的类型.
  - 泛型迭代器的作用:遍历元素避免频繁类型转换
  - 泛型迭代器与泛型集合是黄金搭挡.
  - 泛型迭代器语法:Iterator<数据类型> 迭代器名=集合名.iterator();

```java
public static void main(String[] args) {
		//创建泛型集合对象
		List<Teacher> list5=new ArrayList();
		//向集合中存引用数据类型
		list5.add(new Teacher("孙星", 18));
		list5.add(new Teacher("安静", 18));
		list5.add(new Teacher("张宇延", 18));
		
		/*遍历集合*/
		//获得集合的迭代器容器
		Iterator<Teacher> it1=list5.iterator();
		//每判断一次就迭代一次
		while (it1.hasNext()) {
			//获得迭代元素
			Teacher ob= it1.next();
			System.out.println(ob);
		}
	}
```



#### 13.7.2 泛型类

- 泛型类:将泛型作为参数传给类.

  ```java
  /**
   * 泛型类
   * <T>是泛型,T是泛型占位符,指代任何一个具体的引用数据类型
   * @author sx
   * @version 2021年4月26日
   */
  public class Dog<T>{
  	public String nickName;
  	public T dt;
  }
  
  public static void main(String[] args) {
  		//创建泛型类的对象
  		Dog<String> d1=new Dog<String>();
  		//用对象调用属性
  		d1.nickName="大发";
  		//创建对象时,泛型传的是什么类型,属性就是什么类型
  		d1.dt="哈哈哈";
  		
  		//创建泛型类的对象
  		Dog<Integer> d2=new Dog<Integer>();
  		//用对象调用属性
  		d2.nickName="大发";
  		//创建对象时,泛型传的是什么类型,属性就是什么类型
  		d2.dt=11;
  	}
  ```

  

#### 13.7.3 泛型方法

- 泛型方法:将泛型作为参数的数据类型传给方法.作用:增加方法灵活性.

```java
/**
 * 泛型方法的使用
 * @author sx
 * @version 2021年4月26日
 */
public class Dog2 {
	/**
	 * 泛型方法
	 * @param <T> 泛型, T是泛型占位符,可以是任何一个具体的数据类型
	 * @param t1 泛型类型形参
	 */
	public <T> void show1(T t1) {
		System.out.println("方法参数为:"+t1);
	}
}

public static void main(String[] args) {
		//创建对象
		Dog2 d2=new Dog2();
		//用对象调用泛型方法
		d2.show1("呵呵");
		d2.show1(123);
		d2.show1(true);
	}
```

> 泛型变量不可以用static和final修饰.
>
> (扩展)受限泛型:
> 		(1)<?>：表示任意类型
> 		(2)<? super T>：表示T类或者T类的父类
> 		(3)<? extends T>：表示T类或者T类的子类 
>
> Stack继承自Vector类,是按压栈的方法存值,取值是按后进先出的方式取值.



### 13.8 HashSet

- HashSet：存储有序的，唯一的单一对象，底层采用HashMap的Key存值
  - 注意：HashSet想要根据元素的值去重，那么HashSet的泛型中要重写HashCode（）和equals（）;
  - 优点：去重性。
  - 去重性：通过hashCode（）和equals（）两个方法去实现去重的。

![image-20210428215203594](E:\qianfengJava2103\资料\笔记\笔记图片\HashSet1.png)



```java
public static void main(String[] args) {
		//创建集合对象
		HashSet<Student> set1=new HashSet<Student>();
		
		//向集合中添加元素
		set1.add(new Student("张三", 66));
		set1.add(new Student("李四", 33));
		set1.add(new Student("王五", 44));
		set1.add(new Student("赵六", 88));
		set1.add(new Student("张三", 66));
		
		//获得集合迭代器
		Iterator<Student> it1=set1.iterator();
		//第判断一个元素就迭代一个元素
		while (it1.hasNext()) {
			//获得迭代的当前元素
			Student s=it1.next();
			System.out.println(s);
		}
		System.out.println("-------------------------------");
		
		//删除集合中元素
		set1.remove(new Student("王五", 44));
		
		//遍历集合
		for (Student i : set1) {
			System.out.println(i);
		}
	}

2.(了解)LinkedHashSet:存储是有序的,唯一的单一对象.
	eg:public static void main(String[] args) {
		//创建集合对象
		HashSet<Student> set1=new LinkedHashSet<Student>();
		
		//向集合中添加元素
		set1.add(new Student("张三", 66));
		set1.add(new Student("李四", 33));
		set1.add(new Student("王五", 44));
		set1.add(new Student("赵六", 88));
		set1.add(new Student("张三", 66));
		
		//获得集合迭代器
		Iterator<Student> it1=set1.iterator();
		//第判断一个元素就迭代一个元素
		while (it1.hasNext()) {
			//获得迭代的当前元素
			Student s=it1.next();
			System.out.println(s);
		}
		System.out.println("-------------------------------");
		
		//删除集合中元素
		set1.remove(new Student("王五", 44));
		
		//遍历集合
		for (Student i : set1) {
			System.out.println(i);
		}
	}

```



### 13.9 TreeSet

- TreeSet:存储无序的,可排序的,唯一的单一对象.底层采用TreeMap的key存值.

  - 注意：TreeSet一定要用排序器

    - 如果用无参构造创建的TreeSet，默认采用自然排序器，要求TreeSet泛型类中实现自然排序器接口（Comparable），重写排序方法compareTo（）;

    - 如果用有参构造创建的TreeSet，要将自定义排序器（Comparator）对象作为参数构造方法，采用自定义排序器中排序方法compare（）来排序。

  - 优点：可排序，去重性。

    - 可排序：通过排序器的排序方法返回负数排在前面，返回正数排在后面。
    - 去重性（唯一性）：通过排序器排序方法返回0，表示相同元素不存。

![image-20210428215047310](E:\qianfengJava2103\资料\笔记\笔记图片\TreeSet1.png)



```java
public static void main(String[] args) {
		//创建集合对象
		TreeSet<Integer> set2=new TreeSet<Integer>();
		
		//向集合中添加元素
		set2.add(66);
		set2.add(44);
		set2.add(33);
		set2.add(55);
		set2.add(88);
		set2.add(77);
		set2.add(99);
		set2.add(66);
		
		/*遍历集合*/
		//获得集合迭代器对象
		Iterator<Integer> it2=set2.iterator();
		//每判断一次就迭代一次
		while (it2.hasNext()) {
			Integer i=it2.next();
			System.out.println(i);
		}
		System.out.println("----------------------------------");
		
		//删除集合中元素
		set2.remove(44);
		
		//遍历集合
		for (Integer i : set2) {
			System.out.println(i);
		}
	}

```



### 13.10 排序器

#### 13.10.1 自然排序器(Comparable)

```java
/**
 * 老师类,实现自然排序器接口,重写排序方法
 * @author sx
 * @version 2021年4月27日
 */
public class Teacher implements Comparable<Teacher>{
	public String tname;
	public Integer tage;
	
	@Override
	public String toString() {
		return "Teacher [tname=" + tname + ", tage=" + tage + "]";
	}

	public Teacher() {
		super();
	}

	public Teacher(String tname, Integer tage) {
		super();
		this.tname = tname;
		this.tage = tage;
	}

	/**
	 * 自然排序方法
	 * 排序:先根据对象姓名进行升序来排序,姓名相同再根据年龄升序排序
	 * this 表示当前要添加元素
	 * @param o 表示从根节点开始每个要比较的节点对象
	 * @return int 返回负数排在前面,返回正数排在后面,返回0表示相同元素
	 */
	@Override
	public int compareTo(Teacher o) {
		if (this.tname.compareTo(o.tname)!=0) {//姓名不同
			return this.tname.compareTo(o.tname);
		}else {//姓名相同
			if (this.tage<o.tage) {
				return -1;
			}else if (this.tage>o.tage) {
				return 1;
			}else {//姓名相同,年龄相同
				return 0;
			}
		}
	}
}

public static void main(String[] args) {
		//创建集合对象
		TreeSet<Teacher> set2=new TreeSet<Teacher>();
		
		//向集合中添加元素
		set2.add(new Teacher("hh", 66));
		set2.add(new Teacher("aa", 44));
		set2.add(new Teacher("bb", 33));
		set2.add(new Teacher("aa", 55));
		set2.add(new Teacher("mm", 88));
		set2.add(new Teacher("ww", 77));
		set2.add(new Teacher("pp", 99));
		set2.add(new Teacher("hh", 66));
		
		/*遍历集合*/
		//获得集合迭代器对象
		Iterator<Teacher> it2=set2.iterator();
		//每判断一次就迭代一次
		while (it2.hasNext()) {
			Teacher i=it2.next();
			System.out.println(i);
		}
		System.out.println("----------------------------------");
		
		//删除集合中元素
		set2.remove(new Teacher("aa", 44));
		
		//遍历集合
		for (Teacher i : set2) {
			System.out.println(i);
		}
	}

```



#### 13.10.2 自定义排序器(Comparator)

```java
/**
 * 自定义排序器类
 * @author sx
 * @version 2021年4月27日
 */
public class MyComparator implements Comparator<Cat>{

	/**
	 * 自定义排序器的排序方法
	 * 排序:先根据年龄降序,年龄相同,再根据昵称升序
	 * @param o1 当前要添加元素
	 * @param 02 表示从根节点开始每个要比较的节点元素
	 * @return int 返回负数排在前面,返回正数排在后面,返回0表示相同元素
	 */
	@Override
	public int compare(Cat o1, Cat o2) {
		if (o1.age.compareTo(o2.age)!=0) {//年龄不同
			return -o1.age.compareTo(o2.age);
		}else {//年龄相同
			return o1.nickName.compareTo(o2.nickName);
		}
	}
}

public static void main(String[] args) {
		//创建自定义排序器对象
		MyComparator mc=new MyComparator();
		//创建集合对象,将自定义排序器对象作为构造方法的参数传入
		TreeSet<Cat> set2=new TreeSet<Cat>(mc);
		
		//向集合中添加元素
		set2.add(new Cat("hh", 66));
		set2.add(new Cat("aa", 44));
		set2.add(new Cat("bb", 33));
		set2.add(new Cat("aa", 33));
		set2.add(new Cat("mm", 88));
		set2.add(new Cat("ww", 77));
		set2.add(new Cat("pp", 99));
		set2.add(new Cat("hh", 66));
		
		/*遍历集合*/
		//获得集合迭代器对象
		Iterator<Cat> it2=set2.iterator();
		//每判断一次就迭代一次
		while (it2.hasNext()) {
			Cat i=it2.next();
			System.out.println(i);
		}
		System.out.println("----------------------------------");
		
		//删除集合中元素
		set2.remove(new Cat("aa", 44));
		
		//遍历集合
		for (Cat i : set2) {
			System.out.println(i);
		}
	}

```



#### 13.10.3 匿名内部类自定义排序器

```java
public static void main(String[] args) {
		//创建集合对象,将匿名内部类自定义排序器对象作为构造方法的参数传入
		TreeSet<Cat> set2=new TreeSet<Cat>(new Comparator<Cat>() {
			/**
			 * 自定义排序器排序方法
			 * 排序:先根据昵称降序排序,昵称相同再根据年龄降序
			 * @param o1 当前要添加的元素
			 * @param o2 从根节点开始每个要比较节点元素
			 * @return int 返回负数排在前面,返回正数排在后面,返回0相同
			 */
			@Override
			public int compare(Cat o1, Cat o2) {
				if (o1.nickName.compareTo(o2.nickName)!=0) {//昵称不同
					return -o1.nickName.compareTo(o2.nickName);
				} else {//昵称相同,根据年龄降序
					return -o1.age.compareTo(o2.age);
				}
			}
		});
		
		//向集合中添加元素
		set2.add(new Cat("hh", 66));
		set2.add(new Cat("aa", 44));
		set2.add(new Cat("bb", 33));
		set2.add(new Cat("aa", 33));
		set2.add(new Cat("mm", 88));
		set2.add(new Cat("ww", 77));
		set2.add(new Cat("pp", 99));
		set2.add(new Cat("hh", 66));
		
		/*遍历集合*/
		//获得集合迭代器对象
		Iterator<Cat> it2=set2.iterator();
		//每判断一次就迭代一次
		while (it2.hasNext()) {
			Cat i=it2.next();
			System.out.println(i);
		}
		System.out.println("----------------------------------");
		
		//删除集合中元素
		set2.remove(new Cat("aa", 44));
		
		//遍历集合
		for (Cat i : set2) {
			System.out.println(i);
		}
	}

```



### 13.11 Map 

- Map是一种依照键（key）存储元素的容器，键（key）很像下标，在List中下标是整数。在Map中键（key）可以使任意类型的对象。Map中不能有重复的键（Key），每个键（key）都有一个对应的值（value）。
- Map一次存一对元素, Collection 一次存一个。Map 的键不能重复，保证唯一。是以键值对的形式存在.键与值存在映射关系.一定要保证键的唯一性.

- 一个键（key）和它对应的值构成map集合中的一个元素。

- Map中的元素是两个对象，一个对象作为键，一个对象作为值。键不可以重复，但是值可以重复。

- Map与Collection在集合框架中属并列存在，Map存储的是键值对，Map存储元素使用put方法。
- Map集合没有直接取出元素的方法，而是先转成Set集合，在通过迭代获取元素
- Map集合中键要保证唯一性，也就是Collection是单列集合, Map 是双列集合。



- Map体系：

  - Map接口    将键映射到值的对象。一个映射不能包含重复的键；每个键最多只能映射到一个值。

    - HashMap  采用哈希表实现，所以无序。

    - TreeMap   可以对健进行排序

  - Hashtable:

    - 底层是哈希表数据结构，线程是同步的，不可以存入null键，null值。效率较低，被HashMap 替代.

  - HashMap:

    - 底层是哈希表数据结构，线程是不同步的，可以存入null键，null值。要保证键的唯一性，需要覆盖hashCode方法，和equals方法。

  - LinkedHashMap：
    - 该子类基于哈希表又融入了链表。可以Map集合进行增删提高效率。
  - TreeMap:
    - 底层是二叉树数据结构。可以对map集合中的键进行排序。需要使用Comparable或者Comparator 进行比较排序。return 0，来判断键的唯一性。



- Map的常用方法：

  1、添加：
  	1、V put(K key, V value)    （可以相同的key值，但是添加的value值会覆
  盖前面的，返回值是前一个，如果没有就返回null）                                         

  ​	2、putAll(Map<? extends K,? extends V> m)  从指定映射中将所有映射关
  系复制到此映射中（可选操作）。
  2、删除
  ​	1、remove()    删除关联对象，指定key对象
  ​	2、clear()     清空集合对象
  3、获取
  ​     1：value get(key); 可以用于判断键是否存在的情况。当指定的键不存在的时候，返
  回的是null。

  4、判断：
  	1、boolean isEmpty()   长度为0返回true否则false
      2、boolean containsKey(Object key)  判断集合中是否包含指定的key
      3、boolean containsValue(Object value)  判断集合中是否包含指定的value

  5、长度：int size（）

```java
public class MapTest01 {
    public static void main(String[] args) {
        //定义一个Map的容器对象
        Map<String,Integer> map1 = new HashMap<String, Integer>();
        map1.put("jack",20);
        map1.put("rose",22);
        map1.put("lucy",24);
        map1.put("tom",26);
        System.out.println("map1:"+map1);

        Map<String,Integer> map2 = new HashMap<String, Integer>();
        map2.put("张三丰",45);
        map2.put("张无忌",24);
        System.out.println("map2:"+map2);

        map1.putAll(map2);
        System.out.println("map1:"+map1);

        //删除
        System.out.println(map1.remove("张无忌",24));
        System.out.println(map1);

        //获取 get(Object key) 通过指定的key对象获取value对象
        System.out.println(map1.get("tom"));
        //int size() 获取容器的大小
        System.out.println(map1.size());

        /*
        判断
        1、boolean isEmpty()   长度为0返回true否则false
        2、boolean containsKey(Object key)  判断集合中是否包含指定的key
        3、boolean containsValue(Object value)  判断集合中是否包含指定的value
         */
        System.out.println("isEmpty:"+map1.isEmpty());
        System.out.println("containsKey："+map1.containsKey("tom"));
        System.out.println("containsValue："+map1.containsValue(100));
    }
}

```



- 遍历Map的方式：

  1、将map 集合中所有的键取出存入set集合。Set<K> keySet() 返回所有的key对象的Set集合，再通过get方法获取键对应的值。

  2、 values() ，获取所有的值.
  		Collection<V> values()不能获取到key对象
  3、 Map.Entry对象 (推荐)
  		Set<Map.Entry<k,v>> entrySet()
  将map 集合中的键值映射关系打包成一个对象，Map.Entry对象通过Map.Entry 对象的getKey，getValue获取其键和值。



- 第一种方式:使用keySet

  将Map转成Set集合（keySet()），通过Set的迭代器取出Set集合中的每一个元素（Iterator）就是Map集合中的所有的键，再通过get方法获取键对应的值。

```java
public class MapTest02 {
    public static void main(String[] args) {
        Map<Integer,String> map = new HashMap<Integer, String>();
        map.put(1,"aaa");
        map.put(2,"bbb");
        map.put(3,"ccc");

        Set<Integer> it1 = map.keySet();
        Iterator<Integer> iterator = it1.iterator();
        while (iterator.hasNext()){
            Integer key = iterator.next();
            String value = map.get(key);
            System.out.println("key=："+key+"\t"+"value=："+value);
        }
    }
}
```



- 第二种方式: 通过values 获取所有值,不能获取到key对象

  ```java
  public class MapTraverse02 {
      public static void main(String[] args) {
          Map<Integer,String> map = new HashMap<Integer, String>();
          map.put(1,"aaa");
          map.put(2,"bbb");
          map.put(3,"ccc");
  
          Collection<String> it1 = map.values();
          Iterator<String> iterator = it1.iterator();
          while (iterator.hasNext()){
              String s = iterator.next();
              System.out.println(s);
          }
      }
  }
  ```

  

- 第三种方式: Map.Entry

  public static interface Map.Entry<K,V>

  通过Map中的entrySet()方法获取存放Map.Entry<K,V>对象的Set集合。

  Set<Map.Entry<K,V>> entrySet()

  面向对象的思想将map集合中的键和值映射关系打包为一个对象，就是Map.Entry，将该对象存入Set集合，Map.Entry是一个对象，那么该对象具备的getKey，getValue获得键和值。

  ```java
  public class MapTraverse03 {
      public static void main(String[] args) {
          Map<Integer,String> map = new HashMap<Integer, String>();
          map.put(1,"aaa");
          map.put(2,"bbb");
          map.put(3,"ccc");
  
          // 返回的Map.Entry对象的Set集合 Map.Entry包含了key和value对象
          Set<Map.Entry<Integer,String>> entries = map.entrySet();
          Iterator<Map.Entry<Integer,String>> iterator = entries.iterator();
          while (iterator.hasNext()){
              // 返回的是封装了key和value对象的Map.Entry对象
              Map.Entry<Integer, String> integer = iterator.next(); 
              // 获取Map.Entry对象中封装的key和value对象
              Integer key =  integer.getKey();
              String value = integer.getValue();
              System.out.println("key=："+key+"\t"+"value："+value);
  
          }
      }
  }
  ```

  

### 13.12 HashMap

- HashMap是基于Map接口的实现，底层采用数组+链表结构存值，键不可以重复，值可以重复。可以存入null键，null值，但键只能有一条记录为null，值可以有多条记录为null；线程不安全；

- 注意:如果HashMap的Key想要根据值去重,key的泛型类中要重写hashCode()和equals().
  	优点:key可以去重.
  	key的唯一性(去重):通过hashCode()和equals()来去重的.

  ![HashMap1](E:\qianfengJava2103\资料\笔记\笔记图片\HashMap1.png)

- 自定义对象作为Map的键

```java
public class Person {
    private String name;
    private int age;

    public Person() {

    }

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Person person = (Person) o;
        return age == person.age &&
                Objects.equals(name, person.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }
}

```

```java
public class HashMapTest {
    public static void main(String[] args) {
        HashMap<Person,String> hashMap = new HashMap<>();
        hashMap.put(new Person("jack",23),"1001");
        hashMap.put(new Person("tom",21),"1002");
        hashMap.put(new Person("luck",25),"1003");
        hashMap.put(new Person("rose",31),"1004");
        hashMap.put(new Person("jim",35),"1005");

        System.out.println(hashMap);
        System.out.println(hashMap.put(new Person("tom",21),"1006"));

        Set<Map.Entry<Person,String>> en = hashMap.entrySet();
        Iterator<Map.Entry<Person,String>> iterator = en.iterator();
        while (iterator.hasNext()){
            Map.Entry<Person,String> next = iterator.next();
            Person key = next.getKey();
            String value = next.getValue();
            System.out.println("key=："+key+"\t"+"value："+value);
        }
    }
}
```



### 13.13 TreeMap

TreeMap:按key-value对方式存值.它的key是无序的,可排序的,唯一的单一对象.底层采用二叉树结构存值.
	注意:TreeMap一定要用排序器.如果是用无参构造创建的TreeMap默认采用自然排序器,要求 TreeMap的key的泛型类实现自然排序器接口(Comparable),重写排序方法;如果用有参构造创建TreeMap,要求将自定义排序器(Comparator)对象作为TreeMap构造方法的参数传入,在自定义排序器类中重写排序方法.
	优点:key的可排序性,唯一性.
	key的可排序性:通过排序器排序方法返回负数排在前面,返回正数排在后面.
	唯一性(去重):通过排序器排序方法返回0,表示相同元素,key不存,value覆盖.

![image-20210428214339526](E:\qianfengJava2103\资料\笔记\笔记图片\TreeMap1.png)


- 自然排序器

```java
public class Demo4 {
	public static void main(String[] args) {
		TreeMap<String, Integer> tree = new TreeMap<String, Integer>();
		tree.put("张三", 19);
		tree.put("李四", 20);
		tree.put("王五", 21);
		tree.put("赵六", 22);
		tree.put("周七", 23);
		tree.put("张三", 24);
		System.out.println(tree);
		System.out.println("张三".compareTo("李四"));//-2094
	}
}
```

- 自定义排序器

  ```java
  public class Person {
      private String name;
      private int age;
  
      public Person() {
  
      }
  
      public Person(String name, int age) {
          this.name = name;
          this.age = age;
      }
  
      public String getName() {
          return name;
      }
  
      public void setName(String name) {
          this.name = name;
      }
  
      public int getAge() {
          return age;
      }
  
      public void setAge(int age) {
          this.age = age;
      }
  
      @Override
      public String toString() {
          return "Person{" +
                  "name='" + name + '\'' +
                  ", age=" + age +
                  '}';
      }
  
      @Override
      public boolean equals(Object o) {
          if (this == o) return true;
          if (o == null || getClass() != o.getClass()) return false;
          Person person = (Person) o;
          return age == person.age &&
                  Objects.equals(name, person.name);
      }
  
      @Override
      public int hashCode() {
          return Objects.hash(name, age);
      }
  }
  
  ```

  

  ```java
  public class TreeMapTest {
      public static void main(String[] args) {
          TreeMap<Person,String> map = new TreeMap<Person,String>(new Comparator<Person>() {
              @Override
              public int compare(Person p1, Person p2) {
                 if (p1.getAge() < p2.getAge()){
                     return -1;
                 }else if (p1.getAge() > p2.getAge()){
                     return 1;
                 }else{
                     return p1.getName().compareTo(p2.getName());
                 }
              }
          });
  
          map.put(new Person("jack",23),"1001");
          map.put(new Person("tom",21),"1002");
          map.put(new Person("luck",25),"1003");
          map.put(new Person("rose",31),"1004");
          map.put(new Person("jim",35),"1005");
  
          Set<Map.Entry<Person,String>> en = map.entrySet();
          Iterator<Map.Entry<Person,String>> it1 = en.iterator();
          while (it1.hasNext()){
              Map.Entry<Person,String> next = it1.next();
              Person key = next.getKey();
              String value = next.getValue();
              System.out.println("key=："+key+"\t"+"value："+value);
          }
      }
  }
  ```




- 匿名自定义排序器

  ```java
  public static void main(String[] args) {
  		//创建集合对象,用有参构造创建TreeMap,要求将自定义排序器对象作为构造方法参数传入
  		Map<Teacher3, String> map2=new TreeMap(new Comparator<Teacher3>() {
  
  			/**
  			 * 重写自定义排序器排序方法
  			 * 排序:根据年龄降序排序
  			 * @param o1 当前要添加元素的key
  			 * @param o2 从根节点开始每个要比较的节点对象的key
  			 * @return int 返回负数排在前面,返回正数排在后面,返回0表示相同,key不存value覆盖
  			 */
  			@Override
  			public int compare(Teacher3 o1, Teacher3 o2) {
  				return -o1.tage.compareTo(o2.tage);
  			}
  		});
  		//向集合中添加元素
  		map2.put(new Teacher3("dd", 66), "kk");
  		map2.put(new Teacher3("bb", 44), "uu");
  		map2.put(new Teacher3("aa", 33), "mm");
  		map2.put(new Teacher3("cc", 55), "ss");
  		map2.put(new Teacher3("hh", 11), "aa");
  		map2.put(new Teacher3("yy", 56), "bb");
  		map2.put(new Teacher3("bb", 78), "qq");
  		map2.put(new Teacher3("dd", 66), "kk");
  		
  		/*第一种遍历map集合的方式*/
  		//将key-value当作entry整体,将map集合转换为set集合
  		Set<Entry<Teacher3, String>> set2=map2.entrySet();
  		for (Entry<Teacher3, String> e : set2) {
  			System.out.println("键为:"+e.getKey()+",值为:"+e.getValue());
  		}
  		System.out.println("-------------------------------");
  		
  		//删除集合中元素
  		map2.remove(new Teacher3("bb", 44));
  		
  		/*第二种遍历map集合的方式*/
  		//将map集合中所有key获得
  		Set<Teacher3> keys=map2.keySet();
  		//获得集合的迭代器
  		Iterator<Teacher3> it2=keys.iterator();
  		//循环迭代key
  		while (it2.hasNext()) {
  			//获得当前迭代的key
  			Teacher3 k=it2.next();
  			System.out.println("键为:"+k+",值为:"+map2.get(k));
  		}
  	}
  ```



### 13.14 Hashtable

- (了解)Hashtable:哈希表.线程安全,运行效率慢;不允许null作为key或者是value.



### 13.15 HashMap VS HashTable:(面试)

相同点:

- 都是按key-value对方式存值,它的key是无充的,唯一的单一对象.底层采用数组+链表结构存值.
- 常用方法相同.
- 都是Map接口下子类．

10.2:不同点:

- 初始容量不同:HashMap默认初始容量为16,HashTable默认初始容量为11.
- 扩容不同:HashMap默认按原来2倍扩容,HashTable默认按原来2倍+1扩容.
- 线程安全不同:HashMap线程不安全,效率高;HashTable线程安全,效率低.
- null不同:HashMap的key与value都可以存null;HashTable的key与value都不可以存null.	
- 推出时间不同:HashMap在jdk1.2之后才推出的;HashTable在jdk1.2之前就推出.



### 13.16 总结

1.ArrayList:存储有序的,可重复的单一对象.底层采用Object[]结构存值.
		优点:遍历和修改效率高.按顺序添加效率高.
		缺点:删除和按索引添加效率低.

2.LinkedList:存储有序的,可重复的单一对象.底层采用双向链表结构存值.
		优点:增,删效率高
		缺点:遍历和修改效率低.

3.HashSet:存储无序的,唯一的单一对象.底层采用HashMap的key存值.
		优点:去重(唯一性).
		唯一性(去重):通过泛型所在类中重写HashCode()和equals()来实现根据值去重.

4.TreeSet:存储无序的,可排序的,唯一的单一对象.底层采用TreeMap的key存值.
		注意:TreeSet一定要使用排序器.如果用无参构造创建TreeSet默认使用自然排序器,要求TreeSet的泛型类实现自然排序器接口,重写排序方法.如果用有参构造创建TreeSet,要求将自定义排序器的对象作为构造方法的参数传入,在自定义排序器类中重写排序器方法.
		优点:可排序性,唯一性.
		可排序性:通过排序器的排序方法返回负数排在前面,返回正数排在后面.
		唯一性(去重):通过排序器的排序方法返回零,表示相同不存.

5.HashMap:按key-value对存值.它的key是无序的,唯一的单一对象.底层采用数组+链表结构存值.
		优点:key是唯一的(去重).
		key的唯一性(去重):通过HashMap的key的泛型类中重写HashCode()和equals()来实现
					根据key的值去重.

6.TreeMap:按key-value对存值.它的key是无序的,可排序的,唯一的单一对象.底层采用二叉树
			结构存值.
		注意:TreeMap一定要用排序器.如果用无参构造创建TreeMap,默认使用自然排序器,要求
			TreeMap的key的泛型所在类中要实现自然排序器接口,重写排序器方法;如果用有参构造创建TreeMap,将自定义排序器对象作为构造方法的参数传入,在自定义排序器类中重写排序方法.
		优点:key可排序性,key的唯一性.
		key的可排序性:通过排序器的排序方法返回负数排在前面,返回正数排在后面.
		key的唯一性(去重):通过排序器的排序方法返回零,表示相同key不存,value覆盖.

7.能实现直接去重的集合:HashSet,TreeSet,HashMap,TreeMap.首选HashSet去重.
	HashSet和HashMap通过重写hashCode()和equals()来实现去重的.
	TreeSet和TreeMap通过排序器的排序方法返回0来实现去重的.

8.能实现直接排序的集合:TreeSet,TreeMap.首选TreeSet排序.
	TreeSet和TreeMap通过排序器的排序方法返回负数排在前面,返回正数排在后面来实现排序.





## 十四、异常

- 异常:程序执行到一半时意外终止,这就是异常.
- 异常的根类java.lang.Throwable,它的下面两个子类
  - Error:由于硬件或软件环境出故障而导致严重错误,程序无法解决.
  - Exception:由于程序设计不合理或偶然外界因素导致的异常,这些异常是开发人员需要处理的.
    - 运行时异常(非检查异常):由于程序设计不合理而导致异常.eg:NullPointerException,ArrayIndexOutOfBoundsException,ClassCastException.
    - 检查异常(非运行时异常):由于偶然外界因素导致的异常.代码没有问题,但是写完了下面报一条红线.这种就是检查异常.eg:ParseException,IOException

- 异常处理机制:Java编程语言使用异常处理机制为程序提供了异常处理的能力。

  - 捕获异常异常:
    - 适用场景:任何异常情况.
    - 语法:
      			try{
        				可能会出异常的代码
        			}catch(异常类型1|异常类型2 e1){
        				出现异常类型1或者2的处理代码;
        			}catch(异常类型3 e1){
        				出现异常类型3的处理代码;
        			}finally{
        				关闭对象释放资源的代码
        			}

  - 语法特点:

    - 在try-catch-finally块中,try有且仅有一个,catch块可以有0到多个,finally块可以有0到1个.catch块和finally块至少要有一个.
    - 在try-catch-finally块中,每个catch块中小括号中可以写1到多个异常类型,异常类型间用|分隔,表示只要出现了其中任何一种异常类型,就可以执行这个catch块中处理代码.
    - 在try-catch-finally块中,有多个catch块时,代码从上到下,异常类型由小到大.
    - 在try-catch-finally块中,catch块最多执行一个,最小一个都不执行.
    - 在try-catch-finally块中,finally无论如何一定会执行,除非遇到System.exit(0)就不能执行;finally块执行优先级高于return.

    ```java
    public static void main(String[] args) {
    		try {
    			System.out.println("开始执行代码");
    			//int num=8/0;
    			System.out.println("代码执行结束");
    			//return;
    			System.exit(0);
    		}catch (ArithmeticException|NullPointerException e2) {
    			//打印异常信息
    			e2.printStackTrace();
    			System.out.println("出异常了2");
    		}catch (Exception e) {
    			System.out.println("出异常了1");
    		}finally {
    			System.out.println("这是finally");
    		}
    	}
    
    			eg:巧用try-catch让出异常的代码回归正轨执行
    				public static void main(String[] args) {
    		//声明变量作标记,标记是否需要重新输入
    		boolean flag=false;
    		do {
    			//初始化标记
    			flag=false;
    			try {
    				Scanner input=new Scanner(System.in);
    				System.out.println("请输入一个整数:");
    				int num=input.nextInt();
    				System.out.println("你接收值为:"+num);
    			}catch (InputMismatchException e) {
    				//输入错误,重新输入
    				System.out.println("你的输入有误,请重新输入!");
    				//改变标记
    				flag=true;
    			} catch (Exception e) {
    				e.printStackTrace();
    			}
    		} while (flag);
    
    	}
    
    ```

    

  

