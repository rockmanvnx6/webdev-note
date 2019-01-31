# Variables

```javascript
var globalScope; // global
function something() {
    var localScope; //local
}
```

### Const and Let

**Const**

> Constant
>
> Can't be changed once defined
>
> `const MYCONSTANT = 5`



**Let**

> Block scope variable
>
> Smaller scope than var
>
> **Example:**
>
> ```javascript
> function testLocal() {
>     var myLocal = "This is a local";
>     if (myLocal) {
>         var myLocal = "another thing";
>         console.log(myLocal);
>     }
>     console.log(myLocal);
> }
> testLocal();
> ```
>
> What do you think the result is ? Based on our knowledge about local variable. the `myLocal` in the `if` statement should be another new `myLocal` which is different than the old one.
>
> However, when generate:
>
> `another thing`
>
> `another thing`
>
> which means it automatically changed the content in the original `myLocal`
>
> Now is when `let` comes in handy:
>
> ```javascript
> function testLocal() {
>     var myLocal = "This is a local";
>     if (myLocal) {
>         let myLocal = "another thing";
>         console.log(myLocal);
>     }
>     console.log(myLocal);
> }
> testLocal();
> ```
>
> Now the result will be:
>
> `another thing`
>
> `This is a local`

