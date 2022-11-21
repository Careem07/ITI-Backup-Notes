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
 
 - If virtual keyword only in parent (Rect) and the pointer from grandparent (geoShape) point to child (square) this is not dynamic binding
  
geoShape*p = &Square s => implement from geoShape. 
 
 Rect *p = & Square s => implement from Square. 
 
 geoShape*p = &Rect r => implement from geoShape.
 
 
 - Rectangle r = r2  -> copy constructor
 
   Rectangle r;
 
   r = r2           -> Assignment operator
 - Protected Class -> functions and attributes cannot be accessed in main just inside class
 
 - function(Complex x) -> calls copy constructor for parameters
   function(Complex &x) -> pass by reference no call for copy constructor
 
 - to return array from function return as pointer if array declared in the function should be static
 
     int *display(){
 
                int arr[50] = {0}; //error should be static int arr[50]
 
                return arr;
          }
 
    why => because if it's not static its scope will be end with end of function so should be static to put it in heap memory not in stack 
