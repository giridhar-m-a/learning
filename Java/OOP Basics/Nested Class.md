- A class inside a class

```java
public class Main{

    public static void main( String []args){

        Student student = new Student();
        student.setName("name");

        Student.Score score = student.new Score("maths", 95);
        score.show();
    }
}

public class Student{

    private String name;
    private static int std = 10;

    public void setName(String name){
            this.name = name;
    }

    public String getName(){
        return this.name;
    }

  
    public int getStd(){
        return std;
    }

    class Score{
        private String subjectName;
        private int mark;
        
        Score(String subjectName, int mark ){
            this.subjectName = subjectName;
            this.mark = mark;
        }
        
        public void show(){
            System.out.println("Subject :" + subjectName +"\nMark : " + mark);
        }
    }
}
```