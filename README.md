# week3homework
color yellow = color(251, 227, 7);
color red = color(225, 10, 5);
color blue = color(76, 115, 194);
color black = color(21, 12, 15);
color white = color(255);
int lw=20;
int A=220;
int B=370;
int C=640;
int D=960;
int x;
int y;
float c;
float s;
int r;
float chang;
float gao;
int num=1;
float pos1;
float pos2;

void setup() {
  size (1000, 1000);
  background(white);
  stroke(yellow);
  strokeWeight(lw);
}
void keyPressed( ) {
}

void draw() {
  chang=random(0, 400);
  gao=random(0, 400);
  stroke(yellow);
  strokeWeight(lw);
  line(100, 0, 100, 1000);
  line(C, 0, C, 1000);
  line(D, 0, D, 1000);
  line(800, B, 800, C);
  line(B, C, B, 1000);
  line(0, 100, D, 100);
  line(C, 0, C, 1000);
  line(C, B, D, B);
  line(0, C, 1000, C);
  line(C, 900, D, 900);
  stroke(yellow);
  strokeWeight(lw);
}
void functionA() {
  println("excute me once!");
}

void mousePressed() {
  r=r+1;
  if (r>=3) {
    r=0;
  }
  if (r==1) {
    moveR();
  } else if (r ==2) {
    moveY();
  } else {
    moveB();
  }
}



//draw rect

void moveR() {
  if (key=='1') {
    noStroke();
  } else if (key=='2') {
    strokeWeight(lw);
  }
  x=mouseX;
  y=mouseY;
  c=random(30, 200);
  s=random(30, 200);
  fill(red);
  rect(x, y, c, s);
  line(0, y, 1000, y);
  line(x, 0, x, 1000);
  noStroke();
  for (pos1=chang; pos1<=random(800, 980); pos1+=random(10, 300)) {
    rect(pos1, y-10, 20, 20);
  }
  for (pos2=gao; pos2<=random(800, 980); pos2+=random(10, 500)) {
    rect(x-10, pos2, 20, 20);
  }
}
void moveY() {
  if (key=='1') {
    noStroke();
  } else if (key=='2') {
    strokeWeight(lw);
  }
  x=mouseX;
  y=mouseY;
  c=random(30, 200);
  s=random(30, 200);
  fill(255, 255, 0);
  rect(x, y, c, s);
  line(0, y, 1000, y);
  line(x, 0, x, 1000);
  noStroke();
  rect(chang, y-10, 20, 20);
  rect(x-10, gao, 20, 20);
}
void moveB() {
  if (key=='1') {
    noStroke();
  } else if (key=='2') {
    strokeWeight(lw);
  }
  x=mouseX;
  y=mouseY;
  c=random(30, 200);
  s=random(30, 200);
  fill(0, 0, 255);
  rect(x, y, c, s);
  line(0, y, 1000, y);
  line(x, 0, x, 1000);
  noStroke();
  rect(chang, y-10, 20, 20);
  rect(x-10, gao, 20, 20);
}
