```java 

public enum Result {
    pass, fail;
}

public class Main{
	public static void main( String []args){
		//Enum
		Result r = Result.pass;
		System.out.println("Result: "+r); // prints pass
		System.out.println("Result ordinal: "+r.ordinal()); // prints o (position of the variable)
	}
}

```