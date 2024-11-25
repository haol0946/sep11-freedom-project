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

### 11/10/24
*https://codehs.com/tutorial/ryan/introduction-to-p5play

User Input & Sprite interactions

* Keyboard Inputs
	* kb.presses(key letter or name)
		* At the time of press
	* kb.pressing(key letter or name)
		* The duration of press
* Mouse Inputs
	* sprite.mouse.presses()
		* At the time of click on sprite
	* sprite.mouse.pressing()
		* The duration of click on sprite
	* sprite.mouse.dragging()
		* If user is clicking AND dragging sprite around
* Sprite Interactions
	* sprite1.overlaps(sprite2)
		* The moment of overlap
	* sprite1.overlapping(sprite2)
		* The duration of overlap
	* sprite1.collides(sprite2)
		* The moment of collision
	* sprite1.colliding(sprite2)
		* The duration of collision

```js
   if (ball.mouse.dragging()) {
        ball.moveTowards(mouse, 0.1);
    }
    if (kb.pressing('up')) {
        brick1.width += 2;
        brick2.width += 2;
    } else if (kb.pressing('down')) {
        brick1.width -= 2;
        brick2.width -= 2;
    }
```
* If mouse is dragging ball = Ball moves towards mouse
* If kb is being pressed with up then increase brick 1 & 2 width or if pressing down then brick 1 & 2 minus width

### 11/19/24
*https://codehs.com/tutorial/ryan/introduction-to-p5play

## Groups + Tile system

Groups
* Allows you to group sprites
	* Each sprite will have same color, position, diameter, and bounciness

```js
let ballGroup = new Group();
ballGroup.diameter = 20;
ballGroup.y = -20;
ballGroup.vel.y = 2;
ballGroup.bounciness = 0.5;
ballGroup.color = 'lightblue';
```
*I.e, all of the sprites in this group will have these specfic properties

`
let ball = new ballGroup.Sprite();
`
*Allows you to create a sprite from the group


Tile system
* A grid like structure (Similar to Arrays but not exactly)
	* "." Periods or " " Empty spaces to mark blank spots
	* "var".tile = " " aka you can choose your tile symbol



`
   tiles.tile = '+';
`

* Would create a new tile group called tiles with + being used for tiles

```js
  new Tiles(
    	[
        ".....+++++.....",
        "....+++++++.....",
        ".....+++++......",
        "......+++.......",
        ".......+........",
        ".......+........",
        "....+++++++.....",
        ".......+........",
        ".......+........",
        "......+.+......",
        ".....+...+......",
    	],
    );
```
* Would create a stick figure with "+" as "tiles"

### 11/22/24
*https://codehs.com/tutorial/ryan/introduction-to-p5play

## Sprite Image & Animation

* preload()
	* Function that makes sure loadImage runs first
		* loadImage()
			* Loads image from local sever (MUST BE INSIDE preload)
* addAni()
	* What your adding ani to + name of ani + sprite sheet + Dimensions of ONE image + row + # of imgs (Frames) + Frame delay


```js
let idleSheet = loadImage('______');
    let walkingSheet = loadImage('______');
    let runningSheet = loadImage('______');

```
* Creating different images for each "Frame"


```js
  character.addAni('idle', idleSheet, {w: 128, h: 82, row: 0, frames: 6, frameDelay: 8});
    character.addAni('walking', walkingSheet, {w: 128, h: 83, row: 0, frames: 8, frameDelay: 8});
    character.addAni('running', runningSheet, {w: 128, h: 82, row: 0, frames: 8, frameDelay: 8});
```
* Examples of addAni




```js
    if (kb.pressing('arrowRight')) {
        // Sprite runs faster if user presses r key
        if (kb.pressing('r')) {
            character.ani = 'running';
            character.vel.x = 4;
        } else {
            character.ani = 'walking';
            character.vel.x = 2;
        }
```
* Example of animations working with user input
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
