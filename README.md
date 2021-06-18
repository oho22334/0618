# 0618
```C
void setup(){
  size(400,200);
  textSize(40);
}
String line="";
String []Q= {"hello","world","other"};
int Qi=0;///第幾個Q
void draw(){
  background(0);
  text("Score: "+score, 100,50);
  text("Q:  "+Q[Qi],     100,100);
  text("A:  "+line,  100,150);
}
int score=0;
void keyPressed(){///鍵盤輸入
  int len =line.length();
  if( key>='a' && key<='z') line =line+key;
  if( key>='A' && key<='Z') line =line+key;
  if( key == BACKSPACE && len>0) line = line.substring(0,len-1);
  if( key == ENTER ){
    if(line.equals(Q[Qi])==true ){
      score++;
      Qi++;///換下一筆 ex:Q[0]---->Q[1]
      line ="";
    }else score --;
  }
}//Q:分數
```
