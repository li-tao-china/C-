`http://edu.51cto.com//center/course/lesson/index?id=21945`
入门视频,选一个好视频很重要

## 06
- 类型在C#语言中的作用  
	- 存储此类型变量所需的内存空间大小  
	- 此类型的值可表示的最大、最小值范围		
	- 此类型所包含的成员（如方法、属性、事件等)  
	- 此类型由何基类派生而来
	- 程序运行的时候，此类型的变量被分配在内存的什么位置  
     Stack  
     Heap  
       使用performance Monitor 查看进程的堆内存使用量  
       关于内存泄漏 C#有垃圾回收机制不必手动回收  
    	此类型所允许的操作   
  	
- 语言类型  
	- **强类型**C#    
	- **弱类型**C/C++  
	- **更弱类型**JavaScript  

- C#语言的**类型系统**  
	*五大数据类型*  
	- 类    (Classes)        class  
	- 结构体(Structures)   struct  
	- 枚举   (Enumerations)  enum  
	- 接口   (Interfaces)  
	- 委托   (Delegates)

- Object  
	- 引用类型  
		- 类  
		- 接口  
		- 委托  
	- 值类型     
		- 结构体  
		- 枚举     		
	                   
- 变量、对象与内存  
	**什么是变量**  
表面上来看，变量的用途是存储数据  
实际上，变量表示了存储位置，并且每个变量都有一个类型以决定什么样的值能够存入变量

- 变量一共有**7**类  
	- 静态变量  
	- 实例变量(成员变量，字段)  
	- 数组变量  
	- 值参数  
	- 引用参数  
	- 输出参数  
	- 局部变量  
  狭义的变量指局部变量，因为其他种类的变量都有自己的约定名称  
     简单说，局部变量就是方法体里声明的变量  

- 变量=以变量名所对应的内存地址为起点、以其数据类型所要求的存储空间为长度的一块内存区域

- 值类型存储   
  值类型没有实例，所谓的“实例”与变量合二为一  
- 引用类型的变量与实例  
  引用类型变量与实例的关系：引用类型变量里存储的数据是对象的内存地址

## 08
	方法的由来  
	方法的定义与调用  
	构造器（一种特殊的方法）  
	方法的重载（Overload）  
	如何对方法进行debug  
	方法的调用与栈  

C++创建类，.h文件包含类的声明 .cpp文件包含类的定义  
C# java是纯面向对象语言  
- 方法的由来  
	- 方法的前身是C/C++语言的函数   
	- 方法是面向对象范畴的概念，在非面向对象语言中仍称为函数,只有作为类（结构体）的成员时才被称为方法  
	-  使用C/C++语言做对比  
	C++中使可以的，称为“全局函数”  
	C#语言中函数不可能独立于类（结构体）之外,永远都是类（或结构体）的成员  
	- 是类（或结构体）最基本的成员之一  
	最基本的成员只有两个--字段与方法（成员变量与成员函数），本质还是数据+算法  
	方法表示类（或结构体）“能做什么事情”   

- 方法的声明与调用  
  	声明方法的语法详解  
  
 	C#（声明/定义不分家）  
  	栈分配内存时从底往上分配直到溢出  

## 09
- 方法的重载
	- 方法签名由方法的名称、类型形参的个数和它的每一个形参(按从左到右的顺序)的类型和种类( 值、引用或输出) 组成。方法签名不包含返回类型。  
	- 实例构造函数签名由它的每一个形参(按从左到右的顺序)的类型和种类(值、引用或输出) 组成。  
	- 重载决策(到底调用哪一个重载):用于在给定了参数列表和一组候选函数成员的情况下，选择一个最佳函数成员来实施调用。  

- 如何对方法进行debug  
	- 设置断点(breakpoint)  
	- 观察方法调用时的call stack 函数掉用栈  
	- Step-in(F11), Step-over(F10), Step-out(shift+F11) 返回到调用它的方法  
	- 观察局部变量的值变化  
	需要观察locals窗口  

- 方法的调用与栈（内存中的）stack  
	方法调用时栈内存的分配  
	对stack frame的分析  
	在c++中被调函数的内存归主调函数管理  
	返回值 存放在CPU的寄存器上 闪存。。。  

## 10-12操作符详解  
	操作符概览  
	操作符的本质  
	操作符的优先级  
	同级操作符的运算顺序  

- Operator类别(优先级从上到下依次降低)  
	- 基本
	x.y	f(x) a[x] x++ x-- new typeof default checked unchecked delegate sizeof ->  
	- 一元 + - ! ~ ++x --x (T)x await &t *x  
	
	- 乘法 * / % 
	 
	- 加减 + - 
	 
	- 移位 << >>  
	
	- 关系和类型检测 < > <= >= is as  
	
	- 相等 == !=  
	
	- 逻辑"与"AND  
	&  
	- 逻辑"异或"XOR  
	^  
	- 逻辑"或"OR  
	|  
	- 条件"与"AND  
	&&  
	- 条件"或"OR  
	||  
	- null 合并  ??  
	
	- 条件  ?: 
	 
	- 赋值和lambda表达式 = *= /= %= += -= <<= >>= &= ^= |= =>  
	
	操作符是用来操作数据的，被操作符操作的数据称为操作数（Operand）

- 操作符的本质  
	操作符的本质是函数（即算法）的“简记法”  
	操作符不能脱离与它关联的数据类型  
	可以说操作符就是与固定数据类型相关联的一套基本算法的简记法   
例如：  
```
namespace operatorOfMethons
{
    class Program
    {
        static void Main(string[] args)
        {
            Person person1 = new Person();
            Person person2 = new Person();
            person1.Name = "Deer";
            person2.Name = "Deer'wife";
            List<Person> nation = person1 + person2;
            foreach (var i in nation)
            {
                Console.WriteLine(i);
            }
        }
    }
}

class Person
{
    public string Name;

    public static List<Person> operator +(Person p1,Person p2)
    {
        List<Person> people = new List<Person>();
        people.Add(p1);
        people.Add(p2);
        for(int i = 0; i< 11; i ++)
        {
            Person child = new Person();
            child.Name = p1.Name + "&" + p2.Name + "'s child";
            people.Add(child);
        }
        return people;
    }
}
```
- 优先级与运算顺序  
	- 操作符的优先级  
	可以使用圆括号提高被括起来表达式的优先级  
	- 同优先级操作符的运算顺序  
	带有赋值功能的操作符的运算顺序是由右向左 
- 基本操作符   
	- 成员操作符'.'  
	1、访问外层名称空间中的子集名称空间  
	2、访问名称空间中的类型  
	3、访问类型中的静态成员  
	4、访问对象的成员（实例成员、方法）
	
	- 方法调用操作符'()'  
	f'()'圆括号  
	委托类Action 简接调用PrintHello这个方法,这时不需要()  
	  //Action myAction = new Action(c.PrintHello);  
	  //myAction();  
	
	- 元素访问操作符'[]'  
	访问数组中的元素  
	注意索引不一定都是整数  
	访问字典中的元素  
	
	- typeof操作符  
	查看一个类型的内部结构，属于的名称空间、类、名称、拥有的方法  
	```
	Type t = typeof(int);
	Console.WriteLine(t.Namespaces);
	Console.WriteLine(t.FullName);
	Console.WriteLine(t.Name);
	int c = t.GetMethods().Length;
	foreach(var mi in t.GetMethods())
	{
	  Console.WriteLine(mi.Name);
	}
	Console.WriteLine(c);
	```
	- default操作符  
	获取一个类型的默认值  
	引用类型 NULL  
	结构体  0  
	枚举   
	谁在第一个返回谁（谁是0返回谁）没有0返回0  
	
	```
	enum Level
	{
	  Low,
	  Mid,
	  High
	}
	```
	返回Low  
	```
	enum Level
	{
	  Low = 1;
	  Mid = 0;
	  High= 2;
	}
	```
	返回Mid
	```
	enum Level
	{
	  Low = 1;
	  Mid = 3;
	  High= 2;
	}
	```
	返回0
	
	- `new` 操作符    
		- 在内存中构造一个类型实例并调用实例构造器    
		如果左边有赋值符号，new操作符会把自己拿到的实例内存地址  
		通过赋值操作符交给负责访问实例的引用变量   
		`Form myForm = new Form();`  
		- var关键字  
	 	声明隐式类型变量 让编译器根据赋值来推断   
	 	显式  告诉编译器这是什么类型   
		- 2、调用实例的初始化器'{}'  
		`Form myForm = new Form(){Text = "hello"};`  
		- 3、`new Form() {Text = "hello"}.ShowDialog();`  
		使用完就被垃圾收集器收走了  
		- 语法糖衣   
		```
		int x = 100;
		string name = "Tim";
		```  
		`new `操作符被隐藏起来了    
	
		- 为匿名类型创造对象 让编译器自己去推断类型  
		`var person = new{Name="Mr.Okay",Age=34};`  
	
		- new的危险性  
		会造成依赖和紧耦合  
		设计模式，通过依赖注入设计模式，将紧耦合变松   
	
		- 继承中隐藏父类成员  
		```
		class Student
		{
	 	 	public void Report()
	  		{
	    		Console.WriteLine("I'm a student.");
	  		}
		}
	
		class CsStudent:Student
		{
	  		new public void Report()
	  		{
	   		 Console.WriteLine("I'm CS student");
	  		}
		}
		```
		
		- `checked unchecked`操作符  
		检查一个值在内存中是否有溢出  
		`checked`表示要程序去检查是否有溢出  
		`unchecked`表示不要程序去检查  
		`OverflowException`异常   
			
		```
		static void Main(string[] args)
		{
			uint x = uint.MaxValue;
			Console.WriteLine(x);
			string binStr = Convert.ToString(x,2);
			Console.WriteLine(binStr);
			unchecked/checked
			{
			    try
			    {
			        uint y = x + 1;
			        Console.WriteLine(y);
			    }
			    catch(OverflowException ex)
			    {
			        Console.WriteLine("There's overflow!");
			    }
			}
		}
		```
				
		- delegate操作符  
		lambda表达式替代了它这种功能  
		常用于委托声明 委托匿名方法  
		```
		public partial class MainWindow:Window
		{
			public MainWindow()
			{
			    InitializeComponent();
			    this.myButton.Click += myButton_Click;
			}
			
			void myButton_Click(object sender,RoutedEventArgs e)
			{
			    this.myTextBox.Text = "Hello,World!";
			}
		}
		```
		匿名方法
		```
		public partial class MainWindow:Window
		{
			public MainWindow()
			{
			    InitializeComponent();
			    this.myButton.Click += delegate(object sender,RoutedEventArgs e)
			    {
			        this.myTextBox.Text = "Hello,World!";
			    };
			} 
		}
		```
		lamada表达式
		```
		public partial class MainWindow:Window
		{
			public MainWindow()
			{
			    InitializeComponent();
			    this.myButton.Click += (sender, e)=>
			    {
			      this.myTextBox.Text = "Hello,World!";
			    };
			} 
		}
		```	
	- sizeof操作符   
	获取对象在内存中所占字节数  
	两点注意  
		- 1、只能获取基本数据类型实例在内存所占的字节数  结构体数据类型 string object不是结构体
		- 2、非默认情况下，可以获取自定义结构体类型实例在内存中所占的字节数 但只能放在unsafe条件下  
		```
		decimal           //占16字节
		double            //   8
		struct Student    //  16
		{
			int ID;
			long Score;
		}
		```
		
	- ->(箭头)操作符  
	 不安全上下文中   
	在`C#`中,指针操作,只能操作**结构体**中的数据