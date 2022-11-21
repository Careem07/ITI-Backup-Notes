# ITI-Backup-Notes
# C/CPP Notes
# Constructor

//class
complex(float r){}
complex(float r,float i){}

//main
Complex comp(); → error no default constructor

# Destructor 

- Only one destructor in class
- Last behavior in object life cycle
- Deallocate resources 

# Inline function

- Method implementation in class
- Simple method no loops
- Like text replacement

# Copy constructor

- Shallow(default) - deep (user creation)
- Call by value
- Return by value
- Create object from another object (=)
- Classname classname(classname &obj ){ }

# Example what happen when call,return by value and create object

//class
Complex add(complex c) //call by value , call copy constructor
{
Complex temp; //create temp object, call default constructor
temp.real=this->real+c.real; 
// c.real and real private member with no error because implementation in class
temp.img=img+c.img;
Return temp; // return by value,call copy constructor
}
//After call ending
//Call destructor for temp
//Call destructor for arguments 

//main
Complex c1,c2,c4;
Complex c3=c2.add(c1);   
//optimization create c3 object and assign return in it
//consider the return object is c3. So doesn’t destruct it 

//take return then call destructor for copy, doesn't need this object anymore
c4=c2.add(c1);               
or
c2.add(c1);		 

C2.real; // error not accessible

# Static members

- One copy in class, shared by all members 
- Instance members can deal with static members, and not virus wise.
- Because, static members in memory once class creation and terminate at the end of program, before any object creation so how do static members deal with members that don't exist ? 

//class

1)error can’t initialize a class member here 
Static int counter=0; 
Or 
Int size=10;

2)Must initialize outside the class using scope operators ::
If not initialize it will cause linker error

Int Stack::counter=0;

//main 
stack::counter=0 // error not accessible (private)

4) must call public members in main
Stack::getCounter();

# Friend function

- Stand alone function
- Can access all private members

# Dynamic area problem

- When object create dynamic allocation and call by value 
- When return from method destructor of shallow copy will deallocate this area
- If in destructor delete [] ptr;

# overloading
//class
Return Complex(real+c.real,img+c.img); // create temp object then return it without destroy it

//main
Complex c1,c2,c3
Complex c4=c1+c2 //return object will be c4 and don’t destroy it
c3=c1+c2; //take object in c3 then destroy return object
