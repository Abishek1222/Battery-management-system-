# Battery-management-system-
Embedded C Code (Arduino):

float batteryVoltage;
int sensorPin = A0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(sensorPin);
  batteryVoltage = sensorValue * (5.0 / 1023.0);
  Serial.print("Battery Voltage: ");
  Serial.println(batteryVoltage);
  delay(1000);
}
