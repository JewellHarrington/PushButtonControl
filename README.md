# PushButtonControl
// Example 03B: Turned an LED on and off with a button  // I copied this code and changed the LED and Buttons after having trouble  // with the redboard  //started by watching many Youtube videos and web researching //feels like I'm finally understanding  //started with wires, green LED, pentontemeter, resitor, arduino examples, //redboard, breadboard  //pentontometer exchanged for button to complete circuit, something wasnt working //many failures experienced before lighting the LED  //due to possibly not uploading the example sketch for the board correctly //what changed was that sketch was uploade correctly, the one from github  //after a lot of relief from board working correctly decided to just switch pins //pin 13 was switched for 12 and I dont remember what pin 8 was switched from //I ended up with the board and LED wprking correctly  //was begining to think my board was damaged somehow possibly due to shipment  //This project has and will continue to lead to a greater understanding of boards //and electronics for me //and I hope others as well //GOOD NIGHT, AND THANK YOU FOR ATTENDING, DTC 338 VANCOUVER!!!  #define LED 12         // LED pin #define BUTTON 8       // input pin for Pushbutton                                                int val = 0;         // val will be used to store the state                     // of the input pin                      int old_val = 0;   // this variable stores the previous                   // value of "val" int state = 0;      // 0 = LED off and 1 = LED on  void setup() {  pinMode(LED, OUTPUT);     // tell Arduino LED is an output pinMode(BUTTON, INPUT);    // and BUTTON is an input }   void loop(){ val = digitalRead(BUTTON);     // read input value and store it                                                    // check if there was a transition                               if ((val == HIGH) &amp;&amp; (old_val == LOW)){ state = 1 - state; }  old_val = val;             // val is now old, let's store it  if (state == 1) { digitalWrite(LED, HIGH);    // turn LED ON } else { digitalWrite(LED, LOW); } }
Sketch for pushbutton


//This is my pushbutton sketch
// I copied this code and changed the LED and Buttons after having trouble 
// with the redboard

//started by watching many Youtube videos and web researching
//feels like I'm finally understanding

//started with wires, green LED, pentontemeter, resitor, arduino examples,
//redboard, breadboard

//pentontometer exchanged for button to complete circuit, something wasnt working
//many failures experienced before lighting the LED

//due to possibly not uploading the example sketch for the board correctly
//what changed was that sketch was uploade correctly, the one from github

//after a lot of relief from board working correctly decided to just switch pins
//pin 13 was switched for 12 and I dont remember what pin 8 was switched from
//I ended up with the board and LED wprking correctly

//was begining to think my board was damaged somehow possibly due to shipment

//This project has and will continue to lead to a greater understanding of boards
//and electronics for me
//and I hope others as well
//GOOD NIGHT, AND THANK YOU FOR ATTENDING, DTC 338 VANCOUVER!!!

#define LED 12         // LED pin
#define BUTTON 8       // input pin for Pushbutton
                      
                       
int val = 0;         // val will be used to store the state
                    // of the input pin
                    
int old_val = 0;   // this variable stores the previous
                  // value of "val"
int state = 0;      // 0 = LED off and 1 = LED on

void setup() {

pinMode(LED, OUTPUT);     // tell Arduino LED is an output
pinMode(BUTTON, INPUT);    // and BUTTON is an input
}


void loop(){
val = digitalRead(BUTTON);     // read input value and store it
                     
                             // check if there was a transition
                             
if ((val == HIGH) && (old_val == LOW)){
state = 1 - state;
}

old_val = val;             // val is now old, let's store it

if (state == 1) {
digitalWrite(LED, HIGH);    // turn LED ON
} else {
digitalWrite(LED, LOW);
}
}
