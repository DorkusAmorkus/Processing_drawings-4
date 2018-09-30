# Processing_drawings-4


/* Your name: Elias Han

Date: 9/28/18

Project/assignment name: Java Sketch

Description: A sketch of a moving triangle that changes color when mouse is clicked

Credits for code referenced: 
https://processing.org/tutorials/color/
https://processing.org/tutorials/pshape/
https://processing.org/tutorials/interactivity/

notes:
color
triangle
PShape
mouse input

*/

PShape triangle;
  
void setup() {
  size(500, 500, P2D);
    fill(color(0,255,0));
  triangle = createShape(TRIANGLE,mouseX,mouseY, mouseX-50, mouseY+100, mouseX+50, mouseY+100);
    fill(color(0,0,0));
    stroke(color(1));
} 

void draw() {
  background(0,255,0);
  translate(mouseX,mouseY);
triangle.setStroke(color(255));
  triangle.setStrokeWeight(4);  
  shape(triangle);
  if (mousePressed == true) {
    triangle.setFill(color(255,0,0)); // White
  } else {
    triangle.setFill(color(0,0,255)); // Black
  }
  
}
