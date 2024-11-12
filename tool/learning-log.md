# Tool Learning Log

## Tool: **P5 Play**

## Project: **Photography Game**

---

### 10/19/24:
* https://p5play.org/learn/sprite.html?page=1
## Basics
* sprite = Ghost/Character that moves infront of a background
* sprite.x/y= 175; = Where sprite will be
* sprite.w/h = 200; = Width & Height respectively
* sprite.color = 'pink'; = Color filled in = pink
* sprite.stroke = 'red'; = Color outline = red
* sprite.d = 40; = Diameter
* sprite.textSize = 40; = Text size
* sprite.text = "p5"; = What text
## Physics
* Dynamic Physics!!! = Able to freely move AND be affected by gravity
* ```js
function setup() {
	new Canvas(300, 350);

}
ball = new Sprite();
	ball.diameter = 10;
	ball.y = 170;
  ball.x = 150
	ball.collider = 'static';
ball = new Sprite();

	ball.y = 100;
  ball.x = 150
  world.gravity.y = 10;
function draw() {
	clear();
}
```
^ Created circle and square sprite with circle being static & not moving with square falling ontop of it
* Going to finish looking at p5play website and look at https://codehs.com/tutorial/ryan/introduction-to-p5play to see overlaping details or details missed



### 11/4/24
*https://codehs.com/tutorial/ryan/introduction-to-p5play
## Physics

* Collider types
	* Dynamic
		* Can collide
		* Moves with
			* Code, Collisions, Gravity
	* Kinematic
		* Can collide
		*Moves with Code
	* Static
		* Can collide
	* None
		* Moves with Code

```js
    world.gravity.y = 10;


    ground.y = 200;
    ground.friction = 0.01;
    ground.collider = 'static';
```
Ground sprite would stay still dude to its 'static' nature even though there is a gravity of 10



<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
