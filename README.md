# SIngleton


In object-oriented programming, a singleton class is a class that can have only one object
(an instance of the class) at a time. After first time, if we try to instantiate the Singleton class,
the new variable also points to the first instance created.




# ---------------- This is Java Code ---------------------


# Singleton class
 
package firstproject;
 
public class Singleton {
    
    private static Singleton s=new Singleton();
    private Singleton(){
        
    }
    
    public static Singleton getSingleton(){
        return s;
    }
    
}


# TextSingleton
  
 
        package firstproject;

                        public class TextSingleton {
                            private static TextSingleton t=null;
                            private TextSingleton(){}
                            public static TextSingleton getInstance(){
                                if(t  != null){
                                } else {
                                    t=new TextSingleton();
                                }

                                return t;
                            }

                        }


# MainClass Of the Project.
 
package firstproject;


 
 
 
public class FirstProject {

    private static Singleton s,s1;
    private static TextSingleton t,t1;

    
    public static void main(String[] args) {
       
        s=Singleton.getSingleton();
        s1=Singleton.getSingleton();
        
        t=TextSingleton.getInstance();
        t1=TextSingleton.getInstance();
       
       if(s!=null){
           System.out.println(s.toString());
           System.out.println(s1.toString());
           
            } 
       
        else
            System.out.println("not instantiated");System.out.println(t.toString());
           System.out.println(t1.toString());
    }
    
}
