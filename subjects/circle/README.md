## circle

### Instructions

Create the structures `Circle` and `Point` and the methods necessary for the code in [usage](#usage) to compile and run giving the expected result.

Methods:
  - Point;
    distance()
  - Circle:
    diameter -> returns the diameter of the circle
    area -> returns the area of the circle
    intersection -> returns true if the 2 circles intersect
Associated Functions
  - Circle:
    new -> receives three 64 bits floating point numbers in the following
    order: x, y and radius (x and y are the coordinates of the center).
    and returns a new circle
	
	
### Expected Functions and Structures

This snippets are incomplete and it's part of the exercise to discover the how to complete them

```rust
struct Circle {
	center //..
	radius //..
}

struct Point {
// ...	
}

// Point
fn distance(p1, p2) -> _ {

}

// Circle
fn new(x: f64, y: f64, radius: f64) -> Circle {
}

fn diameter(_) -> _ {
}

fn area() -> _ {
}
```

### Usage

Here is a program to test your function

```rust
use std::f64::consts;
use circle::{Circle, Point};

fn main() {
	let circle = Circle::new(500.0, 500.0, 150.0);
	let circle1 = Circle {
		center: Point { x: 80.0, y: 115.0 },
		radius: 30.0,
	};
	let point_a = Point { x: 1.0, y: 1.0 };
	let point_b = Point { x: 0.0, y: 0.0 };
	println!("circle = {:?} area = {}", circle, circle.area());
	println!("circle = {:?} diameter = {}", circle, circle.diameter());
	println!("circle1 = {:?} diameter = {}", circle1, circle1.diameter());
	println!(
		"circle and circle1 intersect = {}",
		circle.intersect(&circle1)
	);

	println!(
		"distance between {:?} and {:?} is {}",
		point_a,
		point_b,
		point_a.distance(&point_b)
	);

}
```

And its output

```console
student@ubuntu:~/[[ROOT]]/test$ cargo run
circle = Circle { center: Point { x: 500.0, y: 500.0 }, radius: 150.0 } area = 70685.83470577035
circle = Circle { center: Point { x: 500.0, y: 500.0 }, radius: 150.0 } diameter = 300
circle1 = Circle { center: Point { x: 80.0, y: 115.0 }, radius: 30.0 } diameter = 60
circle and circle1 intersect = false
distance between Point { x: 1.0, y: 1.0 } and Point { x: 0.0, y: 0.0 } is 1.4142135623730951
student@ubuntu:~/[[ROOT]]/test$
```
