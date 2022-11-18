# ITI-Backup-Notes

# OOP C 

 -Template class creates a new class with passed datatype
  eg : Stack<int> , Stack<float> it creates 2 new classes with different datatypes
   
 - Method Hiding Vs Method overriding 
  if Child inherit from parent 
   Parent{
   
   void func()
  virtual void f()
 }
 Child{
  void f()
  void func()
 }
 Method hiding -> according to object we call the func()
 Method overriding -> call f() directly
 - Static variables can be used by non-static methods but static methods use ONLY static variables 
 - void method(int parmater1){}
   void method(float parameter2){}
   calling the method with float parameter2 raises an error: call of overloaded ‘method(double)’ is ambiguous
   but calling the method with int parameter is fine
