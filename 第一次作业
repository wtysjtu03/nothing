Eye s1, s2;

void setup() {
  size(340, 360);
  noStroke();
  s1 = new Eye( 250,  16, 120);
  s2 = new Eye( 164, 185,  80);  

}

void draw() {
  background(102);
  
  s1.update(mouseX, mouseY);
  s2.update(mouseX, mouseY);

  s1.display();
  s2.display();
}

class Eye {
  int x, y;
  int size;
  float angle = 0.0;
  
  Eye(int tx, int ty, int ts) {
    x = tx;
    y = ty;
    size = ts;
 }

  void update(int mx, int my) {
    angle = atan2(my-y, mx-x);
  }
  
  void display() {
    pushMatrix();
    translate(x, y);
    fill(255);
    ellipse(0, 0, size, size);
    rotate(angle);
    fill(0, 0, 0);
    ellipse(size, 0, size, size);
    popMatrix();
  }
}
