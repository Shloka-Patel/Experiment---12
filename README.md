# Experiment---12 

#### Aim 
To study and implement Constructors and Destructors. 

#### Software 
Visual Studio Code 

#### Theory 
Constructors -> A constructor is a member functoin of a class that has the same name as teh class name. <br>  
It helps to initialize the object of a class. <br> 
It is called whenever an instance of the class is created. <br> 
#### Code 

(A) <br> 
```
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
