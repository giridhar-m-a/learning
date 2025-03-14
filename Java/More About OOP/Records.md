- Records are used to store data 
- Records are used only to transfer data

```java
public record Records(String name, int age){}

public class Main{
	public static void main( String []args){
		//Records 
		Records rec = new Records("name", 20);
		System.out.println("record: "+ rec);
	}
}
```