
## Angular Notes
---
angular cli = ng

to create a new  angular project

ng new project-name 


## TypeScript Notes
---
### Primitives

[Handbook](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#the-primitives-string-number-and-boolean)

[tsconfig-json](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)

number, boolean, string, any 

`let isDone: boolean = false`<br>
`let count: number = 6`<br>
`let name: string = "leon"`<br>
`let list: number[] = [1,2,3] || let list Array<number> = [1,2,3]` 

### Differences Between Type Aliases and Interfaces

Type aliases and interfaces are very similar, and in many cases you can choose between them freely. Almost all features of an `interface` are available in `type`, the key distinction is that a type cannot be re-opened to add new properties vs an interface which is always extendable.

```
type Point = {
	x: number,
	y: number 
}

function printCoord( pt: Point ) {
	console.log(pt.x,pt.y)
}

printCoord({x: 1, y:2})
```

```
interface Point = {
	x: number,
	y: number
}
```

### Type Assertions

```
const myCanvas = document.getElementById("main_canvas") as HTMLCanvasElement;

const myCanvas = <HTMLCanvasElement>document.getElementById("main_canvas");
```

### Enums

Enums are one of the few features TypeScript has which is not a type-level extension of JavaScript.<br><br>

Enums allow a developer to define a set of named constants. Using enums can make it easier to document intent, or create a set of distinct cases. TypeScript provides both numeric and string-based enums.

```
enum Direction {
  Up = 1,
  Down,
  Left,
  Right,
}
```
Above, we have a numeric enum where Up is initialized with 1. All of the following members are auto-incremented from that point on. In other words, Direction.Up has the value 1, Down has 2, Left has 3, and Right has 4.




