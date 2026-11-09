# Generics and Promises In TypeScript

##Introduction 

TypeScript provides sevarel features that make javaScript development  more reliable. Generics and promises are two usefull feature  that developer often use in real project  , Genrics help us write reusable code ,  while Promises help us handle operation that take  time, such as fatching data from an api 

## Generics in Typescript

Generics allow a function , class or interface to work with differnt data  types  without losing type sefty 

For example :



```ts function getValue<T>(value: T): T {
  return value;
}
const numberValue = getValue<number>(100);
const textValue = getValue<string>("Hello");
```

here the example  T repesents the  type passed to the function

  
##  Pomises in  TypeScript

 A promise return the result  of an asynchromous operatiom .it can be three states : pending , fulfiled rejected . we  commmonly use  promises when  working with apirequests or other operation  that do not finish immediatly 

in TypeScript, Promise<T> defines the type of value that a Promise will return when the operation is successful. For example, Promise<string> means the Promise will return a string value

example like :

```ts function getUser(): Promise<string> {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("User data loaded");
    }, 1000);
  });
}

async function showUser(): Promise<void> {
  const result = await getUser();
  console.log(result);
}

showUser();
```

### conculation :

Generics and promises slove differnt problems . but both are  important in TypeScript . Generice help us  create reusabel and type safe code , while promise make asychronous
