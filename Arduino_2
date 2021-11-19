int ledPin = 13;  // choose the pin for the LED
int inputPin = 2;               
int pirState = LOW;             
int val = 2;  
int piezoPin = 12;
       
void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(piezoPin, OUTPUT); 
  pinMode(inputPin, INPUT);
  Serial.begin(9600);

}
 
void loop(){
  val = digitalRead(inputPin);  // read input value
  if (val == HIGH) {            // check if the input is HIGH
    digitalWrite(ledPin, HIGH);
    digitalWrite(ledPin, HIGH);
    tone(piezoPin, 1000, 600);
    // turn LED ON
    if (pirState == LOW) {
      Serial.println("Motion Detected!");
      pirState = HIGH;
    }
  } else {
    digitalWrite(ledPin, LOW);
  
    if (pirState == HIGH){
      
      Serial.println("Motion ended!");
      
      pirState = LOW;
    }
  }
}
