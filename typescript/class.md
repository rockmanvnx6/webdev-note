# Classes

```typescript
class Student {
    fullName: string;
    constructor(public firstName: string, public middleName: string, public lastName: string) {
        this.fullName = firstName + " " + middleName + " " + lastname;
    }
}
```

`public` is a shorthand to automatically create properties with that field.

> **To communicate with interface**, `public` must be used so the interface can see.



**Example communicate with interface**

```typescript
class Student {
    fullName: string;
    constructor(public firstName: string, public middleName: string, public lastName: string, public age: number) {
        this.fullName = firstName + " " + middleName + " " + lastname;
    }
}

interface Person {
    firstName: string;
    lastName: string;
    age: number;
}

let user = new Person("Thang", "N", "Pham", 10);

function greetings(person: Person) {
    return "Hello, " + person.firstName + " " + person.lastName;
}

document.body.innerHTML = greetings(user);
```



