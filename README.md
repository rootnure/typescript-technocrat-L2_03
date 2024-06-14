# Object Oriented Typescript

- oop -> class in ts
    - declare a class
    - declare property in class
    - declare property type in class
    - constructor in class
    - declare method in class
    - create instance from class
    - parameter properties
- oop -> inheritance in ts
    - Inherit property and method from another (parent) class and extends it
    - ```class Student extends Person```
        - Here Student will get all the property and method of Person class also may/will have some extra property and method of its own.
    - **Every class must have a constructor of its own.**
    - To send value to ***parent*** class from ***child*** class ```super()``` method is used
- Type Guard
    - ```typeof```
    - ```in```
- Type Guard with Instance
    - ```instanceof``` is used to check if a instance is a instance of a specific class
    - It can be handled using function to narrow down the type --> ***type narrowing***
        - This functions' return type can be a class
        - ```const isCat = (animal: Animal): animal is Cat => animal instanceof Cat;``` here the return type is boolean but updated by its class *Cat*
- Access Modifier
    - **public** [Default Access] -> Can access from anywhere (inside the class or from instance)
    - **private** -> Only accessible inside the class where it is declared/initialized
    - **protected** -> Accessible from inside the class itself or the class that extends that parent class
    - Access modifier can be used for both property and method
    - Private/Protected property name stats with ```_``` *(Underscore)* to identify as the property is private **(i.e: _balance)**
- Getter and Setter in TS
    - Access special method as like property of the instance
    - ```set``` keyword is used to declare a method that receive a parameter from the method
        - ```set depositAmount(amount: number) { // function code here }```
        - ```instanceName.depositAmount = 100;```
    - ```get``` keyword is used to declare a method that does not need any parameter to receive
        - ```get balance(amount: number) { // function code here }```
        - ```console.log(instanceName.balance);```
- Static --> OOP
    - ***static*** is a special type of access modifier that helps to specialized a property or method to access specially
    - A property as **static** need to be called inside the class by the class name instead of ```this``` keyword
        - ```static count: number = 0;```
        - ```increment() { ClassName.count = ClassName.count + 1; }```
    - A method as **static** need to be called by the method of that class name
        - ```static increment() { ClassName.count = ClassName.count + 1; }``` *[inside the class]*
        - ```console.log(ClassName.increment());``` *[outside the class]*