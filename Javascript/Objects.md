# Objects

### Long hand:

```javascript
var weapons = new Object();
weapons.name = "Y thien kiem";
weapons.damage = 72;
weapons.durability = 100;
```

if you call `weapons` in console:

```console
{name: "Y thien kiem", damage: 72, durability: 100}
damage: 72
durability: 100
name: "Y thien kiem"
__proto__: Object
```

#### Short hand:

```javascript
var weapons = {
    name: "Y thien kiem",
    damage: 72,
    durability: 100,
}
```

remember to use `,` instead of `;`

> You can access to any instance by: `object.variable`. For example: `weapons.name`



## Function in object

We can create a local function inside an object:

```javascript
var weapons = {
    name: "Y thien kiem",
    damage: 72,
    durability: 100,
    skill: function () {
    	return weapons.damage+=100;
	},
}

console.log(weapons.damage);
weapons.skill();
console.log(weapons.damage);
```

```console
72
172
172
```

## Create multiple object

So what if you want to create multiple object ?

Use `function` with **capital first letter - actually you can without it.** and use `this` to refer to it owns object.

```javascript
function AddWeapons(name, damage, durability) {
    this.name = name;
    this.damage = damage;
    this.durability = durability;
    this.skill = function() {
    	return this.damage += 100;
    };
}

// We now can create new objects by:

var weapon1 = new AddWeapons("y thien kiem", 72, 100);
var weapon2 = new AddWeapons("dau long dao", 82, 50);


console.log(weapon1);
weapon1.skill();
console.log(weapon2);
```

```console
AddWeapons {name: "y thien kiem", damage: 72, durability: 100, skill: ƒ}
172
AddWeapons {name: "dau long dao", damage: 82, durability: 50, skill: ƒ}
```

#### Array way:

You can put all of the objects into 1 array.

```javascript
var weapons = [
    new AddWeapons("y thien kiem", 72, 100),
    new AddWeapons("dau long dao", 82, 50),
];
console.log(weapons)
```

```javascript
0 AddWeapons {name: "y thien kiem", damage: 72, durability: 100, skill: ƒ}
1 AddWeapons {name: "dau long dao", damage: 82, durability: 50, skill: ƒ}
length: 2
```

now you can just

`weapons[0], weapons[1]`



## Notation

Two type of notation:

| Dot notation | Bracket notation |
| ------------ | ---------------- |
| weapon1.name | weapon1["name"]  |

**So when do we use Bracket ?**

When there is an odd properties name: for example `WP:image`.

if you use `weapon1.WP:image` there will be error.

So you have to use `weapon1["WP:image"]`

