# ITI-Backup-Notes

# OOP C 

-Template class creates a new class with passed datatype
eg : Stack<int> , Stack<float> it creates 2 new classes with different datatypes
  
  
 - Method Hiding Vs Method overriding 
 - Static variables can be used by non-static methods but static methods use static variables ONLY
 - If virtual in parent (Rect) and the pointer from grand parent(geoShape)point to child this not dynamic binding
  geoShape*p = &Square s => implement from geoShape. 
  Rect *p = & Square s => implement from Square. 
  geoShape*p = &Rect r => implement from geoShape. 
