
<a href="https://www.uwstout.edu/"><img src="https://dcstatic.library.wisc.edu/Collections/images/UWStout_logoNew.png" title="UW-Stout" alt="UW-Stout"></a>





# Brendan-Kanta-Protfolio

> This portfolio will showcase the projects that I have worked on. You can reach me by Email (brendan.k29@gmail.com) or on LinkedIn (www.linkedin.com/in/brendan-kanta)

# Resume

<details>
<summary>My Resume</summary> 
<br>
<p><a href="https://github.com/kantab/Brendan-Kanta-Protfolio/blob/master/Brendan%20Kanta%20Resume%20MR%20.pdf">My Resume</a>.</p>
This is a copy of my resume if you wish to download it.
 </br>
</details>

# Java 


<details>
<summary>WebPage</summary> 
<br>(https://kantab.github.io/testWeb/)
This project was designed to give an introduction to HTML and JS. This was the first web page I made. 
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
This project was designed to practice using Math.random. The hardest part for the project was figuring out the layout of where the lighting starts and ends.
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
<br>
The project goal was to display dice on the screen and out put their sum. This was my favorite project because I was able to put my own creative spin on it. I display the dice as a game where you would win if your sum of 3 dice was 3, or if all 3 numbers were the same.
 </br>
</details>
<details>
<summary>Chemotaxis JS</summary>
 
 ```Java
 'use strict';

var d = new Array();
var img1;
var img2;
var img3;
var img4;
var x;
var y;
var speedx = 2;
var speedy = 2;
var ex = 800 / 2;
var ey = 600 / 2;
var sizex = 20;
var sizey = 20;
var clic = 0;
var bounce = 0;


function preload() {
    img3 = loadImage("data/candy.png");
    img4 = loadImage("data/ghost.png");
    img1  = loadImage("data/pump.png.png");
    img2  = loadImage("data/witch.png");

    
}

function setup() {
    createCanvas(800, 600);
    for (var i = 0; i < 4; i++) {
        d[i] = new Dot(width / 2, height / 2);
    }
}

function draw() {
    background(0, 25, 45);
    fill(255, 200, 0);
    textSize(75);
    text("Happy Holloween", 100, 100);
    for (var i = 0; i < d.length; i++) {
        
        
    //works
        d[i].mouseShow();
        d[i].show();
        d[i].move();
        
        
       // d[i].gameOver();
        //d[i].autoMove();
       // d[i].autoMouse();
    }
    //move and show the bacteria   
}



class Dot {

    constructor(x, y) {
        this.x = x;
        this.y = y;
        var ss = true;
        this.clic = 0;
        this.bounce = 0;

    }
    move() {

        this.x += (Math.random() * 5) - 2;
        this.y += (Math.random() * 5) - 2;
        // Start movement
        if (mouseIsPressed != true && this.ss == true) {

            if (mouseX > this.x) {
                this.x += (Math.random() * 7);
            } else if (mouseX < this.x) {
                this.x -= (Math.random() * 7);
            }
            if (mouseY > this.y) {
                this.y += (Math.random() * 7);
            } else if (mouseY < this.y) {
                this.y -= (Math.random() * 7);
            }
        }


        if (mouseIsPressed == true && this.ss == true) {


            if (mouseX > this.x + 100 && mouseX < this.x + 100 && mouseY > this.y + 100 && mouseY < this.y + 100) {

                if (mouseX > this.x) {
                    this.x -= (Math.random() * 7);
                } else if (mouseX < this.x) {
                    this.x += (Math.random() * 7);
                }
                if (mouseY > this.y) {
                    this.y -= (Math.random() * 7);
                } else if (mouseY < this.y) {
                    this.y += (Math.random() * 7);
                }
            }
        }
        // End of mousePressed
    }

    show() {
        fill(255);
        

        if (this.bounce > 4) {
            this.clic++;
            this.bounce = 0;

        }

        if (mouseIsPressed && this.ss) {
            // if mouse is over button 

            this.clic++;

        }
        // enable button when mouse is not pressed
        if (!mouseIsPressed) {
            this.ss = true;
        }
        if (mouseIsPressed) {
            this.ss = false;
        }


        if (this.clic == 0) {
            image(img1, this.x, this.y);
        }
        if (this.clic == 1) {
            image(img2, this.x, this.y);

        }
        if (this.clic == 2) {
            image(img4, this.x, this.y);

        }
        if (this.clic > 2) {
            this.clic = 0;

        }
    }
    mouseShow() {
        image(img3, mouseX, mouseY);
        //ellipse(mouseX, mouseY, 20, 20);
    }}
   
    
    
    
    
    
    
    
    
    
    
    
    /*gameOver() {
        if (this.x == this.ex && this.y == this.ey) {
            this.x = 0;
            this.y = 0;
        }
    }
    autoMouse() {

        if (keyIsPressed == true) {
            console.log("hello");
            if (keyCode == 'a') {

                this.speedx++;
                this.speedy++;
            }
        }

        this.ex += this.speedx;
        this.ey += this.speedy;

        if (this.speedx * 2 + this.ex >= width - 90) {
            this.bounce++;
            this.speedx *= -1;
        }
        if (this.speedy * 2 + this.ey >= height - 90) {
            this.bounce++;
            this.speedy *= -1;
        }
        if (this.speedx * 2 + this.ex <= 0) {
            this.bounce++;
            this.speedx *= -1;
        }
        if (this.speedy * 2 + this.ey <= 0) {
            this.bounce++;
            this.speedy *= -1;
        }
        image(img3, ex + this.speedx, this.ey + this.speedy);
        //rect(ex+speedx, ey+speedy, sizex, sizey);
    }
    autoMove() {
        this.x += (Math.random() * 5) - 2;
        this.y += (Math.random() * 5) - 2;

        if (this.ex > this.x) {
            this.x += (Math.random() * 3);
        } else if (this.ex < this.x) {
            this.x -= (Math.random() * 3);
        }
        if (this.ey > this.y) {
            this.y += (Math.random() * 3);
        } else if (this.ey < this.y) {
            this.y -= (Math.random() * 3);
        }
    }
}
*/
     
 ```
<br>
The project was designed to learn a bit more with arraylist. The hardest part of this project was once I was complete I converted the code into JavaScript. This was the first time I had worked with JavaScript.
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
This project was one of the hardest for me to understand. I had a hard time understanding how the objects were to be displayed on the screen and the angle in which they moved. I had to partner up with other class mates so they could show me how it worked.
 </br>
</details>

<details>
<summary>Maps/Data Project</summary>
 
 ```Java
 import java.io.File;
import java.io.IOException;
import java.util.Map;
import java.util.TreeMap;
import java.util.Scanner;
import java.util.Set;
import java.util.Iterator;
import java.util.LinkedHashSet;
import java.util.ArrayList;
import java.util.*;
import static java.lang.System.*;
ArrayList<Visual> vis = new ArrayList(); // List of all of the different circles
boolean start = true; // On-off switch for the scrolling
int time = 1; // Keeps track of frames gone by since run started

void setup() {
  size(1200, 900);
  DataHandling run = new DataHandling();
  ArrayList<String> keys = new ArrayList<String>(); // Keeps track of all keys that are put into the map
  //vis.add(new Visual("X", "x", "x", "s"));
  String [] str=loadStrings("C:/Users/Brendan/Desktop/majors.txt"); // NOT SURE WHAT THIS DID
  String allText=join(str, ","); //NOT SURE WHAT THIS DID
  try {
    Scanner scan = new Scanner(new File("C:/Users/Brendan/Desktop/majors.txt"));
    scan.useDelimiter("/,");
    while (scan.hasNext()) {
      run.putData(scan.nextLine(), keys);
    }
  } 
  catch (Exception e) {
    out.println(e);
    e.printStackTrace();
  } 
  finally {
    //run.printMap();
    //out.println(keys);
  }
  int spaceOut = 0; //How far out new circles must bve put
  for (String s : keys) {
    vis.add(new Visual(s, run.getFirst(s), run.getSecond(s), run.getThird(s), 255, spaceOut + 20 + (parseInt(run.getFirst(s))/500), 400));
    spaceOut += 20 + (parseInt(run.getFirst(s))/500);
    out.println(s + " equals " + run.getFirst(s) + " " + run.getSecond(s) + " " + run.getThird(s));
  }
  /*for (String key : run.dataList.keySet()){
   vis.add(new Visual(key, run.getFirst(key), run.getSecond(key), run.getThird(key)));
   out.println(key + " equals " + run.getFirst(key) + " " + run.getSecond(key) + " " + run.getThird(key));
   }*/
}

void draw() {
  background(0);
  //time++;
  if (start == true) {
    for (int i = 0; i < vis.size(); i++) {
      vis.get(i).display(0);
    }
    out.print(vis.size());
    out.println(vis.get(1).xpos + " " + vis.get(1).ypos);
    out.println(vis.get(2).xpos + " " + vis.get(2).ypos);
    start = false;
  }
  for (int i = 0; i < vis.size(); i++) {
      vis.get(i).display(time);
      vis.get(i).checkMouse();
    }
}
/////////////////////////////////////
 class DataHandling {
  private Map<String, LinkedHashSet<String>> dataList;
  Iterator<String> search;
  public DataHandling(){
    dataList = new TreeMap<String, LinkedHashSet<String>>();
    //search = dataList.iterator();
  }
  
  void putData (String data, ArrayList al) {
    String[] dataEntry = data.split(",");
    String d1 = dataEntry[1];
    al.add(d1);
    String d2 = dataEntry[3];
    String d3 = dataEntry[5];
    String d4 = dataEntry[7];
    if (dataList.get(d1) == null){
      dataList.put(d1, new LinkedHashSet<String>());
    }
    dataList.get(d1).add(d2);
    dataList.get(d1).add(d3);
    dataList.get(d1).add(d4);
  }
  
  String getFirst(String k){
    for (String name : dataList.keySet()) {  
            search = dataList.get(name).iterator();
            k = search.next();
          }
    return k;
  }
  
  String getSecond(String k){
    for (String name : dataList.keySet()) {  
            search = dataList.get(name).iterator();
            search.next();
            k = search.next();
          }
    return k;
  }
  
  String getThird(String k){
    for (String name : dataList.keySet()) {  
            search = dataList.get(name).iterator();
            search.next();
            search.next();
            k = search.next();
          }
    return k;
  }
  
  void printMap(){
    out.println(dataList);
  }
}
/////////////////////////////////////////////////////////////////////////////
class Visual {
  String name;
  String grads;
  String employed;
  String unemployed;
  int shade;
  int xpos;
  int ypos;

  public Visual(String nam, String grad, String emp, String unemp, int col, int posx, int posy) {
    name = nam;
    grads = grad;
    employed = emp;
    unemployed = unemp;
    shade = col;
    xpos = posx;
    ypos = posy;
  }

  void checkMouse() { // Checks to see if the mouse is hovering over this object
    if (mouseX > xpos - ((parseInt(grads)/500)/2) && mouseX < xpos + ((parseInt(grads)/500)/2) && mouseY > ypos - 200 && mouseY < ypos + 200){
        out.println(name);   
        showInfo();
    }
  }


  void showInfo() { // Shows info of the object that the mouse is hovering over
    int r = 0;
    int g = 0;
    int b = 0;
    textSize(32);
    fill(255);
    rect(0, 75, 1200, 200);
    
    if(parseInt(unemployed)>1500){
      r=232;
      g=18;
      b=18;
    }
    if(parseInt(unemployed)<=1500 && parseInt(unemployed)>500){
      r=246;
      g=246;
      b=42;
    }
    if(parseInt(unemployed)<500){
      r=42;
      g=246;
      b=42;
    }
    fill(r,g,b);
    text("Major: "+name+" \nNumber of Grads: "+grads+" \nNumber of Grads employed: "+employed+" \nNumber of grads unemployed: "+unemployed, 50, 120);
  }

  void display(int timer) {
    noStroke();
    fill(shade);
    xpos -= timer;
    ellipse(xpos, ypos, parseInt(grads)/500, parseInt(grads)/500);
  }
}
 
 ```
 <br>
This project was designed to teach us how to take in data and load it into a map to then be analyzed. This project was a partner project and it was nice to be able to share ideas and learn how to work with other people in a coding aspect.
 </br>
</details>
<details>
<summary>LinkedList</summary>
 
 ```Java
 void setup() {
  ListFunHouse listrun = new ListFunHouse();
  ListNode test = new ListNode("go", new ListNode("on", new ListNode("at", new ListNode("34", new ListNode("2.1", new ListNode("-a-2-1", new ListNode("up", new ListNode("over", null))))))));
  out.println("Lab15b Test Code\n\n");  

  out.println("Original list values\n");  
  out.println("\n");

  out.println("num nodes = " + listrun.nodeCount(test));

  out.println("\nList values after calling nodeCount\n");  
  listrun.toString(test);
  out.println();    

  listrun.doubleFirst(test);    
  out.println("\nList values after calling doubleFirst\n");              
  listrun.toString(test);
  out.println();   

  listrun.doubleLast(test);    
  out.println("\nList values after calling doubleLast\n");              
  listrun.toString(test);
  out.println();        

  listrun.removeXthNode(test, 2);    
  out.println("\nList values after calling removeXthNode(2)\n");          
  listrun.toString(test);
  out.println();      

  listrun.setXthNode(test, 2, "one");    
  out.println("\nList values after calling setXthNode(2,one)\n");                    
  listrun.toString(test);
  out.println();    

  listrun.removeXthNode(test, 2);    
  out.println("\nList values after calling removeXthNode(2)\n");                    
  listrun.toString(test);
  out.println();
}
///////////////////////////////////////////////////////////////////////////////////
import static java.lang.System.*;
import java.util.LinkedList;
import java.util.ArrayList;
class ListFunHouse
{
   
  public int nodeCount(ListNode list)
  {
    int count=0;
    while (list!=null) {
      count++;
      list= list.getNext();
    }
    return count;
  }

  
  public void doubleFirst(ListNode list)
  {
    list.setNext(new ListNode(list.getValue(), list.getNext()));
  }

 
  public void doubleLast(ListNode list)
  {
    ListNode prev=null;
    while (list!=null &&list.getNext()!=null) {
      list=list.getNext();
    }
    list.setNext(new ListNode(list.getValue(), null));
  }

 
  public void skipEveryOther(ListNode list)
  {
    while (list!=null&&list.getNext()!=null) {
      list.setNext(list.getNext().getNext());
      list=list.getNext();
    }
  }

  
  public void setXthNode(ListNode list, int x, Comparable value)
  {
    int count=1;
    while (list!=null) {
      if (x==count) {
        list.setValue(value);
      }
    }
  }  

 
  public void removeXthNode(ListNode list, int x)
  {  
    ListNode prev= list;
    int count=1;
    if (x==count-1) {
      prev.setNext(list.getNext().getNext());
      count=1;
    } else
      count++;
    prev=list;
    list=list.getNext();
  }
  String toString(ListNode list)
  {
    while (list!=null) {
      print(list.getValue()+" ");
      list=list.getNext();
    }
    return "end";
  }
}


 ```
 
  <br>
This project was desgined to teach us how to use Linked lists in java.
 </br>
</details>
<details>
<summary>Stacks and Queue labs</summary>
 
 ```Java
 import java.util.Stack;
import java.util.Scanner;
import static java.lang.System.*;
Stack<String>circus=new Stack<String>();
int count = 0;
void setup() {
  try{
    Scanner scan = new Scanner(new File("C:/Users/Brendan/Desktop/circus.txt"));
    int num=scan.nextInt();
    for(int i = 0; i<num; i++){
     String name=scan.next();
     if(count%2==0){
      println(name); 
     }else{
      circus.push(name); 
     }
     count++;
    }
    while(!circus.isEmpty()){
      println(circus.pop());
    }
  }
  catch(Exception e){
    println(e);
  }
}
 
 ```
  <br>
These labs were desgined to teach us more about how to use and code up stacks and queues in Java.
 </br>
</details>

<details>
<summary>Final project</summary>



 <br>(https://github.com/kantab/storyFinalPro)
This was the final project that we worked on for this class. I worked on it with a partner Max. It is a madlib of sorts and it asks you questions then generates a story.
 </br>
</details>

***

 This is one of my most worthy peice of code so far. This code is from my JS chemotaxis. I like this code because it was not only a little tricky to figure out how to cycle through the images but I then had to take this code and change it from Java to JavaScript, a language I was learning at the time. What was tricky about cycling through was the fact when I had a mousePressed method, when I would increase the counter that would in turn change the pictures it would add more then once when the mouse was clicked/ pressed. How I solved this is I created a boolean that would flip if the mouse was pressed and when it wasnt it would be flipped back. This then made it able to only increase by one when the mouse was pressed.
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

***

<br>
	This is another worthy peice of code. This code is from my data project. In the code was where you loaded in the data and then had to use a Delimiter to format it how it needed to be for the porgram to take it in and run it properly. It then called all of our funticons to be able to print them out. All of this stuff was relatively know me me and it was definitely good to be able to work with a partner to ease the work load. You can also see in the comments all of the difrent thing that we were trying to work through. I like to leave those in there to either come back to them or to remind me what doesnt work so I do not try them again.
	
</br>

```Java
	void setup() {
  size(1200, 900);
  DataHandling run = new DataHandling();
  ArrayList<String> keys = new ArrayList<String>(); // Keeps track of all keys that are put into the map
  //vis.add(new Visual("X", "x", "x", "s"));
  String [] str=loadStrings("C:/Users/Brendan/Desktop/majors.txt"); 
  String allText=join(str, ","); 
  try {
    Scanner scan = new Scanner(new File("C:/Users/Brendan/Desktop/majors.txt"));
    scan.useDelimiter("/,");
    while (scan.hasNext()) {
      run.putData(scan.nextLine(), keys);
    }
  } 
  catch (Exception e) {
    out.println(e);
    e.printStackTrace();
  } 
  finally {
    //run.printMap();
    //out.println(keys);
  }
  int spaceOut = 0; //How far out new circles must bve put
  for (String s : keys) {
    vis.add(new Visual(s, run.getFirst(s), run.getSecond(s), run.getThird(s), 255, spaceOut + 20 + (parseInt(run.getFirst(s))/500), 400));
    spaceOut += 20 + (parseInt(run.getFirst(s))/500);
    out.println(s + " equals " + run.getFirst(s) + " " + run.getSecond(s) + " " + run.getThird(s));
  }
  /*for (String key : run.dataList.keySet()){
   vis.add(new Visual(key, run.getFirst(key), run.getSecond(key), run.getThird(key)));
   out.println(key + " equals " + run.getFirst(key) + " " + run.getSecond(key) + " " + run.getThird(key));
   }*/
}

```
	
# C++ 

<details>
<summary>Payroll</summary> 
 
 ```cpp
 #include <iostream>
#include <string>
#include <array>
#ifndef Inter_HEADER //stackoverflow do not know what it does but fixed an isue I was having
#define Inter_HEADER

using namespace std;

class Inter {
public:
	Inter() {}
	~Inter() {}
	void setState(double stTax);
	void setFedral(double fdTax);
	void setLocal(double lcTax);
	double stateTaxRate();
	double fedralTaxRate();
	double localTaxRate();
	//double totalTaxRate();
	double totalTaxAmount();
	double payWithTax();
	double getGross();
	void newEmp(double yearPay);
	void newEmp(double hoursWorked, double pay1);
	void newEmp(double hoursWorked, double pay1, int con);





};
#endif
////////////////////////////////////////////////////
#include <iostream>
#include<iomanip>
#include <string>
//#include "payRoll62.cpp"
#include "inter.h"
using namespace std;
	int main() {
		cout << fixed << setprecision(2);
		char inp;
		double hoursWorked;
		double *hr = &hoursWorked;
		double yearPay;
		double pay1;
		double staTax = 0;
		double *st = &staTax;
		double fdrTax = 0;
		double *ft = &fdrTax;
		double lclTax = 0;
		double *lt = &lclTax;
		int con;
		int cou = 0;
		bool loo = false;
		bool isCon = false;
		string firstNm = "";
		string middleNm = "";
		string lastNm = "";



		Inter pay;
		while (true) {
			if (cou < 1) {
				cout << "Enter State tax rates in decimals:" << endl;
				cin >> staTax;
				pay.setState(*st);
				cout << "Enter Fedral tax rates in decimals:" << endl;
				cin >> fdrTax;
				pay.setFedral(*ft);
				cout << "Enter Local tax rates in decimals:" << endl;
				cin >> lclTax;
				pay.setLocal(*lt);
				cou++;
			}

			cout << "Please type s for a salarly employee" << endl;
			cout << "Please type h for a hourly paid employee" << endl;
			cout << "Please type c for a hourly contract employee" << endl;
			cout << "Enter any other key to stop" << endl;
			cin >> inp;

			switch (inp)
			{
			case 's':
				loo = false;
				cout << "Enter employee First, Middle, and then Last name:" << endl;
				cin >> firstNm;
				cin >> middleNm;
				cin >> lastNm;
				cout << "Enter yearly pay:" << endl;
				cin >> yearPay;
				pay.newEmp(yearPay);
				break;
			case 'h':
				loo = true;
				cout << "Enter employee First, Middle, and then Last name:" << endl;
				cin >> firstNm;
				cin >> middleNm;
				cin >> lastNm;
				cout << "Enter hourly pay:" << endl;
				cin >> pay1;
				
				while (true) {
					cout << "Enter employees hours worked:" << endl;
					cin >> *hr;
					try {
						if (*hr > 55) {
							throw 404;
						}
						else {
							break;
						}
					}
					catch (int tc) {
						if (tc == 404) {
							cout << " invalid input:" << endl;
							
						}
						else {
							break;
						}
					}
					/*if (hoursWorked > 45) {
						cout << " invalid input:" << endl;
						//cin >> hoursWorked;
					}
					else {
						break;
					}*/
				}
					pay.newEmp(hoursWorked, pay1);
					break;
			case 'c':
				isCon = true;
				loo = true;
				cout << "Enter employee First, Middle, and then Last name:" << endl;
				cin >> firstNm;
				cin >> middleNm;
				cin >> lastNm;
				cout << "Enter hourly pay:" << endl;
				cin >> pay1;
				cout << "Enter contract number:" << endl;
				cin >> con;
				while (true) {
					cout << "Enter employees hours worked:" << endl;
					cin >> *hr;
					try {
						if (*hr > 45) {
							throw 404;
						}
						else {
							break;
						}
					}
					catch (int tc) {
						if (tc == 404) {
							cout << " invalid input:" << endl;

						}
						else {
							break;
						}
					}
				}
				pay.newEmp(hoursWorked, pay1, con);
				break;
			default:
				cout << "No more employees" << endl;
				return 0;
			}
			if (isCon != true) {
				cout << "Employee: " << endl;
				cout << lastNm << ", " << firstNm << ", " << middleNm.at(0) << endl;
				cout << "Gross weekly pay for this employee is:" << endl;
				cout << pay.getGross() << endl;
				cout << "State Tax for this employee is:" << endl;
				cout << pay.stateTaxRate() << endl;
				cout << "Fedral Tax for this employee is:" << endl;
				cout << pay.fedralTaxRate() << endl;
				cout << "Local Tax for this employee is:" << endl;
				cout << pay.localTaxRate() << endl;
				cout << "Weekly net pay:" << endl;
				cout << pay.payWithTax() << endl;
			}
			else {
				isCon = false;
				cout << "Employee: " << endl;
				cout << lastNm << ", " << firstNm << ", " << middleNm.at(0) << endl;
				cout << "Gross weekly pay for this employee is:" << endl;
				cout << pay.getGross() << endl;
			} 
			}

		return 0;

	};
		
	///////////////////////////////////////////////////////////
 #include <iostream>
#include<iomanip>
#include <string>
#include "inter.h"
using namespace std;
double halfPay = 0;
double doublePay = 0;
double hoursOver = 0;
double hoursIn = 0;
double grs = 0;
double stateTax = 0;
double fedralTax = 0;
double localTax = 0;
const int WKS_IN_YR = 52;


	void Inter :: setState(double stTax) {
		if (stTax != 0) {
			stateTax = stTax;
		}
		else {
			stateTax = 0.05;
		}

	}
	void Inter :: setFedral(double fdTax) {
		if (fdTax != 0) {
			fedralTax = fdTax;
		}
		else {
			fedralTax = 0.10;
		}
	}
	void Inter::setLocal(double lcTax) {
		if (lcTax != 0) {
			localTax = lcTax;
		}
		else {
			localTax = 0.03;
		}

	}
	double Inter::stateTaxRate() {
		return grs * stateTax;
	}
	double Inter::fedralTaxRate() {
		return grs * fedralTax;

	}
	double Inter::localTaxRate() {
		return grs * localTax;

	}
	double Inter::totalTaxAmount() {
		return stateTaxRate() + fedralTaxRate() + localTaxRate();
	}
	double Inter::payWithTax() {
		return grs - totalTaxAmount();
	}

	void Inter::newEmp(double yearPay) { //sal employee
		grs = 0;
		grs = yearPay / WKS_IN_YR;

	}
	void Inter::newEmp(double hoursWorked, double pay1) { // hourly employee 

		halfPay = pay1 / 2 + pay1;
		doublePay = pay1 * 2;

		if (hoursWorked < 41) {
			grs = pay1 * hoursWorked;
		}
		else if (hoursWorked > 40 && hoursWorked < 50) {
			hoursIn = hoursWorked - 40;
			grs = pay1 * 40;
			grs += hoursIn * halfPay;
		}
		else if (hoursWorked >= 50) {
			hoursOver = hoursWorked - 50;
			grs = pay1 * 40;
			grs += 10 * halfPay;
			grs += hoursOver * halfPay;
		}


		grs = 0;
		grs = pay1 * hoursWorked;

	}
	void Inter::newEmp(double hoursWorked, double pay1, int con) { // contract employee
		con = 1;
		grs = 0;
		grs = pay1 * hoursWorked;
	}

	double Inter::getGross() {
		return grs;
	}
	
 ```
<br>
This project was one that I worked on in my introduction to C++ class I took at Inver Hills Community College. This project was designed to teach us how to use things such as setprecision, switchs, try/ catch statements, interfaces, user inputs, and a lot of the key foundations to help learn and understand C++. We made a few different variations of this project and this is the final one.
 </br>
</details>

<details>
<summary>Payroll with creating .txt, and .csv files</summary> 

```cpp
#include <iostream>
#include <regex>
#include <string>
#include <fstream>
#include<cstdlib>
using namespace std;

int main() {
	string fileNm;
	cout << "Enter a name for the file without the extention, the file created will be .txt" << endl;
	cin >> fileNm;
	ofstream outClientFile{ fileNm + ".txt", ios::out };

	if (!outClientFile) {
		cerr << "File could not be opened" << endl;
		exit(EXIT_FAILURE);
	}
	cout << "You will be prompted to enter the Employee Department ID, Employee Number, First Name, Last Name, \nEmail Address, Number of hours worked, and Pay rate, but first\n"
		<< "\nType \"start\" then press enter\n\n Then your inputs one after the other (type input press enter, type input press eter, ect.)\n\n Type end-of-file to end input.\n\n";
	string empDepID;
	string empNum;
	regex integer("(\\+|-)?[[:digit:]]+");
	regex emailReg("^[A-Za-z0-9](([_\.\-]?[a-zA-Z0-9]+)*)@([A-Za-z0-9]+)(([\.\-]?[a-zA-Z0-9]+)*)\.([A-Za-z]{2,})$");
	string nameFst;
	string nameLst;
	string email;
	regex floatin("[-+]?[0-9]*\.?[0-9]+");
	string hrsWrk;
	string payRt;
	string start;

	cin >> start;


	if (start == "end-of-file") {
		return 0;
	}
	while (true) {
		cout << "Enter the employee department ID number: ";
		cin >> empDepID;
		
			if (empDepID == "end-of-file") {
				return 0;
			}
			while (true) {
			if (regex_match(empDepID, integer)) {
				break;
			}
			if (empDepID == "end-of-file") {
				return 0;
			}
			else {
				cout << "invalid input enter a Employee Department Number that meets the requirments:\n The Employee Department ID Number must be a whole number (such as 12345)\n Enter end-of-file to end input." << endl;
				cin >> empDepID;
			}
		}
		cout << "Enter the employee number: ";
		cin >> empNum;
		while (true) {
			if (empNum == "end-of-file") {
				return 0;
			}
			if (regex_match(empNum, integer)) {
				break;
			}
			if (empNum == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a Employee Number that meets the requirments:\n The Employee Number must be a whole number (such as 12345)\n Enter end-of-file to end input." << endl;
				cin >> empNum;
			}
		}
		cout << "Enter the employee First name: ";
		cin >> nameFst;
		while (true) {
			if (nameFst == "end-of-file") {
				return 0;
			}
			if (nameFst.size() < 20) {
				break;
			}
			if (nameFst == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a First Name that meets the requirments:\n The Last Name must be less the 20 charters\n Enter end-of-file to end input." << endl;
				cin >> nameFst;
			}
		}
		cout << "Enter the employee Last name: ";
		cin >> nameLst;
		while (true) {
			if (nameLst == "end-of-file") {
				return 0;
			}
			if (nameLst.size() < 20) {
				break;
			}
			if (nameLst == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a Last Name that meets the requirments:\n The Last Name must be less the 20 charters\n Enter end-of-file to end input." << endl;
				cin >> nameLst;
			}
		}
		cout << "Enter the employee email: ";
		cin >> email;
		while (true) {
			if (email == "end-of-file") {
				return 0;
			}
			if (regex_match(email, emailReg)) {
				break;
			}
			if (email == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a email that meets the requirments:\n Enter end-of-file to end input." << endl;
				cin >> email;
			}
		}
		cout << "Enter the employee number of hours worked: ";
		cin >> hrsWrk;
		while (true) {
			if (hrsWrk == "end-of-file") {
				return 0;
			}
			if (regex_match(hrsWrk, floatin)) {
				break;
			}
			if (hrsWrk == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a valid number for hours worked:\n The hours worked must be a floating point of (such as 55 or 55.55)\n Enter end-of-file to end input." << endl;
				cin >> hrsWrk;
			}
		}
		cout << "Enter the employee pay rate: ";
		cin >> payRt;
		while (true) {
			if (payRt == "end-of-file") {
				return 0;
			}
			if (regex_match(payRt, floatin)) {
				break;
			}
			if (payRt == "end-of-file") {
				return 0;
			}
			else {
				cout << " invalid input enter a Pay Rate that meets the requirments:\n The Pay Rate must be a floating point of (such as 55 or 55.55)\n Enter end-of-file to end input." << endl;
				cin >> payRt;
			}
		}

		outClientFile << empDepID << ' ' << empNum << ' ' << nameFst << ' ' << nameLst << ' ' << email << ' ' << hrsWrk << ' ' << payRt << endl;
		cout << "?Start entering new employee data now or \"end-of-file\" to end program\n";

	}


}
///////////////////////////////////////////////////////
#include <iostream>
#include <string>
#include <fstream>
#include <cstdlib>
#include <iomanip>
#include "readh.h"
using namespace std;
int main() {
	double hrsWrk;
	double payRt;
	int num;
	string nameFst;
	string nameLst;
	string email;
	string fileNm;
	char type;
	payroll emp;


	cout << "enter the name of the file you wish to open, note you do not need to add .txt to the name" << endl;
	cin >> fileNm;

	ifstream inClientFile(fileNm+".txt", ios::in);

	if (!inClientFile) {
		cerr << "File could not be opened" << endl;
		exit(EXIT_FAILURE);
	}

	ofstream outClientFile(fileNm + ".csv", ios::out);

	if (!outClientFile) {
		cerr << "File could not be opened" << endl;
		exit(EXIT_FAILURE);
	}
	while (inClientFile >> email >> nameFst >> nameLst >> hrsWrk >> payRt >> num) {
		emp.newEmp(hrsWrk, payRt);
		outClientFile << num << "," << nameLst << "," << nameFst.at(0) << "," << email << "," << emp.getHrs() << "," << emp.getOverTm() << "," << payRt << "," << emp.getGrs() << " Record" << endl;

		cout << right << "\nEmployee Number" << setw(40) << num << "\nEmployee name" << setw(40) << nameLst << "," << nameFst.at(0) << "\nEmployee email" << setw(40) << email << "\nEmployees normal hours worked" << setw(40) << emp.getHrs() << "\nEmployees overtime hours worked" << setw(40) << emp.getOverTm() << "\nEmployees pay rate" << setw(40) << "$" << payRt << "\nEmployees gross pay" << setw(40) << "$" << emp.getGrs() << endl;
		break;
	}
	return 0;
}


/////////////////////////////////////////////////////////////

#include <string>
#include <iostream>
using namespace std;
class payroll {
public:
	void newEmp(double hrsWrk, double payRt) {
		halfPay = payRt / 2 + payRt;


		if (hrsWrk < 41) {
			hours = hrsWrk;
			grs = payRt * hrsWrk;
		}
		else if (hrsWrk > 40) {
			hoursIn = hrsWrk - 40;
			grs = payRt * 40;
			grs += hoursIn * halfPay;
			overTm = hrsWrk - 40;
		}



		grs = 0;
		grs = payRt * hrsWrk;

	}
	double getGrs() {

		return grs;

	}
	double getHrs() {

		return hours;

	}
	double getOverTm() {

		return overTm;

	}

private:

	double halfPay = 0;
	double hoursOver = 0;
	double hoursIn = 0;
	double grs = 0;
	double hours;
	double overTm;
	double payRt;

};
//////////////////////////////////////////////

```
<br>
This project was the Final we had for the class. The goal of the project was to be able to create a .txt file in one program that would take in user inputs and use Regular Expressions and other methods to make sure what the user had enter follows the guide lines for the project. We then had to in a separate program take that .txt file in and use some of the inputs from it to create a .csv file that did some payroll calculations.
</br>
</details>


