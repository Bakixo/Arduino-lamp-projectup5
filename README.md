# Arduino-lamp-projectup5
Servo motor oscillating between 0 degrees and 180 degrees



#include <Servo.h>

Servo motor; 

int pos=0;

void setup(){

motor.attach(9);



}

void loop(){

  for (pos = 0; pos <= 180; pos +=1) {
  motor.write(pos);
  delay(10);

  }
  for (pos = 180; pos >= 0; pos -=1) {
  motor.write(pos);
  delay(10);

  }
}
