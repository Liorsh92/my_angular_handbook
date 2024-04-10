
## Angular Notes
---
angular cli = ng

to create a new  angular project

ng new project-name 


## TypeScript Notes
---
### Primitives

[Handbook](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#the-primitives-string-number-and-boolean)

number, boolean, string, any 

`let isDone: boolean = false`
`let count: number = 6`
`let name: string = "leon"`
`let list: number[] = [1,2,3] || let list Array<number> = [1,2,3]` 

### Differences Between Type Aliases and Interfaces

Type aliases and interfaces are very similar, and in many cases you can choose between them freely. Almost all features of an `interface` are available in `type`, the key distinction is that a type cannot be re-opened to add new properties vs an interface which is always extendable.

```
type Point = {
	x: number,
	y: number 
}

function printCoord( pt: point ) {
	console.log(pt.x,pt.y)
}
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

