
<a href="http://public.district196.org/rhs/"><img src="http://public.district196.org/rhs/imagesmain/crest150_trans.png" title="Rosemount High School" alt="RHS"></a>





# Senior-Year-Protfolio

> This portfolio will showcase the projects that I have been working on in my senior year of High School.


# Java Portfolio


<details>
<summary>WebPage</summary> 
<br>(https://kantab.github.io/testWeb/)
This project was desgined to give an introduction to HTML and JS. This was the first web page I made. 
The hardest part was understanding a new launage.
 </br>
</details>
<details>
<summary>Lightning</summary>
 
  ```Java
  int startx=150;
  int starty=200;
  int endx=50;
  int endy=150;
  int cl1=232;
  int cl2=171;
  int cl3=18;
void setup()
{
    size(400,280);
    strokeWeight(5);
    background(255);
  
  
}
void draw()
{
  background(255);
  fill(96, 72, 12);
  stroke(0);
  rect(75, 200, 75, 5);
  rect(285, 170, 16, 20);
  fill(cl1, cl2, cl3);
  stroke(0);
  ellipse(295, 224, 90, 75);
  ellipse(295, 224, 75, 75);
  ellipse(295, 224, 35, 75);
  fill(0);
  stroke(0);
  triangle(70, 148, 60, 260, 111, 260);
  fill(8, 84, 34);
  stroke(0);
  ellipse(75, 144, 72, 72);
  fill(0);
  triangle(70, 38, 50, 120, 101, 120);
  
  
  fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
  stroke((int)(Math.random()*256),(int)(Math.random()*256),(int)(Math.random()*256));
  
  while(endx<300){
    endx=startx+(int)(Math.random()*5);
    endy=starty+(int)(Math.random()*2);
    
    line(startx,starty,endx,endy);
    startx=endx;
    starty=endy;
  }
 // for(int i=0; i<=300; i++){
  //startx=0;
  //starty=150;
  //endx=50;
  //endy=150;
  //}
  
}
void mousePressed()
{
  
  startx=150;
  starty=200;
  endx=0;
  endy=50;
  cl1=(int)(Math.random()*256);
  cl2=(int)(Math.random()*256);
  cl3=(int)(Math.random()*256);
  

}
```

<br>
This project was desgined to practice using Math.random. The hardest part for the project was figuring out the layout of where the lighting starts and ends.
 </br>
</details>
<details>
<summary>Dice</summary>
 
 ```Java
Die die1;
Die die2;
Die die3;
int cou1=0;
int cou2=0;
int cou3=0;
int numClick=0;
int money=5000;
int w =60;
int bwx=0;
int bwy=0;

void setup()
{
  
  size(600,600);
  
  noLoop();
}
void draw()
{
  background(600,600);
  fill(255,100,0);
  rect(50,50,500,500);
  fill(255,100,200);
  rect(60,60,480,100);
  fill(255,100,255);
  rect(80,200,50,300);
  fill(255,100,100);
  rect(150,350,100,100);
  rect(260,350,100,100);
  rect(370,350,100,100);
  textSize(75);
  fill(0,255,255);
  text("Big 9 $lot$",100,125);
  textSize(30);
  text("Total:",160,335);
  textSize(20);
  
  text("Num Click:",260,335);
  
  textSize(25);
  text("Money $:",380,335);
  text("$ "+money,370,410);
  die1 = new Die(200,200);
     die1.roll();
     die1.show();
     if(die1.getNum()==1){
       cou1++;
     }
     if(die1.getNum()==2){
       cou1+=2;
     }
     if(die1.getNum()==3){
       cou1+=3;
     }
     if(die1.getNum()==4){
       cou1+=4;
     }
     if(die1.getNum()==5){
       cou1+=5;
     }
     if(die1.getNum()==6){
       cou1+=6;
     }
  die2 = new Die(300,200);
     die2.roll();
     die2.show();
     if(die2.getNum()==1){
       cou2++;
     }
     if(die2.getNum()==2){
       cou2+=2;
     }
     if(die2.getNum()==3){
       cou2+=3;
     }
     if(die2.getNum()==4){
       cou2+=4;
     }
     if(die2.getNum()==5){
       cou2+=5;
     }
     if(die2.getNum()==6){
       cou2+=6;
     }
  die3 = new Die(400,200);
     die3.roll();
     die3.show();
     if(die3.getNum()==1){
       cou3++;
     }
     if(die3.getNum()==2){
       cou3+=2;
     }
     if(die3.getNum()==3){
       cou3+=3;
     }
     if(die3.getNum()==4){
       cou3+=4;
     }
     if(die3.getNum()==5){
       cou3+=5;
     }
     if(die3.getNum()==6){
       cou3+=6;
     }
     if(cou1+cou2+cou3==9){
       
       textSize(50);
       fill(0,255,0);
       text("WINNER!",280,500);
       money+=500;
       
     }
     if(cou1+cou2+cou3!=9){
       
      
       textSize(50);
       fill(255,0,0);
       text("LOSER!",280,500);
       money-=100;
       
     }
     if(cou1!=3&&cou1==cou2 && cou2 == cou3){
       textSize(75);
       fill(0,255,0);
       bwx=100;
       bwy=100;
       money+=1000;
       text("Big WINNER!!",bwx,bwy);
     }
     if(cou1==3&&cou2==3&&cou3==3){
       textSize(75);
       fill(0,255,0);
       bwx=100;
       bwy=100;
       money+=10000;
       text("Megga WINNER!!!",bwx,bwy);
     }
  textSize(65);
  text(cou1+cou2+cou3,160,425);
  
  if(numClick >= 100){
    w=45;
  }
  textSize(w);
  text(numClick,270,425);
  
  //for(int i=0; i<1200; i+=60){
   // for(int j=0; j<600; j+=60){
    //  die = new Die(i,j);
     // die.roll();
     // die.show();
   // }
 // }
    //your code here
  }
  //your code here

void mousePressed()
{
  cou1=0;
  cou2=0;
  cou3=0;
  bwy=0;
  bwx=0;
  numClick++;
  redraw();
}
////////////////////////////////////////////////
 
 class Die //models one single dice cube
{
  int x;
  int y;
  int num;
  //variable declarations here
  Die(int x, int y) //constructor
  {
    this.x=x;
    this.y=y;
    
    //variable initializations here
  }
  void roll()
  {
    num= (int)((Math.random()*6)+1);
    //num=6;
    //your code here
  }
  void show()
  {
    rect(x,y,50,50);
    if(num==1){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
      ellipse(x+25,y+25,10,10);
      
     }
     if(num==2){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
      ellipse(x+10,y+10,10,10);
      ellipse(x+40,y+40,10,10);
      
     }
    if(num==3){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
      ellipse(x+10,y+10,10,10);
      ellipse(x+25,y+25,10,10);
      ellipse(x+40,y+40,10,10);
      
      
     }
    if(num==4){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
     ellipse(x+10,y+10,10,10);
     ellipse(x+40,y+40,10,10);
     ellipse(x+10,y+40,10,10);
     ellipse(x+40,y+10,10,10);
      
     }
    if(num==5){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
     ellipse(x+10,y+10,10,10);
     ellipse(x+25,y+25,10,10);
     ellipse(x+40,y+40,10,10);
     ellipse(x+10,y+40,10,10);
     ellipse(x+40,y+10,10,10);
      
     }
    if(num==6){
      fill((int)(Math.random()*256)+10,(int)(Math.random()*256)+10,(int)(Math.random()*256)+10);
     ellipse(x+10,y+10,10,10);
     ellipse(x+40,y+40,10,10);
     ellipse(x+10,y+40,10,10);
     ellipse(x+40,y+10,10,10);
     ellipse(x+10,y+25,10,10);
     ellipse(x+40,y+25,10,10);
      
     }
    
    //your code here
  
}
int getNum(){
   return num;
}
}

 ```
<br>(https://kantab.github.io/dice3/)
The project goal was to display dice on the screen and out put their sum. This was my favorite project beacuse I was able to put my own creative spin on it. I displayed the dice as a game where you would win if your sum of 3 dice was 3, or if all 3 numbers were the same.
 </br>
</details>
<details>
<summary>Chemotaxis JS</summary>
<br>( https://kantab.github.io/chemotaxis4/)
The project was desgined to learn a bit more with arrylist. The hardest part of this project was once I was complete I converted the code into JavaScript. This was the first time I had worked with JavaScript. 
 </br>
</details>
<details>
<summary>Starfeilds</summary>

 ```Java
 Particle [] p = new Particle[100];
Particle [] p2 = new Particle[100];
Particle [] p3 = new Particle[100];
void setup(){
size(800,600);
for(int i =0; i<p.length; i++){
 p[i]= new NormalParticle();
 p2[i]= new oddBallParticle();
 p3[i]= new jumpoParticle();
}
for(int j =0; j<p2.length; j++){
//p2[j]= new oddBallParticle();
}
  
}
void draw(){
  
  
  noStroke();
  fill( 2, 0, 0, 5);
  rect(0, 0, width, height,50);
  for(int i=0; i<p.length; i++){
    p[i].move();
    p[i].show();
    p2[i].move();
    p2[i].show();
    p3[i].move();
    p3[i].show();
  }
}

interface Particle{
  void show();
  void move();
  
}
////////////////////////////////////////////////////////
class NormalParticle implements Particle {
  double x, y, speed, angle;

  public NormalParticle() {
    x=width/2-100;
    y=height/2-100;
    speed=5;
    angle=0.25;
  }
  void move() {
    /* if(angle>0.025){
     angle-=0.05;
     }
     else {
     angle+=0.05;
     }
     */
    if (angle>0) {
      angle+=0.05;
    }
    x+=Math.cos(angle)*speed;
    y+=Math.sin(angle)*speed;
    angle+=0.025;
  }
  void show() {
    fill(0, 255, 200);
    //fill((int)((Math.random()*200)+150), (int)((Math.random()*200)+150), (int)((Math.random()*200)+150));
    ellipse((int)x, (int)y, 20, 20);
  }
}
//////////////////////////////////////////////////////////
class jumpoParticle implements Particle {
  double x, y, speed, angle;

  public jumpoParticle() {
    x=width/2+100;
    y=height/2-100;
    speed=5;
    angle=0.25;
  }
  void move() {
    x+=Math.cos(angle)*speed;
    y+=Math.sin(angle)*speed;
    angle+=0.025;
    
  }
  void show() {
    fill((int)((Math.random()*200)+150), (int)((Math.random()*200)+150), (int)((Math.random()*200)+150));
    ellipse((int)x, (int)y, 80, 30);
    
    ellipse((int)x, (int)y-10, 40, 40);
  }
}
/////////////////////////////////////////////
class oddBallParticle implements Particle {
  double x, y, speed, angle;

  public oddBallParticle() {
    x=width/2;
    y=height/2;
    speed=Math.random()*5;
    angle=Math.random()*Math.PI*8;
  }
  void move() {
    x+=Math.cos(angle)*speed;
    y+=Math.sin(angle)*speed;
    angle+=0.025;
    if (x>500) {
      x=100;
      speed*=-1;
    }
    if (y>500) {
      y=300;
      
      speed*=-1;
    }
  }
  void show() {
    fill((int)((Math.random()*200)+150), (int)((Math.random()*200)+150), (int)((Math.random()*200)+150));
    ellipse((int)x, (int)y, 20, 20);
  }
}
//////////////////////////////////////////////////
 
 ```
 <br>
This project was by far the hardest for me to understand. I had a hard time understaning how the objects were to be displayed on the screen and the angle in which they moved. I had to partner up with other class mates so they could show me how it worked.
 </br>
</details>

***

 This is my most worthy peice of code so far. This code is from my JS chemotaxis. I like this code because it was not only a little tricky to figure out how to cycle through the images but I then had to take this code and change it from Java to JavaScript, a launage I was learning at the time. What was tricky about cycling through was the fact when I had a mousePressed method, when I would increase the counter that would in turn change the pictures it would add more then once when the mouse was clicked/ pressed. How i solved this is i created a boolean that would flip if the mouse was pressed and when it wasnt it would be fliped back. This then made it able to only increase by one when the mouse was pressed. 
```Java
 if (!mousePressed) {
    this.ss = true;
  }
  if(mousePressed){
    this.ss=false;
  }
  
    
    if(this.clic==0){
    image(this.img1, this.x, this.y);
    }
    if(this.clic==1){
    image(this.img2, this.x, this.y);
    
    }
    if(this.clic==2){
    image(this.img4, this.x, this.y);
    
    }
    if(this.clic>2){
    this.clic=0;
    
    }
    

```
# C++ Portfolio

<details>
<summary>Payroll</summary> 
<br>(https://kantab.github.io/testWeb/)
This project was one that I worked on in my introduction to C++ class I took at Inver Hills Community College. This project was desgined to teach us how to use things such as setprecision, switchs, try/ catch statements, interfaces, user inputs, and a lot of the key foundations to help learn and understand C++. We made a few difernt variations of this project and this is the final one.
 </br>
</details>


