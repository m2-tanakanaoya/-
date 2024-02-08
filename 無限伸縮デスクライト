float baseH = 3;
float baseX = 0;
float baseY = 0;

float arm1W = 10;
float arm1D = 10;
float arm1L = 20;

float arm2W = 7;
float arm2D = 7;
float arm2L = 40;

float arm3W = 4;
float arm3D = 4;
float arm3L = 30;


float angle0 = 0;
float angle1 = 0;
float angle2 = 0;
float angle3 = 0;
float length1 = 0;

float dif1 = 1.0;

int boxColor = color(0,170);  // 初期の色（黒）

void setup(){
  
  size(1200, 800, P3D);
  
  camera(150, 100, 150, 0, 0, 60, 0, 0, -1);
  
  noStroke();  
}


void draw(){
  
  background(255);
  
  
  if(keyPressed){
  
    if(key == 'z'){
      angle0 = angle0 + dif1;
    }
    if(key == 'Z'){
      angle0 = angle0 - dif1;
    }
    if(key == 'x'){
      angle1 = angle1 + dif1;
    }
    if(key == 'X'){
      angle1 = angle1 - dif1;
    }
    if(key == 'c'){
      angle2 = angle2 + dif1;
    }
    if(key == 'C'){
      angle2 = angle2 - dif1;
    }
    if(key == 'v'){
      length1 = length1 + dif1;
    }
    if(key == 'V'){
      length1 = length1 - dif1;
    }
    if(key == 'R'){
      angle0 = 0;
      angle1 = 0;
      angle2 = 0;
      angle3 = 0;
      length1 = 0;
      boxColor = color(0,170);
  }
  }
  if (key == '1') {
    boxColor = color(255, 0, 0, 170);  // 赤
  } else if (key == '2') {
    boxColor = color(0, 255, 0, 170);  // 緑
  } else if (key == '3') {
    boxColor = color(0, 0, 255, 170);  // 青
  }else if (key == '4') {
    boxColor = color(240, 240, 0, 170);  // 黄
  }else if (key == '5') {
    boxColor = color(0);  // 黒
  }else if (key == '6') {
    boxColor = color(random(255), random(255), random(255),170);  // ランダム配色
  }

  //base
  translate(baseX,baseY,baseH/2);
  rotateZ(radians(angle0));
  fill(10,100,100,150);
  box(20,20,baseH);
  stroke(0);
    
  //1st link
  translate(0,0,arm1L/2+2);
  fill(0,170);
  box(arm1W,arm1D,arm1L);
  stroke(0);
  
  //関節 1
  translate(0,0,arm1L/2+2);
  rotateX(radians(angle1));
  sphere(2);
  
  //2nd link
  translate(0,0,2+arm2L/2+length1);
  fill(0,170);
  box(arm2W,arm2D,arm2L+2*length1);
  stroke(0);
  
 //関節 2
  translate(0,0,arm2L/2+2+length1);
  rotateX(radians(angle2));
  sphere(2);
  
  //3rd link
  translate(0,0,2+arm3L/2);
  fill(0,170);
  box(arm3W,arm3D,arm3L);
  stroke(0);
  
  //light
  translate(0,0,7.5+arm3L/2);
  fill(boxColor);
  box(100,4,15);
  
  
}
  
