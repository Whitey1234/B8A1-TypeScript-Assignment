#Access Modifiers in TypeScript

##introduction

when working  with classes in typescript  it is important to contrl how to properties and method can  be acessed. there is four types of modifire, 1. public, 2. private, 3. protected 4, readonly 

##Access modifire understanding

###public: this is the default access modifire in typeScript, A public property or method can be acess form any where 
like example 

class Student {
  public name: string = "Rahim";
}

const student = new Student();
console.log(student.name);

here the name property can be accessable from outside



###Private: A private property can only be accessed inside the class where it is declared. It helps protect internal data from direct changes.

example :

class Account {
  private balance: number = 5000;
}

###Protected : A Protectd peoperty can be access only this class,  its hils class also can use it whe working with inheritence 
example :

class Employee {
  protected name: string = "Rahim";
}

class Manager extends Employee {
  showName(): string {
    return this.name;
  }
}

###Readonly : A re4adoly property can be asssigned a value during declaration or inside the  constructor, after that  , its value cannot be changed
example : 

class Student {
  readonly id: number = 101;
}

const student = new Student();
console.log(student.id);

##Conculation : acess modifiers make  typescript classes more organized and secure , and help developers  control data access and avoid unwanted changes


