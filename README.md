# Const and "&" usage
# Const keyword in C++
- It stands for *constant*
- Generally in c++ its used to make the values of variables unchangeable through the entire program.
- There are many ways of using this keyword:

1. Constant Variables:
- Once the variable declared as const it must be initialized at the same time.
- The variable can't be assigned by other value anywhere in the program.
- ```
  const int x=7;
  ```
 
2. Using *const* with pointers *3 ways*:
   - It must be initialized once declared as *const*.
   1. Constant Pointer Variable to Value:
    ``` 
     char z= 'v';
     char* const i = &z;
     ```
      - The value of th variable 'z' is changeable but the location that the pointer pointed to is unchangeable.
           
    2. Pointer Variable to Constant Value:
    ```
        int y= 6;
        const int* p = &y;
    ```  
      - We can access and change the value of 'y' but we can't change the value of the pointer p. 

    3. Const Pointer to a Const Variable:
    ```
        int a= 9
        const int* const j = &a;
     ```  
      - Its not allowed to change the value of variable 'a' or the location.
    
3. Function Arguments: 
- We can't pass const argumant value to non-const parameter of a function.
    1. We can declare the parameter of a function by const:
```  
   functype funcName(const datatype var)
   ```
- And the values of 'var' can't be changed.

    2. We can declare the return type of a function by const:  
    ```
    const returntype funcName(datatype var)
    ```
   - There is no problem on passing const or non- const variable to the function, the returned value is const.
    3. For both const parameter and return type together
   ```
      const returntype funcName(const datatype var)
   ``` 
    - We can pass const or non-const to the function but we can't change the value in 'var' afterwards.

4. Constant Objects of a Class:
- Once the object is declared as *const* it needs to be initialized with ONLY constructors at the same time and can't be modified, can only call on const member function.
```
  const ClassName Objectname;
 ```
  
5. Constant function of a Class: 
- Const function can be called on const or non-const objects.
- There are *2 ways* for declaring;
  1. ordinary declaration:
   ```
    const void funcName(){}
  ```
  2. const member function of the class:
   ```
     class{
       void funcName() const{

       }
     }
     ```
      
     


# & symbol in C++  
- It's used as an *Operator*
- Used in only 3 different places:
1. Bitwise AND (Binary operator):
- It work as AND gate comparing each bit of the operands, if both bits is 1 the bit is set to 1 otherwise it's set to 0.
```
int a= 5, b=9; // 5= 0101 , 9=1001
cout<<(a&b);  // the result is 0001 so output is 1.
```
2. Logical AND :
- It's used to check conditions (boolean), if all conditions are ture the result is true otherwise is false.
```
int a=5;
int b=10;
int c=8;
if(b%2==0 && a>c){ //the result is false because a is not bigger than c.
  cout<< "true";
}
``` 
3. Pointer Address Operator:
- Its used to get the address of a variable, then we can store it in pointer or print it.
- ```
  int A= 8;
  int* ptr=&A; // where * is indirection operator.
  cout<<&A;
  ```
  
