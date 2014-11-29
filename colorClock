import processing.core.*; 
import processing.data.*; 
import processing.event.*; 
import processing.opengl.*; 

import java.util.HashMap; 
import java.util.ArrayList; 
import java.io.File; 
import java.io.BufferedReader; 
import java.io.PrintWriter; 
import java.io.InputStream; 
import java.io.OutputStream; 
import java.io.IOException; 

public class colorClock extends PApplet {

float clockDiameter;
int cx, cy;
PFont f, d;
int value;

public void setup(){
  size(640, 640);
  stroke(255);
  clockDiameter = 500;
  cx = width / 2;
  cy = height / 2;
  print(second(), minute(), hour());
  printArray(PFont.list());
  f = createFont("Bebas Neue", 150);
  textFont(f);
}

public void draw() {
  background(255);
  int value = color( second()*0.07f, minute()*4.24f, hour()*21.25f);
  fill(value);
  noStroke();
  ellipse(cx, cy, clockDiameter, clockDiameter);
  if (mousePressed == true) {
     fill(255);
     text(hour(), 100, 380);
     text(":", 220, 370);
     text(minute(), 240, 380);
     text(":", 365, 370);
     text(second(), 400, 380);
  }
}


  static public void main(String[] passedArgs) {
    String[] appletArgs = new String[] { "colorClock" };
    if (passedArgs != null) {
      PApplet.main(concat(appletArgs, passedArgs));
    } else {
      PApplet.main(appletArgs);
    }
  }
}
