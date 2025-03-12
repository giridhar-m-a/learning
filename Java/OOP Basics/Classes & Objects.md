### Class
- classes are the blueprint of an object
- class should be defined as an single entity


### Objects 
- objects are instances of an class
- To declare an object

```java
public class Main{
	public static void main( String []args){
		Student student = new Student()
		student.setName("name")
	}
}

public class Student{
	private String name
	private Int std

	public void setName(String Name){
		this.name = name
	}

	public String getName(){
		return this.name
	}
}
```

