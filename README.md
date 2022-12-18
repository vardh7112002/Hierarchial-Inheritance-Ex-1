# Hierarchial-Inheritance-Ex-1

//import java.util.Scanner; 

class A{
    
    private int x;
    A ()
    {
        x=1;
    }

    A (int x)
    {
        this.x=x;
    }

/*    void getdata ()
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter value of x: ");
        x=sc.nextInt();
    }
*/    
    void display ()
    {
        System.out.println(x);
    }
    
} 
    
class B extends A { 
        private int y;
        
        B(){ 
           super(); // optional
           y=0;
       }

    B(int x,int y)
    {
        super(x);    //Compulsory
        this.y=y;
    }

/*    void getdata()
    {
        super.getdata();
        Scanner sc= new Scanner(System.in);
        System.out.print("Enter value of y: ");
        y=sc.nextInt();
    }
*/
    void display()
    {
        super.display();
        System.out.println(y);
    }

        
}


class C extends A {
    private int z;
    C(){
        super();        //optional
        z=0;
    }
    C(int x,int z)
    {
        super(x);    //Compulsory
        this.z=z;
    }

 /*   void getdata()
    {
 //       super.getdata();
        Scanner sc= new Scanner(System.in);
        System.out.print("Enter value of z: ");
        z=sc.nextInt();
    }
 */
 
    void display()
    {
        super.display();        //Compulsory
        System.out.println(z);
    }
    
}

    public class ABCTest {

    public static void main(String args[]) {

    C c1 = new C(5,15);
    c1.display();
    B b1 = new B(5,10);
    b1.display();
    C c2 = new C();
    c2.display();
    B b2 = new B();
    b2.display();
    A a1 = new A(5);
    a1.display();
    A a2 = new A();
    a2.display();
    }
}
