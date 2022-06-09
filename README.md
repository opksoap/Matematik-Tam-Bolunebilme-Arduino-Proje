# Matematik-Tam-Bolunebilme-Arduino-Proje

# Girilen Sayının 1'den 10'a kadar ki olan sayilara tam bolunup bolunmedigini kontrol eden. Bolunuyorsa sarı, bolunmuyorsa kirmizi isigi yakan bir arduino projesidir.

int gelen=0;

void setup() {
  Serial.begin(9600);
  pinMode(2,OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(4,OUTPUT);
  pinMode(5,OUTPUT);
  pinMode(6,OUTPUT);
  pinMode(7,OUTPUT);
  pinMode(8,OUTPUT);
  pinMode(9,OUTPUT);
  pinMode(10,OUTPUT);
  pinMode(11,OUTPUT);
  pinMode(12,OUTPUT);
  pinMode(13,OUTPUT);
  pinMode(A0,OUTPUT);
  pinMode(A1,OUTPUT);
  pinMode(A2,OUTPUT);
  pinMode(A3,OUTPUT);
  pinMode(A4,OUTPUT);
  pinMode(A5,OUTPUT);
  
}

void loop() {
  if(Serial.available()>1)
  {
  gelen = Serial.parseInt();
  Serial.println(gelen);
  if (gelen%2==0)
  {
  digitalWrite(13,HIGH);
  Serial.println(gelen/2);
  digitalWrite(9,LOW);
  delay(1000);
  }
  else
  {
  digitalWrite(13,LOW);
  digitalWrite(9,HIGH);
  delay(1000);
  }
  if (gelen%3==0){
    digitalWrite(12,HIGH);
    Serial.println(gelen/3);
    digitalWrite(8,LOW);
    delay(1000);
  }
  else{
    digitalWrite(12,LOW);
    digitalWrite(8,HIGH);
    delay(1000);
  }
  if (gelen%4==0){
    digitalWrite(11,HIGH);
    Serial.println(gelen/4);
    digitalWrite(7,LOW);
    delay(1000);
  }
  else{
    digitalWrite(11,LOW);
    digitalWrite(7,HIGH);
    delay(1000);
  }
  if(gelen%5==0){
    digitalWrite(10,HIGH);
    Serial.println(gelen/5);
    digitalWrite(6,LOW);
    delay(1000);
  }
  else{
    digitalWrite(10,LOW);
    digitalWrite(6,HIGH);
    delay(1000);
  }
    if(gelen%6==0){
    digitalWrite(A0,HIGH);
    Serial.println(gelen/6);
    digitalWrite(5,LOW);
    delay(1000);
  }
  else{
    digitalWrite(A0,LOW);
    digitalWrite(5,HIGH);
    delay(1000);
  }
    if(gelen%7==0){
    digitalWrite(A1,HIGH);
    Serial.println(gelen/7);
    digitalWrite(4,LOW);
    delay(1000);
  }
  else{
    digitalWrite(A1,LOW);
    digitalWrite(4,HIGH);
    delay(1000);
  }
    if(gelen%8==0){
    digitalWrite(A2,HIGH);
    Serial.println(gelen/8);
    digitalWrite(3,LOW);
    delay(1000);
  }
  else{
    digitalWrite(A2,LOW);
    digitalWrite(3,HIGH);
    delay(1000);
  }
    if(gelen%9==0){
    digitalWrite(A3,HIGH);
    Serial.println(gelen/9);
    digitalWrite(2,LOW);
    delay(1000);
  }
  else{
    digitalWrite(A3,LOW);
    digitalWrite(2,HIGH);
    delay(1000);
  }
    if(gelen%10==0){
    digitalWrite(A4,HIGH);
    Serial.println(gelen/10);
    digitalWrite(A5,LOW);
    delay(1000);
  }
  else{
    digitalWrite(A4,LOW);
    digitalWrite(A5,HIGH);
    delay(1000);
  }
  }
  else
  return;  
  }
