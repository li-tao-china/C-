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

	- 一元操作符（单目操作符）  
	  +- ! ~ ++x --x (T)x await &t *x  

	- &取地址操作符 *  
	 *pStu. 不行 因为'.'的优先级大于'*'  
		(*pStu).  

	- +- 正负操作符  
	```
	static void Main(string[] args)
	{
	    int x = int.MaxValue;
	    int y = checked(-x);
	    Console.WriteLine(x);
	    Console.WriteLine(y);
 	   string xStr = Convert.ToString(x,2).PadLeft(32,'0');
	    Console.WriteLine(xStr);
	}
	x == y
	```  

	- 有符号数取反    
	x = 0011  3  
	-x= 1000 + 0101 = -8 + 5 = -3   
	计算机中取相反数，先取反再加1  

	- ~取反操作符  
	二进制按位取反
	```
	static void Main(string[] args)
	{
		int x = int.MaxValue;
		int y = ~x;
		Console.WriteLine(x);
		Console.WriteLine(y);
		string xStr = Convert.ToString(x,2).PadLeft(32,'0');
		string yStr = Convert.ToString(y,2).PadLeft(32,'0');
		Console.WriteLine(xStr);
		Console.WriteLine(yStr);
	}
	x =  12345678
	y = -12345679
	```  
    计算机中取相反数，先取反再加1

	- ！取非操作符  
	针对布尔类型值

	- (T)x强制类型转换操作符  
	类型转化  
	隐式（implicit）类型转换  
	不丢失精度的转换  
	子类向父类的转换  
	装箱  
	显式（explicit）类型转换  
	有可能丢失精度（甚至发生错误）的转换，即cast  
	拆箱  
	使用Convert类  
	ToString方法与各数据类型的Parse/TryParse方法  
	自定义类型转换操作符  

	- 数学运算操作符  
	不同类型进行运算会有  类型提升 数值精度提升  
	整型除法 0做除数 会报错  
	浮点数除法 0做除数 根据被除数的正负得到正负无穷大  
	正无穷大除以负无穷大 得到 NAN  
	正无穷大+负无穷大 得到 NAN   

	- is as类型检验操作符 布尔类型  
	检验一个实例对象是不是一个类型的对象  
 
 	- ?? null合并操作符  
	`Nullable<int> x = null;`  
	可以转化为：  
	`int? x = null;`  
	`//x = 100;`  
	`int y = x??0;`  
	如果是null值，就用0代替   

	- ?:双目运算符  
	`int x = 80;`
	`string str  = (x >= 60) ? "pass":"Failed";`

## 13  
	表达式的定义  
	各类表达式概览  
	语句的定义  
	语句详解  
	

- ??null合并操作符   
null合并操作符左边的操作数它的类型的类型参数  
```
Nullable<int> x = null;
var y = x ?? 100;
Console.WriteLine(y.GetType().FullName);
```

- 语句的作用  
陈述算法思想，控制逻辑走向，完成有意义的动作  
由分号结尾的不一定都是语句  
using System; using 指令  
public string Name; 字段声明  
语句一定是出现在方法体里  

- 语句详解  
三大类statement  
labeled-statement        标签语句，并不多见  
declaration-statement    声明语句  
embedded-statement       嵌入式语句  
embedded-statement子类  





- 字段，属性，索引器，常量  

	常量    与类关联的常量值  
	字段    类的变量  
	属性    与读写类的命名属性相关联的操作  
	索引器  与以数组方式索引类的实例相关联的操作  

	- 字段  
		- 什么是字段  
		字段(field)是一种表示与对象或类型(类与结构体)关联的变量  
		字段是类型的成员，旧称"成员变量"  
		与对象关联的字段亦称"实例字段"  
		与类型关联的字段称为"静态字段",由static修饰  
		- 字段声明  
		在类里，方法里的不是字段  
		修饰符  
		new  
		public  
		protected  
		internal  
		private  
		static  
		readonly  
		volatile  
		- 字段的初始值   
		无显式初始化时，字段获得其类型的默认值，所以字段"永远都不会未被初始化"  
		实例字段初始化的时机--对象创建时  
		静态字段初始化的时机--类型被加载(load)时  
		- 只读字段  
		实例只读字段  
		初始化时构造器里  
		静态只读字段  
		初始化时构造器里  
 
- 属性  
 属性(property)是一种用于访问对象或类型的特征的成员，特征反映了状态  
 属性是字段的自然扩展  
 从命名上看，field更偏向于实例对象在内存中的布局，property更偏向于反映现实世界对象的特征  
 对外：暴露数据，数据可以是存储在字段里的，也可以是动态计算出来的  
 对内：保护字段不被非法值"污染"  
属性由Get/Set方法对进化而来   
```
class Student
{
  private int age;
  
  public int Age
  {
    get
    {
      return this.age;
     }

    set
    {
      if(value >= 0 && value <= 120)
      {
       this.age = value;
      } 
      else
      {
        throw new Exception("Age value has errot.");
      }
    }
   }
}
```
- 又一个"语法糖"--属性背后的秘密  
vs tools  
Developer Command Prompt for VS2013  
ildasm 反编译器  

	- 属性的声明  
	完整的声明  
	简略的声明  
	动态计算值的属性  
	注意实例属性和静态属性  
	属性的名字一定是名词  
	只读属性--只有getter没有setter  
	属性与字段的关系  
	一般情况下，它们都用于表示实体(对象或类型)的状态  
	属性大多数情况下是字段的包装器(wrapper)  
	建议:永远使用属性(而不是字段)来暴露数据，即字段永远都是private或privated的  

- 索引器  
什么是索引器，检索一个集合

## 18   
	扩展方法（this 参数）  
	方法必须是公有、静态的，即被public static所修饰  
	必须是形参列表中的第一个，由this修饰  
	必须由一个静态类（一般类名为SomeTypeExtension）来统一收纳对  
	SomeType类型的扩展方法  
	举例：LINQ方法  

## 19
	什么是委托
	委托（delegate） 是函数指针的升级版
	什么是函数指针
C语言实例：
```
#include<stdio.h>
typedef int(Calc*){int x, int y};

int Add(int x, int y)
{
  return x + y;
}

int Sub(int x, int y)
{
  return x - y;
}

int main（）
{
  int x = 100;
  int y = 200;
  int z = 0;

  Calc funcPoint1 = &Add;
  Calc funcPoint2 = &Sub;

  z = funcPoint1(x, y);
  printf("%d+%d=%d\n",x,y,z);

  z = funcPoint2(x, y);
  printf("%d+%d=%d\n",x,y,z);

  system("pause");
  return 0;
}
```
**一切皆地址**  
变量（数据）是以某个地址为起点的一段内存中所存储的值  
函数（算法）是以某个地址为起点的一段内存中所存储的一组机器语言指令  

直接调用：通过函数名来调用函数  
简介调用：通过函数指针来调用函数  

Java中没有与委托相对应的功能实体
Java从C++发展而来

C#通过委托保留了函数指针功能

- 常用委托类
```
Action
Func
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            //Action 类
            Calculator calculator = new Calculator();
            Action action = new Action(calculator.Report);
            calculator.Report();
            action.Invoke();
            action();

            //Func 类
            Func<int, int, int> func1 = new Func<int, int, int>(calculator.Add);
            Func<int, int, int> func2 = new Func<int, int, int>(calculator.Sub);

            int x = 100;
            int y = 200;
            int z = 0;

            z = func1.Invoke(x, y);
            Console.WriteLine(z);
            z = func2.Invoke(x, y);
            Console.WriteLine(z);
        }
    }

    class Calculator
    {
        public void Report()
        {
            Console.WriteLine("I have 3 methods.");
        }

        public int Add(int a, int b)
        {
            int result = a + b;
            return result;
        }
        
        public int Sub(int a, int b)
        {
            int result = a - b;
            return result;
        }
    }
}
```
	- 委托的声明（自定义委托）  
委托是一种类（class），类是数据类型，所以委托也是一种数据类型  
它的声明方式与一般的类不同，主要是为了照顾可读性和C/C++传统  

注意声明委托的位置  
    避免写错地方结果声明成嵌套类型  

委托与封装的方法必须“类型兼容”
```
delegate double Calc(double x,double y);
         double Add(double x, double y){ /* */}
         double Sub(double x, double y){ /* */}
         double Mul(double x, double y){ /* */}
         double Div(double x, double y){ /* */}
```
	     返回值的数据类型一致  
	     参数列表在个数和数据类型上一致  

- 委托的一般使用  
实例：把方法当作参数传给另一个方法  

	- 1、模板方法，“借用”指定的外部方法来产生结果  
	相当于“填空题”  
	常位于代码中部
	委托有返回值
	```
	using System;
	using System.Collections.Generic;
	using System.Linq;
	using System.Text;
	using System.Threading.Tasks;

	namespace practice
	{
		class Program
		{
			static void Main(string[] args)
			{
				ProductFactory productFactory = new ProductFactory();
				WrapFactory wrapFactory = new WrapFactory();

				Func<Product> func1 = new Func<Product>(productFactory.MakePizza);
				Func<Product> func2 = new Func<Product>(productFactory.MakeToyCar);

				Box box1 = wrapFactory.WrapProduct(func1);
				Box box2 = wrapFactory.WrapProduct(func2);

				Console.WriteLine(box1.Product.Name);
				Console.WriteLine(box2.Product.Name);
			}
		}

		class Product
		{
			public string Name { get; set; }
		}

		class Box
		{
			public Product Product { get; set; }
		}

		class WrapFactory
		{
			public Box WrapProduct(Func<Product> getProduct)
			{
				Box box = new Box();
				Product product = getProduct.Invoke();
				box.Product = product;
				return box;
			}
		}

		class ProductFactory
		{
			public Product MakePizza()
			{
				Product product = new Product();
				product.Name = "Pizza";
				return product;
			}

			public Product MakeToyCar()
			{
				Product product = new Product();
				product.Name = "Toy Car";
				return product;
			}
		}
	}
	```
	好莱坞方法  

	- 2、回调(callback)方法，调用指定的外部方法  
	相当于流水线  
	常位于代码末尾  
	委托无返回值  

	```
	using System;
	using System.Collections.Generic;
	using System.Linq;
	using System.Text;
	using System.Threading.Tasks;

	namespace practice
	{
		class Program
		{
			static void Main(string[] args)
			{
				ProductFactory productFactory = new ProductFactory();
				WrapFactory wrapFactory = new WrapFactory();

				Func<Product> func1 = new Func<Product>(productFactory.MakePizza);
				Func<Product> func2 = new Func<Product>(productFactory.MakeToyCar);
				//callback
				Logger logger = new Logger();
				Action<Product> log = new Action<Product>(logger.Log);
													//callback
				Box box1 = wrapFactory.WrapProduct(func1,log);
				Box box2 = wrapFactory.WrapProduct(func2,log);

				Console.WriteLine(box1.Product.Name);
				Console.WriteLine(box2.Product.Name);
			}
		}
		//日志//callback
		class Logger
		{
			public void Log(Product product)
			{
				Console.WriteLine("Product'{0}'created at{1},Price is {2}.",product.Name,
					DateTime.UtcNow,product.Price);
			}
		}

		class Product
		{
			public string Name { get; set; }
			public double Price { get; set; }
		}

		class Box
		{
			public Product Product { get; set; }
		}

		class WrapFactory
		{                                                  //callback
			public Box WrapProduct(Func<Product> getProduct,Action<Product> logCallback)
			{
				Box box = new Box();
				Product product = getProduct.Invoke();
				//callback
				if(product.Price >= 50)
				{
					logCallback(product);
				}
				box.Product = product;
				return box;
			}
		}

		class ProductFactory
		{
			public Product MakePizza()
			{
				Product product = new Product();
				product.Name = "Pizza";
				//callback
				product.Price = 12;
				return product;
			}

			public Product MakeToyCar()
			{
				Product product = new Product();
				product.Name = "Toy Car";
				//callback
				product.Price = 100;
				return product;
			}
		}
	}
	```
**注意：**  
难精通+易使用+功能强大   
缺点1：一种方法级别的紧耦合，现实工作中要慎之又慎  
缺点2：使可读性下降、debug的难度增加  
缺点3：把委托回调、异步调用和多线程纠缠在一起，会让代码变得难以阅读和维护  
缺点4：委托使用不当有可能造成内存泄漏和程序性能下降  

- 委托的高级使用  
	- 多播（multicast）委托（同步调用）  
	```
	using System;
	using System.Collections.Generic;
	using System.Linq;
	using System.Text;
	using System.Threading.Tasks;
	using System.Threading;

	namespace practice
	{
		class Program
		{
			static void Main(string[] args)
			{
				Student stu1 = new Student() { ID = 1, PenColor = ConsoleColor.Yellow };
				Student stu2 = new Student() { ID = 2, PenColor = ConsoleColor.Green };
				Student stu3 = new Student() { ID = 3, PenColor = ConsoleColor.Red };
				Action action1 = new Action(stu1.DoHomework);
				Action action2 = new Action(stu2.DoHomework);
				Action action3 = new Action(stu3.DoHomework);

				action1 += action3;
				action1 += action2;

				action1.Invoke();
			}
		}
		
		class Student
		{
			public int ID { get; set; }
			public ConsoleColor PenColor { get; set; }

			public void DoHomework()
			{
				for (int i = 0; i < 5; i++)
				{
					Console.ForegroundColor = this.PenColor;
					Console.WriteLine("Student{0}doing homework{1}hours.", this.ID, i);
					Thread.Sleep(1000);
				}
			}
		}
		
	}
	```
	- 隐式异步调用   
	同步与异步的简介  
	同步：你做完了我（在你的基础上）接着做  
	异步：咱们两个同时做（同步进行）  

		同步调用与异步调用的对比  
		每一个运行的程序是一个进程（process）  
		每个进程可以有一个或者多个线程（thread）  
		同步调用是在同一个线程内  
		异步调用的底层机理是多线程  
		串行==同步==单线程，并行==异步==多线程  

		隐式多线程 VS 显式多线程  
		直接调用：使用方法名  
		间接同步调用：使用单播/多播委托的Invoke方法  
		隐式异步调用：使用委托的beginInvoke  
		显式异步调用：使用Thread或Task  
	```
	using System;
	using System.Collections.Generic;
	using System.Linq;
	using System.Text;
	using System.Threading.Tasks;
	using System.Threading;

	namespace practice
	{
		class Program
		{
			static void Main(string[] args)
			{
				Student stu1 = new Student() { ID = 1, PenColor = ConsoleColor.Yellow };
				Student stu2 = new Student() { ID = 2, PenColor = ConsoleColor.Green };
				Student stu3 = new Student() { ID = 3, PenColor = ConsoleColor.Red };
				
				/*隐式异步调用
				Action action1 = new Action(stu1.DoHomework);
				Action action2 = new Action(stu2.DoHomework);
				Action action3 = new Action(stu3.DoHomework);
				
				action1.BeginInvoke(null, null);
				action2.BeginInvoke(null, null);
				action3.BeginInvoke(null, null);
				*/

				/*//显式异步调用
				Thread thread1 = new Thread(new ThreadStart(stu1.DoHomework));
				Thread thread2 = new Thread(new ThreadStart(stu2.DoHomework));
				Thread thread3 = new Thread(new ThreadStart(stu3.DoHomework));

				thread1.Start();
				thread2.Start();
				thread3.Start();
				*/
				//Task显式异步调用
				Task task1 = new Task(new Action(stu1.DoHomework));
				Task task2 = new Task(new Action(stu2.DoHomework));
				Task task3 = new Task(new Action(stu3.DoHomework));

				task1.Start();
				task2.Start();
				task3.Start();

				for(int i = 0; i < 10; i ++)
				{
					Console.ForegroundColor = ConsoleColor.Cyan;
					Console.WriteLine("Main thread{0}.", i);
					Thread.Sleep(1000);
				}
			}
		}
		
		class Student
		{
			public int ID { get; set; }
			public ConsoleColor PenColor { get; set; }

			public void DoHomework()
			{
				for (int i = 0; i < 5; i++)
				{
					Console.ForegroundColor = this.PenColor;
					Console.WriteLine("Student{0}doing homework{1}hours.", this.ID, i);
					Thread.Sleep(1000);
				}
			}
		}
		
	}
	```

	- 使用接口（inter）  
	```
	using System;
	using System.Collections.Generic;
	using System.Linq;
	using System.Text;
	using System.Threading.Tasks;
	using System.Threading;

	namespace practice
	{
		class Program
		{
			static void Main(string[] args)
			{
				//ProductFactory productFactory = new ProductFactory();
				IProductory pizzaFactory = new PizzaFactory();
				IProductory toycarFactory = new ToyCarFactory();
				WrapFactory wrapFactory = new WrapFactory();

				//Func<Product> func1 = new Func<Product>(productFactory.MakePizza);
			// Func<Product> func2 = new Func<Product>(productFactory.MakeToyCar);

				Box box1 = wrapFactory.WrapProduct(pizzaFactory);
				Box box2 = wrapFactory.WrapProduct(toycarFactory);

				Console.WriteLine(box1.Product.Name);
				Console.WriteLine(box2.Product.Name);
			}
		}

		interface IProductory
		{
			Product Make();
		}

		class PizzaFactory:IProductory
		{
			public Product Make()
			{
				Product product = new Product();
				product.Name = "Pizza";
				return product;
			}
		}

		class ToyCarFactory:IProductory
		{
			public Product Make()
			{
				Product product = new Product();
				product.Name = "Toy Car";
				return product;
			}
		}

		class Product
		{
			public string Name { get; set; }
		}

		class Box
		{
			public Product Product { get; set; }
		}

		class WrapFactory
		{
			public Box WrapProduct(IProductory productFactory)
			{
				Box box = new Box();
				Product product = productFactory.Make();
				box.Product = product;
				return box;
			}
		}
			
	}
	```
20
初步了解事件
事件的应用
深入理解事件
事件的声明
问题辨析

初步了解事件

定义：单词Event，译为“事件”、
通顺的解释就是“能够发生的什么事情”

角色：使对象或类具备通知能力的成员
“对象O拥有一个事件E”想表达的思想是：当事件E发生的时候，O有能力通知别的对象

使用：用于对象或类间的动作协调与信息传递（消息推送）

原理：事件模型（event model）中的两个“5”
“发生 -> 响应”中的5个部分--闹钟 响了 我 起床、孩子 饿了 我 做饭。。。这里隐含着“订阅”关系
“发生 -> 响应”中的5个动作--（1）我有一个事件 -> （2）一个人或者一群人关心我的这个事件 -> （3）我的这个事件发生了 -> （4）关心这个事件的人会被依次通知到 -> （5）被通知到的人根据拿到的事件信息（又称“事件数据”、“事件参数”、“通知”）对事件进行响应（又称“处理事件”）。

事件的订阅者
事件消息的接收者
事件的响应者
事件的处理者
被事件所通知的对象

(事件信息)
(事件消息)
(事件数据)
 事件参数

提示
事件多用于桌面、手机等开发的客户端编程，因为这些程序经常是用户通过事件来“驱动”的
MVC、MVP、MVVM等模式，事件模式更高级、更有效的“玩法”
Java的“事件”是使用接口来实现的

事件的应用
事件模型的五个组成部分
1、事件的拥有者（event source）
2、事件成员（event，成员）
3、事件的响应者（event subscriber）
4、事件处理器(event handler,成员)--本质上是一个回调方法
5、事件订阅--把事件处理器与事件关联在一起，本质上是一种以委托类型为基础的“约定”



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
//using System.Threading.Tasks;
//using System.Threading;
using System.Timers;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Timer timer = new Timer();
            timer.Interval = 1000;
            Boy boy = new Boy();
            Girl girl = new Girl();
            //事件订阅操作符 +=
            timer.Elapsed += boy.Action;
            timer.Elapsed += girl.Action;
            timer.Start();
            //程序停在这里
            Console.ReadLine();
        }
    }



    class Boy
    {
        internal void Action(object sender, ElapsedEventArgs e)
        {
            Console.WriteLine("Jump!");
        }
    }

    class Girl
    {

        internal void Action(object sender, ElapsedEventArgs e)
        {
            Console.WriteLine("Sing!");
        }
    }

}

1星
最经典的
事件的拥有者和事件的响应者是独立的

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
//using System.Threading.Tasks;
//using System.Threading;
//using System.Timers;
using System.Windows.Forms;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
              //事件拥有者
            Form form = new Form();
                     //事件响应者
            Controller controller = new Controller(form);
        }
    }

    class Controller
    {
        private Form form;

        public Controller(Form form)
        {
            if(form != null)
            {
                this.form = form;
                       //事件 //事件订阅
                this.form.Click += this.FormClicked;
            }
        }
                   //事件处理器
        private void FormClicked(object sender, EventArgs e)
        {
            this.form.Text = DateTime.Now.ToString();
        }
    }

}

2星
事件的拥有者同时也是事件的响应者
拿着自己的方法去订阅和处理自己的事件
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            //事件拥有者 事件响应者
            MyForm form = new MyForm();
            //事件  事件订阅
            form.Click += form.FormClick;
            
        }

    }
		//派生 继承
    class MyForm:Form
    {
                     //事件处理器
        internal void FormClick(object sender, EventArgs e)
        {
            this.Text = DateTime.Now.ToString();
        }
    }

}

3星
事件的拥有者是事件响应者的一个字段成员
事件响应者用自己的方法订阅着自己字段成员的某个事件
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {        //事件响应者
            MyForm form = new MyForm();
            form.ShowDialog();
        }
    }

    class MyForm:Form
    {
        private TextBox textBox;
                    //事件拥有者
        private Button button;

        public MyForm()
        {
            this.textBox = new TextBox();
            this.button = new Button();
            this.button.Text = "click me";
            this.button.Top = 50;
            this.Controls.Add(this.button);
            this.Controls.Add(this.textBox);
                     //事件  事件订阅
            this.button.Click += this.ButtonClicked;
        }
                   //事件处理器
        private void ButtonClicked(object sender, EventArgs e)
        {
            this.textBox.Text = "Hello, World！！！！！！！！！！！！！！！！!";
        }
    }
}


事件的声明

完整声明
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Threading;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Customer customer = new Customer();
            Waiter waiter = new Waiter();
            customer.Order += waiter.Action;

            customer.Action();
            customer.PayTheBill();
        }
    }

    public class OrderEventArgs:EventArgs
    {
        public string DishName{get;set;}

        public string Size{get;set;}
    }

    public delegate void OrderEventHandler(Customer customer,OrderEventArgs e);

    public class Customer
    {
        private OrderEventHandler orderEventHandler;

        public event OrderEventHandler Order
        {
            add
            {
                this.orderEventHandler += value;
            }

            remove
            {
                this.orderEventHandler -= value;
            }
        }

        public double Bill { get; set; }

        public void PayTheBill()
        {
            Console.WriteLine("I will pay ${0}.", this.Bill);
        }

        public void WalkIn()
        {
            Console.WriteLine("Walk into the restaurant.");
        }

        public void  SitDown()
        {
            Console.WriteLine("Sit down.");
        }

        public void Think()
        {
            for(int i = 0; i < 5; i++)
            {
                Console.WriteLine("Let me think ...");
                Thread.Sleep(1000);
            }

            if(this.orderEventHandler != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.orderEventHandler.Invoke(this, e);
            }
        }

        public void Action()
        {
            Console.ReadLine();
            this.WalkIn();
            this.SitDown();
            this.Think();
        }
    }

    public class Waiter
    {

        internal void Action(Customer customer, OrderEventArgs e)
        {
            Console.WriteLine("I will serve you the dish - {0}.", e.DishName);
            double price = 10;
            switch (e.Size)
            {
                case "small":
                    price = price * 0.5;
                    break;
                case "large":
                    price = price * 1.5;
                    break;
                default:
                    break;
            }

            customer.Bill += price;
        }
    }
}

事件简单声明
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Threading;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Customer customer = new Customer();
            Waiter waiter = new Waiter();
            customer.Order += waiter.Action;

            customer.Action();
            customer.PayTheBill();
        }
    }

    public class OrderEventArgs:EventArgs
    {
        public string DishName{get;set;}

        public string Size{get;set;}
    }

    public delegate void OrderEventHandler(Customer customer,OrderEventArgs e);

    public class Customer
    {
        /*
        private OrderEventHandler orderEventHandler;

        public event OrderEventHandler Order
        {
            add
            {
                this.orderEventHandler += value;
            }

            remove
            {
                this.orderEventHandler -= value;
            }
        }
        */
        // 事件简单声明
        public event OrderEventHandler Order;

        public double Bill { get; set; }

        public void PayTheBill()
        {
            Console.WriteLine("I will pay ${0}.", this.Bill);
        }

        public void WalkIn()
        {
            Console.WriteLine("Walk into the restaurant.");
        }

        public void  SitDown()
        {
            Console.WriteLine("Sit down.");
        }

        public void Think()
        {
            for(int i = 0; i < 5; i++)
            {
                Console.WriteLine("Let me think ...");
                Thread.Sleep(1000);
            }
            /*
            if(this.orderEventHandler != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.orderEventHandler.Invoke(this, e);
            }
             */
            if (this.Order != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.Order.Invoke(this, e);
            }
        }

        public void Action()
        {
            Console.ReadLine();
            this.WalkIn();
            this.SitDown();
            this.Think();
        }
    }

    public class Waiter
    {

        internal void Action(Customer customer, OrderEventArgs e)
        {
            Console.WriteLine("I will serve you the dish - {0}.", e.DishName);
            double price = 10;
            switch (e.Size)
            {
                case "small":
                    price = price * 0.5;
                    break;
                case "large":
                    price = price * 1.5;
                    break;
                default:
                    break;
            }

            customer.Bill += price;
        }
    }
}

有了委托字段/属性，为什么还需要事件？
为了程序的逻辑更加“有道理”、更加安全，谨防“借刀杀人”

事件的本质是委托字段的一个包装器
这个包装器对委托字段的访问起限制作用，相当于一个“蒙板”
封装（encapsulation）的一个重要功能就是隐藏
事件对外界隐藏了委托实例的大部分功能，仅暴露添加/移除事件处理器的功能

用于声明事件的委托类型的命名约定
用于声明Foo事件的委托，一般命名为FooEventHandler（除非是一个非常通用的事件约束）
FooEventHandler委托的参数一般有两个
第一个是object类型，名字为sender，实际上就是事件的拥有者、事件的source
第二个是EventArgs类的派生类，类名一般为FooEventArgs，参数名为e。也就是前面讲过的事件参数
虽然没有官方的说法，但我们可以把委托的参数列表看做是事件发生后发送给事件响应者的“事件消息”
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Threading;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Customer customer = new Customer();
            Waiter waiter = new Waiter();
            customer.Order += waiter.Action;

            customer.Action();
            customer.PayTheBill();
        }
    }

    public class OrderEventArgs:EventArgs
    {
        public string DishName{get;set;}

        public string Size{get;set;}
    }

    public delegate void OrderEventHandler(Customer customer,OrderEventArgs e);

    public class Customer
    {
        /*
        private OrderEventHandler orderEventHandler;

        public event OrderEventHandler Order
        {
            add
            {
                this.orderEventHandler += value;
            }

            remove
            {
                this.orderEventHandler -= value;
            }
        }
        */
        // 事件简单声明
        //public event OrderEventHandler Order;

        //厂商给的声明事件的委托类型
        public event EventHandler Order;

        public double Bill { get; set; }

        public void PayTheBill()
        {
            Console.WriteLine("I will pay ${0}.", this.Bill);
        }

        public void WalkIn()
        {
            Console.WriteLine("Walk into the restaurant.");
        }

        public void  SitDown()
        {
            Console.WriteLine("Sit down.");
        }

        public void Think()
        {
            for(int i = 0; i < 5; i++)
            {
                Console.WriteLine("Let me think ...");
                Thread.Sleep(1000);
            }
            /*
            if(this.orderEventHandler != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.orderEventHandler.Invoke(this, e);
            }
             */
            if (this.Order != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.Order.Invoke(this, e);
            }
        }

        public void Action()
        {
            Console.ReadLine();
            this.WalkIn();
            this.SitDown();
            this.Think();
        }
    }

    public class Waiter
    {

        internal void Action(object sender, EventArgs e)
        {
            // 改写了Action 的参数列表，并进行了强制类型转换
            Customer customer = sender as Customer;
            OrderEventArgs orderInfo = e as OrderEventArgs;
            Console.WriteLine("I will serve you the dish - {0}.", orderInfo.DishName);
            double price = 10;
            switch (orderInfo.Size)
            {
                case "small":
                    price = price * 0.5;
                    break;
                case "large":
                    price = price * 1.5;
                    break;
                default:
                    break;
            }

            customer.Bill += price;
        }
    }
}

触发Foo事件的方法一般命名为OnFoo，即“因何引发”、“事出有因”
访问级别为protected，不能为public，不然又成了可以“借刀杀人”

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Threading;

namespace practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Customer customer = new Customer();
            Waiter waiter = new Waiter();
            customer.Order += waiter.Action;

            customer.Action();
            customer.PayTheBill();
        }
    }

    public class OrderEventArgs:EventArgs
    {
        public string DishName{get;set;}

        public string Size{get;set;}
    }

    public delegate void OrderEventHandler(Customer customer,OrderEventArgs e);

    public class Customer
    {
        /*
        private OrderEventHandler orderEventHandler;

        public event OrderEventHandler Order
        {
            add
            {
                this.orderEventHandler += value;
            }

            remove
            {
                this.orderEventHandler -= value;
            }
        }
        */
        // 事件简单声明
        //public event OrderEventHandler Order;

        //厂商给的声明事件的委托类型
        public event EventHandler Order;

        public double Bill { get; set; }

        public void PayTheBill()
        {
            Console.WriteLine("I will pay ${0}.", this.Bill);
        }

        public void WalkIn()
        {
            Console.WriteLine("Walk into the restaurant.");
        }

        public void  SitDown()
        {
            Console.WriteLine("Sit down.");
        }

        public void Think()
        {
            for(int i = 0; i < 5; i++)
            {
                Console.WriteLine("Let me think ...");
                Thread.Sleep(1000);
            }

            this.OnOrder("Kongpao Chicken", "large");
            /*
            if(this.orderEventHandler != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.orderEventHandler.Invoke(this, e);
            }
             */
            /*
            if (this.Order != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = "KongPao Chicken";
                e.Size = "large";
                this.Order.Invoke(this, e);
            }
             */
        }
        //一个方法只做一件事
        protected void OnOrder(string dishName,string size)
        {
            if(this.Order != null)
            {
                OrderEventArgs e = new OrderEventArgs();
                e.DishName = dishName;
                e.Size = size;
                this.Order.Invoke(this, e);
            }
        }

        public void Action()
        {
            Console.ReadLine();
            this.WalkIn();
            this.SitDown();
            this.Think();
        }
    }

    public class Waiter
    {

        internal void Action(object sender, EventArgs e)
        {
            // 改写了Action 的参数列表，并进行了强制类型转换
            Customer customer = sender as Customer;
            OrderEventArgs orderInfo = e as OrderEventArgs;
            Console.WriteLine("I will serve you the dish - {0}.", orderInfo.DishName);
            double price = 10;
            switch (orderInfo.Size)
            {
                case "small":
                    price = price * 0.5;
                    break;
                case "large":
                    price = price * 1.5;
                    break;
                default:
                    break;
            }

            customer.Bill += price;
        }
    }
}


事件的命名约定
带有时态的动词或者动词短语
事件拥有者“正在做”什么事情，用进行时，事件拥有者“做完了”什么事情，用完成时

为什么要使用委托类型来声明事件？
站在source的角度来看，是为了表明source能对外传递哪些消息
站在subscriber的角度来看，它是一种约定，是为了约束能够使用什么样签名的方法来处理（响应）事件
委托类型的实例将用于存储（引用）事件处理器

对比事件与属性
属性不是字段--很多时候是字段的包装器，这个包装器用来保护字段不被滥用
事件不是委托字段--它是委托字段的包装器，这个包装器用来保护委托字段不被滥用
包装器永远都不可能是被包装的东西


23  
类声明  
- 类修饰符 *class-modifier*  
```
new
public
protected
internal
private
abstract
sealed
static
```

24  
- 是一个 is  子类的实例是基类的实例  
小知识点  
1、sealed关键字  封闭类  
2、一个类最多有一个基类但是可以实现多个基接口  
C++一个类可以有多个基类，菱形继承？？？  
3、子类的访问级别不能超过父类的访问级别  
internal 访问级别，程序集级别  

- 继承的本质  
派生类在基类已有的成员的基础之上，对基类进行的横向和纵向上的扩展  
只能扩展不能删减  
横向 类成员在数量上的扩充  变胖了  
纵向 对类成员的版本进行扩充 旧版本在上，新版本在下   


- 静态语言  
c++ c# java  

- 动态语言  
Python JavaScript  

1、  
base 和 this   
base 向上一级  

2、  
实例构造器是不被继承的  

3、类成员的访问级别  
类成员的访问级别是以类的访问级别为上限的  
internal 访问级别，程序集级别  
private 最低的访问级别，类的类体里  默认的访问级别  
protected 子类可以调用 跨程序集的  
internal protected 程序集和子类都可以调用  

- 面向对象的实现风格  
Class-based  
Prototype-based  JavaScript  