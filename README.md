Indoor-Location-Monitor
=======================

Read and display Smarties Project IR sent data


This is for a simulation DO NOT USE , the finished solution will be uploaded by the end of June.


This is used to display the position recived by an Arduino Uno card transmitted via port COM19 (Windows).

The real case application scenario would be for the arduino to read this value using an IR reader, and then transmit it.


For test purposes you can use this Arduino sketch to generate the needed Json :


```C
void setup(){
  Serial.begin(2400);
}

void loop(){
  
  int i =0;
  String toSend0="{\"x\":";
    String toSend1;
    String toSend2;
  while(i<4){
    toSend1= toSend0+ i;
    toSend2 =  toSend1 +", \"y\":3, \"z\":0, \"timestamp\":800, \"crc\":39763}";
  Serial.println(toSend2);
  i++;
  delay(1000);
  }
}


```
