# interface

```typescript
interface Person {
    firstName: string;
    lastName: string;
    age: number;
}
```

to use interface

```bash
function greeter(person: Person) {
    return "Hello, " + person.firstName + " " + person.lastName;
}
```

