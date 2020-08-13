Constructor is a special member function, these are used to initialize the values of objects. When we create a object using the ```new()``` keyword atleast one constructor will be executed to assign initial values to that object.

#### example:

```java
public class Example {
	int a;
	public Example () {
		a = 10;
	}
	public static void main (String[] args) {
		Example ob = new Example();
		System.out.println(ob.a);
	}
}
// output 10
```

### Rules for creating constructor

- All constrcutors of a class must have same name as the class in which it is created
- A constructor in java cannot be abstract, final and static
- Constructors don't have a return type

### Types of constructors

There are 2 types of constructors in java

- Default constructor
- Parameterized constructor

#### 1. Default constructor

- it has 0 parameters
- If we don't create a constructor then the compiler itself a creates a default constructor
- If we create atleast one constructor then the compiler won't do it for us

#### example

```java
class Example {
	public Example () {
		System.out.println("constructor created");
	}
	public static void main (String[] args){
		Example ob = new Example ();
	}
}
// output: constructor created
```

#### 2. Parameterized Constructor

- it has more than 0 parameters
- Iused to provode different values to different objects

#### example

```java
class Example {
	int a,b;
	public Example (int x, int y) {
		a = x;
		b = y;
	}
	public void add () {
		System.out.println(a+b);
	}
	public static void main (String[] args){
		Example ob = new Example (2,3);
		ob.add();
	}
}
// output: 5
```

#### Constructor overloading

If we use more than 1 constructor in a class, then it is said to be constructor overloading.

```java
class Example {
	int a,b,c;
	public Example (int x) {
		a = x;
	}
	public Example (int y, int z) {
		b = y;
		c = z;
	}
	public void add () {
		System.out.println(a+b+c);
	}
	public static void main (String[] args){
		Example ob1 = new Example (20,30);
		Example ob2 = new Example (5);
		ob1.add();
		ob2.add();
	}
}
// output:
50
5
```
