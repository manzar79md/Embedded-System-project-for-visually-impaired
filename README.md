const int trigPin = 12;
const int echoPin = 14;
const int buzzerPin = 15;
const int ledPin = 16;  // LED in place of the vibration motor

void setup() {
  Serial.begin(115200);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  long distance = getDistance();

  Serial.println("Distance: " + String(distance) + " cm");

  if (distance < 50) {
    Serial.println("Activating Buzzer and LED");
    tone(buzzerPin, 2000, 1000);  // Buzzer on
    digitalWrite(ledPin, HIGH);  // LED on
    delay(1000);
    noTone(buzzerPin);  // Buzzer off
    digitalWrite(ledPin, LOW);  // LED off
  }

  delay(500);
}

long getDistance() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  return pulseIn(echoPin, HIGH) * 0.034 / 2;
}
