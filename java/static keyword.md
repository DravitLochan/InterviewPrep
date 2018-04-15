# static keyword

static is used to access a member without instatiating an object of a class.
<br>

- **static variable**<br>
A static variable is a class variable which can be :
	- act as global variables.
	- accessed w/o initializing class object.
	- a single shared copy of the same variable is made.
	- executed in the order they are present in the program.

	example : 
	```
	class StaticVariable{
		static int lucky_number = staticMethod();
		...
		static int staticMethod(){
			System.out.println("static method!\n");
			return 69;
		}
		...
		void someRandomMethod(){
			lucky_number = 6969;
			System.out.println("lucky number is now " + lucky_number);
		}
		...
	}
	```

- **static block**<br>
we can add a *staitc block* in our class. It will add a block of code which will be executed only once, when the class is compiled.

	example : 
	```
	class StaticBlock{
		...
		static {
			System.out.println("static block executed!");
		}
		...
	}
	```


- **static method**<br>
following prperties :
	- can make direct calls to only static members, irrespective of data or a method.
	- cannot use `this` or `super`.


- **static class**<br>
	- no enclosing class can be static.
	- only an inner (nested) class can be defined as static.
	- while using inner static class, reference to enclosing class is not needed.
	- can only access static members of enclosing class.