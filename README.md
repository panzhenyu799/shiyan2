# 计192 2019311237 潘振宇
# shiyan2
Java课程作业项目仓库
# 阅读程序
## 实验目的
1.初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
2.掌握面向对象的类设计方法（属性、方法）；
3.掌握类的继承用法，通过构造方法实例化对象；
4.学会使用super()，用于实例化子类；
5.掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。
## 实验要求
说明：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择“课程”。从简化系统考虑，每名教师仅教授一门课程，每门课程的授课教师也仅有一位，每名学生选仅选一门课程。
对象示例：	人员（编号、姓名、性别、学号）
教师（编号、姓名、性别、工号、所授课程）
学生（编号、姓名、性别、学号、所选课程）
课程（编号、课程名称、上课地点、时间、授课教师）

## 实验过程
1.创建两个包，第一个包下创建people、course、teacher、student四个类，第二个包下创建Test主类。  
2.People类：
在People类中创建属性：
编号num，姓名name，学号id，性别sex，储存stuNo。  
3.Course类：
继承people中的属性并且新增地址属性，构造方法，实现编号、姓名、地址、课程数的说明。利用stuNo实现数目的加减。
4.Teacher类：
继承people类中的num和sex，加入teacherName和teacherId属性。构造方法，实现编号、性别、姓名、授课的说明。     
5.Student类：
继承people类中的num和sex，加入studentName和studentId属性。构造方法，实现编号、性别、姓名、选课的说明。
6.Test类:
调用Course、Teacher、Student类，进行信息输入。构造方法judge.进行判断，add.h和reduce.进行数目的加减。利用print进行打印。
## 核心方法  

1.方法1（Course属性）
```
public Course(int number,String name,String add,int stuNo){
	setNo(number);
	setName(name);
	setAdd(add);
	setStuNo(stuNo);
	}

``` 
2.方法2（数目增减）
```
public void addStuNo(int stuNo) {
	super.stuNo = stuNo+1;
}
public void reduceStuNo(int stuNo) {
	super.stuNo = stuNo-1;
}
	   
``` 
3.方法3（Teacher属性）
```
public Teacher(int number,String name,String sex,String id,String course){
	setNo(number);
	setTeacherName(name);
	setTeacherSex(sex);
	setTeacherId(id);
	setTeaCourse(course);
``` 
4.方法4（打印TeacherName）
```
public String getTeacherName(){
	return teacherName;	
}
void setTeacherName(String teacherName) {
	this.teacherName = teacherName;
}
```
5.方法5（Student属性）
```
public Student(int number,String name,String sex,String id,int course){
	setNo(number);
	setStudentName(name);
	setStudentSex(sex);
	setStudentId(id);
	setCourses(course);
	}
```
6.方法6（课程数目增减）
```
public void addCourses(int courseNumber) {
	this.courseNumber = courseNumber+1;
}
public void reduceCourses(int courseNumber) {
	this.courseNumber = courseNumber-1;
}
```
7.方法7（Test方法）
```
public static void main(String[] args) {
		 
		c: for(;;) {
			printStudentAll();
			Scanner reader = new Scanner(System.in);
			int x =reader.nextInt();
			stuNo=x;
			judgeStu(x);
			
			System.out.println("1.继续选课\n2.结束选课");
			int y =reader.nextInt();
			if (y==2)
				break c;
		}
	printAll();	
	}
```
8.方法8（课程选择）
```
public static void courseChoose(int No) {
		Scanner reader = new Scanner(System.in);
		if(No==1) {
			printTeacher(1);
		   
	}
		if(No==2) {
			printTeacher(2);
		
	}
```
9.方法9（系统打印）
```
public static void printAll() {
		System.out.println("----------------------------------");
		System.out.println("<学生选课系统>");
		System.out.println("<学生信息>");
		System.out.println("编号   姓名   性别   学号   课数");
		System.out.println("  "+stu.getNo()+"    "+stu.getStudentName()+"   "+stu.getStudentSex()+"   "+stu.getStudentId()+"   "+stu.getCourses());
		printTeacherAll();
		printCourseAll();
	}
```
## 流程图 
![1]()
## 实验结果
![1](https://github.com/panzhenyu799/shiyan2/blob/main/1603639333(1).jpg)
## 实验感想  
通过这次实验，我深深体会到了编程的探索性，无论哪一种语言，不去下功夫，不去花时间学，仅仅依靠课上时间是远远不够的。要靠自己平日里不断地钻研，不断摸索，从一个个错误中成长，只想着浑水摸鱼，坐享功成是不可能的。编程的过程可以从中发掘自己的乐趣，也可以收获成就感。要学会使用其他资料帮助学习，还可以找一个一起学习的人互相帮助，互相竞争。只有坚定信念，才可以不断进步。
