package interface1;

public interface Animal {
	//interface is  the blueprint for the class
	//in interface there is only abstract method
	//in interface we can write static constant
	//static is not related to object it is related to class
	public static final int MAX_AGE=150;
	//same no need to write pulic static and final because they are already
	//there are 2 uses of interface to achieve 100%abstraction and multiple inheritence
	public abstract void eat();
	//no need to write public abstract because it is already public and abstract in interface
	void sleep();
	
	//why static method ?
	//it increase fuctionality 
	//complex business 1000 of interface through static method we can give the info of particular interface
	//it is for interface only 
	//easier code no need for writing public ,and adding static keyword in interface
	//it already so you cann write directly

	public static void info() {
		System.out.println("animal is an interface");
		//interface and abstract method can not have body if we remove static
		//if we remove static that means we are creating a method for instance
		//but we know that interface can not be instanciate (we cant create the object constructor of interface because of abstract method)
		//becasue abstraact method have no implimentation
	}


//we can  not create the object of interface because there is no implimentation 
//interface cannot instantiate
//no constructor 
//in java 8 interfaces can have static method and default method also





//diff between abstract and static method in the interface
//if we create any abstract method in interface other classes implemented classes will show warning that impliment this newly made method 
//but we create static method there is no warning 
//can only accessed by that interface using . operator



//default method in interface 
//this is after java 8 so set new version jdk
//default keyword -----
	public default void run () {
		this.eat();// when dog.run then this.run refer dog  //when cat.run then this.run refer cat
		System.out.println(" animal is running");
	}
	// default method benefits
	//if we create deault method then impliment keyword access this default keyword 
	// and other class can access by making an object and by calling with the object
	//access by impliment class default
	//but abstract method will show error 
	
	//interface have -default methods,abstract methods,static methods,static constant
	//interface 2 use case - pure abstraction, multiple inheritence
	
}
