# Experiment---12 

#### Aim 
To study and implement Constructors and Destructors. 

#### Software 
Visual Studio Code 

#### Theory 
Constructors: <br>  
A constructor is a member functoin of a class that has the same name as the class name. <br>  
It helps to initialize the object of a class. <br> 
It is called whenever an instance of the class is created. <br> 
Constructors are mostly declared inthe pulic section of the class though it can be declared  in the private section of the class. <br> 
Constructors can be overloaed. <br> 
They can be defined inside or outside the class declaration.<br> 
They are classified into three types - (1) Default Constructor, (2) Parameterized Constructor and (3) Copy Constructor. <br>  

Destructors: <br> 
A destructor is also a specialmember function like a constructor. Destructor destroys the class objects created by the constructor. <br> 
Destructor has the same name as their class name preceded by a tilde (~) symbol. <br> 
It is not possible to define more than one destructor. <br> 
Destructor cannot be overloaded. <br>  
Destructor neither requires any argument nor returns any value. <br> 
It is automatically called when an object goes out of scope. <br> 
Destructor release memory space occupied by the objects created by the constructor. Objectsaredestroyedc in the reverse  of an object creation. <br>  

#### Code 

(A) <br> 
```
// NAME - SHLOKA PATEL 
// PRN- 23070123120 
// EXPERIMENT - 12(A) 

#include<iostream> 
#include<string>
using namespace std; 
class Data {
    string name;
    int roll_no;
    char dept[50];
    char division;

    public:
    Data() {
        cout<<"Name: ";
        cin>>name;
        cout<<"Roll Number: ";
        cin>>roll_no;
        cout<<"Department: ";
        cin>>dept;
        cout<<"Division: ";
        cin>>division;
    }
    void display() {
        cout<<"\n"<<"DETAILS:"<<"\n"<<name<<"  "<<roll_no<<"  "<<dept<<"  "<<division<<"\n";
    }
};
int main() 
{
    Data d1;
    d1.display();
} 

```

(B) <br> 
```
// NAME - SHLOKA PATEL 
// PRN - 23070123120 
// EXPERIMENT - 12(B)

#include<iostream>
using namespace std;
class Num
{
    public:
    Num(int c, int d)
    {
        if(c>d)
        {
            cout<<c<<" is greater.";
        }
        else 
        {
            cout<<d<<" is greater.";
        }
    }
};
int main()
{
    Num n1(4,3);
} 
```

(C) <br> 
```
// NAME - SHLOKA PATEL 
// PRN - 23070123120 
// EXPERIMENT - 12(C) 

#include<iostream>
using namespace std;
int count=0;
class destruct{
    public:
    destruct()
    {
        count++;
        cout<<"Number of objects created: "<<count<<"\n";
    }
    ~destruct()
    {
        count--;
        cout<<"Number of objects destroyed: "<<count<<"\n";
    }
};
int main()
{
    destruct aa,bb,cc;
    {
        destruct dd;
    }
    return 0;
} 
```

#### Output  

(A) <br>  
![](https://github.com/Shloka-Patel/Experiment---12/blob/main/Output_12A.png) 

(B) <br> 
![](https://github.com/Shloka-Patel/Experiment---12/blob/main/Output_12B.png) 

(C) <br> 
![](https://github.com/Shloka-Patel/Experiment---12/blob/main/Output_12C.png) 

#### Conclusion 
I learnt about constuctors and its types, destructors and performed various programs based on that. <br>            
