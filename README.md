# ສາລະບານ

- **ບົດນຳ**

- Blink

- Experiment Blink

- Switch

- RGB

- Buzzer

- Potentiometer

- Relay

- Servo

- Seven Segment

- Color Matching Sound Alarm System

- See Battery with LED and Seven Segment
  
- Assignment

- Midterm

# ບົດນຳ

#### ໄມໂຄຄອມພິວເຕີ (Microcomputer) ແລະໄມໂຄຣໂປຣເຊັດເຊີ (Microprocessor) ແມ່ນສ່ວນສຳຄັນຂອງລະບົບໄຟຟ້າໃນອຸດສາຫະກຳ, ຄອມພິວເຕີ, ແລະໂທລະສັບ. ບົດລາຍງານນີ້ເປັນການສຳຫຼວດທົດລອງຄວາມສາມາດຂອງໄມໂຄຄອມພິວເຕີຜ່ານການຄວບຄຸມອຸປະກອນຕ່າງໆ ລວມມີ: LED, Switch, RGB LED, Buzzer, Potentiometer, Relay, Servo ແລະ Seven Segment Display.

# ບົດທີ 0: [Blink](https://www.tinkercad.com/things/khVy8mx2xD4-experiment-blink?sharecode=Fum-S0GvZ34HScHrmkwTZ5MU0M8MI4tM_PCyENtME0I)

#### ບົດລາຍງານຂອງໂຄດ Blink ໃນພາສາ C++

- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການຄວບຄຸມ LED ດ້ວຍ Arduino.
  - ອຸປະກອນ: Arduino, LED (pin 13).
  - ໂຄດໃຊ້: digitalWrite(LED_BUILTIN, HIGH/LOW); ລູບຊ້ຳໂດຍມີ delay(1000);

### 1\. ບົດນຳ

- ໂຄດນີ້ເປັນຕົວຢ່າງພື້ນຖານຂອງການນຳໃຊ້ Arduino ສໍາລັບເຮັດໃຫ້ LED ເທິງບອດກະພິບ (Blink) ໂດຍນຳໃຊ້ຟັງຊັນພື້ນຖານຂອງ Arduino ເຊັ່ນ pinMode() ແລະ digitalWrite() ເພື່ອກຳນົດໂໝດ ແລະ ສະຖານະຂອງ output

### 2\. ອຸປະກອນທີ່ໃຊ້

- ບອດ Arduino (ເຊັ່ນ Arduino Uno, Arduino Mega ເປັນຕົ້ນ)
- ໄຟ LED ທີ່ຢູ່ໃນບອດ (LED_BUILTIN)
- ສາຍ USB ສຳລັບເຊື່ອມຕໍ່ກັບຄອມພິວເຕີ

### 3\. ການອະທິບາຍໂຄດ

- ໂຄດນີ້ປະກອບໄປດ້ວຍສອງຟັງຊັນຫຼັກໄດ້ແກ່ setup() ແລະ loop()

### 3.1 ຟັງຊັນ setup()
```
void setup() {

pinMode(LED_BUILTIN, OUTPUT); // ກຳນົດໃຫ້ຂາ LED_BUILTIN ເປັນຂາ OUTPUT

}
```
- ຟັງຊັນນີ້ຈະເຮັດວຽກພຽງຄັ້ງດຽວເມື່ອເລີ່ມຕົ້ນໃຊ້ງານບອດ
- ໃຊ້ຄຳສັ່ງ pinMode(LED_BUILTIN, OUTPUT); ເພື່ອກຳນົດໃຫ້ຂາ LED_BUILTIN (ຂາ 13 ຂອງ Arduino) ເປັນຂາອອກ

### 3.2 ຟັງຊັນ loop()
```
void loop() {

digitalWrite(LED_BUILTIN, HIGH); // ເປີດ LED

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

digitalWrite(LED_BUILTIN, LOW); // ປິດ LED

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

}
```
- ຟັງຊັນ loop() ຈະເຮັດວຽກຊ້ຳໄປຊ້ຳມາ
- ໃຊ້ຄຳສັ່ງ digitalWrite(LED_BUILTIN, HIGH); ເພື່ອເປີດ LED
- ໃຊ້ຄຳສັ່ງ delay(1000); ເພື່ອລໍຖ້າ 1 ວິນາທີ
- ໃຊ້ຄຳສັ່ງ digitalWrite(LED_BUILTIN, LOW); ເພື່ອປິດ LED
- ໃຊ້ຄຳສັ່ງ delay(1000); ເພື່ອລໍຖ້າ 1 ວິນາທີ ກ່ອນທີ່ຈະເຮັດຊ້ຳໃໝ່

### 4\. ການເຮັດວຽກຂອງໂຄດ

1. ເມື່ອອັບໂຫລດໂຄດໃສ່ Arduino ແລະເລີ່ມຕົ້ນໃຊ້ງານ LED ຈະຕິດເປັນເວລາ 1 ວິນາທີ
2. ຫຼັງຈາກນັ້ນ LED ຈະດັບເປັນເວລາ 1 ວິນາທີ
3. ວົງຈອນນີ້ຈະເຮັດວຽກຊ້ຳໄປເລື່ອຍໆ

### 5\. ຂໍ້ສັງເກດ

- ຖ້າຕ້ອງການໃຫ້ LED ກະພິບໄວຂຶ້ນ ຫຼື ນານຂຶ້ນ ສາມາດປ່ຽນຄ່າ delay() ໄດ້ ເຊັ່ນ delay(500); ຈະເຮັດໃຫ້ LED ກະພິບໄວຂຶ້ນ
- ຖ້າຕ້ອງການໃຊ້ LED ພາຍນອກ ຄວນເຊື່ອມ LED ຜ່ານຕົວຕ້ານ (ເຊັ່ນ 220 ໂອມ) ທີ່ຂາ 13 ແລະ GND ຂອງບອດ

### 6\. ຮູບວົງຈອນ
<img width="451" alt="image" src="https://github.com/user-attachments/assets/ba29f29e-e746-4af2-92e7-2b87223eb079" />

### 7\. ສະຫຼຸບ

ໂຄດ Blink ນີ້ເປັນໂຄດພື້ນຖານທີ່ໃຊ້ໃນ Arduino ເພື່ອສາທິດການຄວບຄຸມ output ໂດຍໃຊ້ LED ໃນການສະແດງຜົນ. ການເຂົ້າໃຈໂຄດນີ້ເປັນພື້ນຖານສຳຄັນໃນການຮຽນຮູ້ການຂຽນໂປຣແກຣມ ແລະ ການເຮັດວຽກຂອງອຸປະກອນໄຟຟ້າທີ່ຄວບຄຸມໂດຍໄມໂຄຣຄອນໂທຣລເລີ

# ບົດທີ 1 [Experiment Blink](https://www.tinkercad.com/things/khVy8mx2xD4-experiment-blink?sharecode=Fum-S0GvZ34HScHrmkwTZ5MU0M8MI4tM_PCyENtME0I)

#### ບົດລາຍງານຂອງ Experiment Blink ໃນພາສາ C++

### 1\. ບົດນຳ

- ໂຄດນີ້ເປັນຕົວຢ່າງພື້ນຖານຂອງການນຳໃຊ້ Arduino ສໍາລັບເຮັດໃຫ້ LED ກະພິບ (Blink) ໂດຍນຳໃຊ້ຟັງຊັນພື້ນຖານຂອງ Arduino ເຊັ່ນ pinMode() ແລະ digitalWrite() ເພື່ອກຳນົດໂໝດ ແລະສະຖານະຂອງ output

### 2\. ອຸປະກອນທີ່ໃຊ້

- ໄມໂຄຣຄອນໂທຣລເລີ (Arduino)

- LED

- ຕົວຕ້ານ (220Ω)

- ສາຍຈຳເຊີ (Jumper wires)

- ເບຣດບອດ (Breadboard)

- ສາຍ USB ສຳລັບເຊື່ອມຕໍ່ກັບຄອມພິວເຕີ

### 3\. ການອະທິບາຍໂຄດ

- ໂຄດນີ້ປະກອບໄປດ້ວຍສອງຟັງຊັນຫຼັກໄດ້ແກ່ setup() ແລະ loop()

### 3.1 ຟັງຊັນ setup()
```
void setup() {

pinMode(LED_BUILTIN, OUTPUT); // ກຳນົດໃຫ້ຂາ LED_BUILTIN ເປັນຂາ OUTPUT

}
```
### 3.2 ຟັງຊັນ loop()
```
void loop() {

digitalWrite(LED_BUILTIN, HIGH); // ເປີດ LED

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

digitalWrite(LED_BUILTIN, LOW); // ປິດ LED

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

}
```
### 4\. ການເຮັດວຽກຂອງໂຄດ

1. ເມື່ອອັບໂຫລດໂຄດໃສ່ Arduino ແລະເລີ່ມຕົ້ນໃຊ້ງານ LED ຈະຕິດເປັນເວລາ 1 ວິນາທີ

2. ຫຼັງຈາກນັ້ນ LED ຈະດັບເປັນເວລາ 1 ວິນາທີ

3. ວົງຈອນນີ້ຈະເຮັດວຽກຊ້ຳໄປເລື່ອຍໆ

### 5\. ຂໍ້ສັງເກດ

- ຖ້າຕ້ອງການໃຫ້ LED ກະພິບໄວຂຶ້ນ ຫຼື ນານຂຶ້ນ ສາມາດປ່ຽນຄ່າ delay() ໄດ້

- ຖ້າໃຊ້ LED ພາຍນອກ ຕ້ອງໃຊ້ຕົວຕ້ານ 220Ω ຕໍ່ອອກຈາກຂາອອກ

### 6\. ຮູບວົງຈອນ
<img width="386" alt="image" src="https://github.com/user-attachments/assets/deef2faa-6e65-4fd4-b0de-b442c2c3f347" />

### 7\. ສະຫຼຸບ

- ໂຄດ Experiment Blink ນີ້ເປັນຕົວຢ່າງພື້ນຖານທີ່ໃຊ້ໃນ Arduino ເພື່ອສາທິດການຄວບຄຸມຂາ output ໂດຍໃຊ້ LED. ການເຂົ້າໃຈໂຄດນີ້ເປັນພື້ນຖານສຳຄັນໃນການຮຽນຮູ້ການຂຽນໂປຣແກຣມ ແລະ ການເຮັດວຽກຂອງອຸປະກອນໄຟຟ້າທີ່ຄວບຄຸມໂດຍໄມໂຄຣຄອນໂທຣລເລີ

# ບົດທີ 2 Switch

- ບົດລາຍງານຂອງ Experiment Switch ໃນພາສາ C++
- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການອ່ານ input ແລະ ຄວບຄຸມ output.
  - ອຸປະກອນ: Arduino, Pushbutton, LED, Resistor.
  - ໂຄດທີ່ໃຊ້: digitalRead() ກວດສອບ button ແລະ digitalWrite() ເປີດ/ປິດ LED.

### 1\. ບົດນຳ

- ໂຄດນີ້ເປັນການສາທິດວິທີການໃຊ້ປຸ່ມກົດ (Push Button) ກັບ Arduino ໂດຍປຸ່ມກົດຈະຖືກເຊື່ອມຕໍ່ກັບຂາ 2 (INPUT) ຂອງ Arduino ແລະ ໃຊ້ປະມວນຜົນເພື່ອຄວບຄຸມສະຖານະຂອງ LED ທີ່ຕິດຕັ້ງຢູ່ບອດ.

### 2\. ອຸປະກອນທີ່ໃຊ້

- ໄມໂຄຣຄອນໂທຣລເລີ (Arduino)
- LED
- ປຸ່ມກົດ (Push Button)
- ຕົວຕ້ານ (220Ω ຫຼື 10KΩ ຂື້ນກັບວິທີໃຊ້ Pull-down/Pull-up)
- ສາຍຈຳເປິ (Jumper wires)
- ເບຣດບອດ (Breadboard)
- ສາຍ USB ສຳລັບເຊື່ອມຕໍ່ກັບຄອມພິວເຕີ

### 3\. ການອະທິບາຍໂຄດ

- ໂຄດນີ້ປະກອບໄປດ້ວຍສອງຟັງຊັນຫຼັກໄດ້ແກ່ setup() ແລະ loop()

### 3.1 ຟັງຊັນ setup()
```
void setup()

{

pinMode(2, INPUT); // ກຳນົດຂາ 2 ເປັນ INPUT ສໍາລັບປຸ່ມກົດ

pinMode(LED_BUILTIN, OUTPUT); // ກຳນົດໃຫ້ LED_BUILTIN ເປັນ OUTPUT

Serial.begin(9600); // ຕັ້ງຄ່າ Serial Monitor ທີ່ baud rate 9600

}
```
### 3.2 ຟັງຊັນ loop()
```
void loop()

{

buttonState = digitalRead(2); // ອ່ານຄ່າຈາກປຸ່ມກົດ

if (buttonState == HIGH) {

Serial.println("Button HIGH"); // ສະແດງຜົນຜ່ານ Serial Monitor

digitalWrite(LED_BUILTIN, HIGH); // ເປີດ LED

} else {

Serial.println("Button LOW");

digitalWrite(LED_BUILTIN, LOW); // ປິດ LED

}

delay(10); // ດຶງເວລາໃຫ້ການຈຳລອງດີຂຶ້ນ

}
```
### 4\. ການເຮັດວຽກຂອງໂຄດ

1. ປຸ່ມກົດຖືກເຊື່ອມຕໍ່ຂາ 2 (INPUT)
2. ເມື່ອກົດປຸ່ມ, ຄ່າ buttonState ຈະຖືກອ່ານເປັນ HIGH
3. ຖ້າ buttonState == HIGH, LED ຈະຕິດ
4. ເມື່ອປ່ອຍປຸ່ມ, buttonState ຈະກັບເປັນ LOW ແລະ LED ຈະດັບ
5. ສະຖານະຖືກສົ່ງໄປຫາ Serial Monitor ໃຫ້ເຫັນຜົນທາງຄອມພິວເຕີ

### 5\. ຂໍ້ສັງເກດ

- ຖ້າບໍ່ມີຕົວຕ້ານ Pull-down (10KΩ) ປຸ່ມອາດຈະໃຫ້ຄ່າຜິດພາດເພາະມີສັນຍານຮົ່ວ
- ສາມາດໃຊ້ Pull-up ຂອງ Arduino ໂດຍກຳນົດ pinMode(2, INPUT_PULLUP);
- ໃນກໍລະນີໃຊ້ Pull-up, ປຸ່ມກົດຈະໃຫ້ຄ່າ LOW ແທນສູງສຸດຂອງສັນຍານ.

### 6\. ຮູບວົງຈອນ
<img width="301" alt="image" src="https://github.com/user-attachments/assets/21e79a79-5b2e-4bc7-8930-720991cf2e28" />

### 7\. ສະຫຼຸບ

- Experiment Switch ເປັນຄວາມຮູ້ພື້ນຖານທີ່ຈຳເປັນສຳລັບການນຳໃຊ້ປຸ່ມກົດໃນ Arduino. ມັນສາມາດນຳໄປປັບໃຊ້ໃນໂຄງການອື່ນໆ ທີ່ມີການໃຊ້ປຸ່ມຄວບຄຸມການເຮັດວຽກຂອງອຸປະກອນຕ່າງໆ.

# ບົດທີ 3 RGB

#### ບົດລາຍງານຂອງ RGB LED Control

- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການປະສົມສີຂອງ RGB LED.
  - ອຸປະກອນ: Arduino, RGB LED, Resistor.
  - ໂຄດທີ່ໃຊ້: analogWrite() ຄວບຄຸມຄວາມສະຫວ່າງສີແດງ, ຂຽວ, ຟ້າ.

### 1\. ບົດນຳ

- ໂຄດນີ້ເປັນຕົວຢ່າງພື້ນຖານຂອງການຄວບຄຸມ RGB LED ດ້ວຍ Arduino, ມັນໃຊ້ຟັງຊັນ Arduino ພື້ນຖານເຊັ່ນ pinMode() ແລະ digitalWrite() ເພື່ອກໍານົດ pins ແລະສະຖານະຂອງ LED, ເຊັ່ນດຽວກັນກັບໄດ້ຮັບຄໍາສັ່ງຈາກ Serial Monitor ເພື່ອເປີດແລະປິດ LED ຕາມຄວາມຕ້ອງການຂອງຜູ້ໃຊ້.

### 2\. ອຸປະກອນທີ່ໃຊ້

- ບອດ Arduino (ເຊັ່ນ Arduino Uno, Arduino Mega ເປັນຕົ້ນ)
- RGB LED
- ສາຍ USB ສຳລັບເຊື່ອມຕໍ່ກັບຄອມພິວເຕີ
- ຕົວຕ້ານ 220 ໂອມ ທີ່ຕິດກັບ RGB LED

### 3\. ການອະທິບາຍໂຄດ

- ໂຄດນີ້ປະກອບໄປດ້ວຍຟັງຊັນຫຼັກ 2 ຕົວເຊັ່ນ: setup() และ loop()

### 3.1 ຟັງຊັນ setup()
```
void setup() {

Serial.begin(9600); // Initialize serial communication

for (int i = 0; i < 3; i++) {

pinMode(ledPins\[i\], OUTPUT); // Set LED pins as OUTPUT

}
}
```
- ຟັງຊັນນີ້ເຮັດວຽກພຽງຄັ້ງດຽວເມື່ອເລີ່ມຕົ້ນໃຊ້ງານບອດ ໂດຍໃຊ້ຄຳສັ່ງ pinMode() ເພື່ອກຳນົດຂາຄວບຄຸມສີ RGB.

### 3.2 ຟັງຊັນ loop()
```
void loop() {

while (Serial.available() > 0) {

String input = Serial.readStringUntil('\\n'); // Read input from serial monitor

for (int i = 0; i < 3; i++) {

digitalWrite(ledPins\[i\], LOW); // Turn off all LEDs

}

if (input == "on" || input == "rgb") {

// Turn on all LEDs

for (int i = 0; i < 3; i++) {

digitalWrite(ledPins\[i\], HIGH);

}

} else if (input == "off") {

// Turn off all LEDs

for (int i = 0; i < 3; i++) {

digitalWrite(ledPins\[i\], LOW);

}

} else if (input == "r") {

digitalWrite(ledPins\[0\], HIGH); // Turn on Red LED

} else if (input == "g") {

digitalWrite(ledPins\[1\], HIGH); // Turn on Green LED

} else if (input == "b") {

digitalWrite(ledPins\[2\], HIGH); // Turn on Blue LED

} else {

allColors(); // Handle other colors

}

}

}
```
- ຟັງຊັນ loop() ຈະເຮັດຊ້ຳຕົວມັນເອງຢ່າງບໍ່ມີກຳນົດ ເພື່ອລໍຖ້າຄໍາສັ່ງຈາກ Serial Monitor.

### 3.3 ຟັງຊັນ allColors()
```
void allColors() {

for(int i = 0; i < 3; i++) {

digitalWrite(ledPins\[i\], HIGH); // Turn on all LEDs

}

delay(100);

for(int i = 0; i < 3; i++) {

digitalWrite(ledPins\[i\], LOW); // Turn off LEDs

}

delay(100);

}
```
- ຟັງຊັນ allColors() ມັນຈະອ່ານຂໍ້ມູນ ແລະ ປະມວນຜົນການເປີດ-ປິດ LEDs ຕາມຄໍາສັ່ງທີ່ໄດ້ຮັບ, ເຊັ່ນ: ຄໍາສັ່ງທີ່ຈະເປີດໄຟ LED ທຸກຄັ້ງ ("on", "rgb") ຫຼື ເປີດ LED ສີດຽວ ("r", "g", "b").

### 4\. ການເຮັດວຽກຂອງໂຄດ

1. ເມື່ອອັບໂຫຼດໂຄດໃສ່ Arduino ແລະ ເລີ່ມຕົ້ນໃຊ້ງານ RGB LED ຈະຕິດເປັນເວລາ 1 ວິນາທີ ຫຼັງຈາກນັ້ນ LED ຈະດັບເປັນເວລາ 1 ວິນາທີ

### 5\. ຂໍ້ສັງເກດ

- ຖ້າຕ້ອງການໃຫ້ RGB LED ດັບໄວຂຶ້ນ, ສາມາດປ່ຽນຄ່າ delay() ຕໍ່ໄປນີ້: delay(500).

### 6\. ຮູບວົງຈອນ
<img width="342" alt="image" src="https://github.com/user-attachments/assets/a470e9f1-15d7-47e2-8fb9-21dfe157286b" />
<img width="399" alt="image" src="https://github.com/user-attachments/assets/97d393b4-4b7a-4ce3-ab73-ff072abb8144" />

### 7\. ສະຫຼຸບ

- ໂຄດນີ້ນີ້ຄວບຄຸມ RGB LEDs ດ້ວຍຄໍາສັ່ງຈາກ Serial Monitor ແລະໃຊ້ຟັງຊັນ Arduino ພື້ນຖານເພື່ອກໍານົດ pins, ເປີດແລະປິດ LEDs, ແລະສ້າງ loops ເພື່ອສະແດງສີທີ່ແຕກຕ່າງກັນ. ເຫມາະສົມສໍາລັບການຮຽນຮູ້ການຄວບຄຸມອຸປະກອນໄຟຟ້າທີ່ມີ Arduino ແລະຟັງຊັນການຂຽນໂປຣແກຣມພື້ນຖານ.

# ບົດທີ 4 Buzzer

#### ບົດລາຍງານຂອງ Buzzer Sound

- ຈຸດປະສົງ: ການສ້າງສຽງຈາກ Buzzer ດ້ວຍ Arduino.
  - ອຸປະກອນ: Arduino, Buzzer.
  - ໂຄດທີ່ໃຊ້: tone(pin, frequency, duration);

### 1\. ບົດນຳ

- ໂຄດນີ້ເປັນຕົວຢ່າງພື້ນຖານຂອງການນຳໃຊ້ Arduino ເພື່ອສ້າງສຽງຈາກບັດເຊີ (Buzzer).

### 2\. ອຸປະກອນທີ່ໃຊ້

- ບອດ Arduino (ເຊັ່ນ Arduino Uno, Arduino Mega ເປັນຕົ້ນ)
- ບັດຊະ (Buzzer)
- ສາຍ USB ສຳລັບເຊື່ອມຕໍ່ກັບຄອມພິວເຕີ

### 3\. ການອະທິບາຍໂຄດ

- ໂຄດນີ້ປະກອບໄປດ້ວຍສອງຟັງຊັນຫຼັກໄດ້ແກ່ setup() ແລະ loop()

### 3.1 ຟັງຊັນ setup()
```
# define SPEAKER 10

# define BTN 2

# define NOTE_C2 65

# define NOTE_D2 73

# define NOTE_E2 82

# define NOTE_F2 87

# define NOTE_G2 98

# define NOTE_A2 110

# define NOTE_B2 123

# define NOTE_C3 130

# define NOTE_D3 146

# define NOTE_E3 164

# define NOTE_F3 174

# define NOTE_G3 196

# define NOTE_A3 220

# define NOTE_B3 246

# define NOTE_C4 261

# define NOTE_D4 293

# define NOTE_E4 329

# define NOTE_F4 349

# define NOTE_G4 392

# define NOTE_A4 440

# define NOTE_B4 493

// Melody notes and durations

int melody\[\] = {

NOTE_C3, NOTE_F3, NOTE_G3, NOTE_A3,

NOTE_G3, NOTE_F3, NOTE_A3, NOTE_G3,

NOTE_A3, NOTE_B3, NOTE_C4, NOTE_A3,

NOTE_C4, NOTE_B3, NOTE_A3, NOTE_B3,

NOTE_C4, NOTE_B3, NOTE_A3, NOTE_G3,

NOTE_E3, NOTE_D3, NOTE_E3, NOTE_F3,

NOTE_G3, NOTE_E3, NOTE_C3, NOTE_D3,

NOTE_G2, NOTE_C3, NOTE_D3, NOTE_E3,

NOTE_F3, NOTE_G3, NOTE_F3, NOTE_A3,

NOTE_G3, NOTE_F3, NOTE_E3, NOTE_D3,

NOTE_C3, NOTE_D3, NOTE_E3, NOTE_F3,

NOTE_E3, NOTE_E3, NOTE_D3, NOTE_C3,

NOTE_D3, NOTE_E3, NOTE_G3, NOTE_E3,

NOTE_D3, NOTE_C3, NOTE_C4, NOTE_C4,

NOTE_A3, NOTE_G3, NOTE_A3, NOTE_C4,

NOTE_A3, NOTE_A3, NOTE_D4, NOTE_C4,

NOTE_A3, NOTE_G3, NOTE_E3, NOTE_G3,

NOTE_E3, NOTE_D3, NOTE_C3, NOTE_C3,

NOTE_C3, NOTE_C3, NOTE_C3, NOTE_D3,

NOTE_E3, NOTE_D3, NOTE_C3, NOTE_G3,

NOTE_G3, NOTE_G3, NOTE_G3, NOTE_E3,

NOTE_G3, NOTE_A3, NOTE_B3, NOTE_A3,

NOTE_G3, NOTE_E3, NOTE_A3, NOTE_G3,

NOTE_E3, NOTE_D3, NOTE_C3, NOTE_A2,

NOTE_G2, NOTE_A2, NOTE_C3

};

int noteDurations\[\] = {

2, 2, 4, 2,

2, 2, 4, 2,

2, 2, 4, 2,

2, 1, 2, 2,

2, 2, 2, 2,

4, 2, 2, 2,

2, 2, 2, 1,

2, 2, 3, 2,

2, 1, 2, 2,

2, 2, 2, 1,

2, 2, 2, 2,

2, 2, 3, 2,

2, 2, 2, 2,

2, 1, 2, 2,

2, 3, 3, 2,

2, 2, 2, 2,

2, 2, 2, 1,

3, 2, 2, 3,

3, 3, 2, 3,

2, 2, 2, 2,

2, 1, 2, 2,

2, 3, 3, 2,

2, 2, 2, 2,

2, 2, 2, 2,

2, 2, 1,

};

int btnState = 0;

void setup() {

Serial.begin(9600);

pinMode(SPEAKER, OUTPUT);

pinMode(LED_BUILTIN, OUTPUT);

pinMode(BTN, INPUT);

}
```
- ຟັງຊັນ setup() ຈະເຮັດວຽກພຽງຄັ້ງດຽວເມື່ອເລີ່ມຕົ້ນການຮຽນຮູ້ ແລະ ການໃຊ້ງານພາຍໃນບອດ

#### 3.2 ຟັງຊັນ loop()
```
void loop() {

btnState = digitalRead(BTN);

Serial.println(btnState);

if(btnState == HIGH){

delay(500);

digitalWrite(LED_BUILTIN, HIGH);

}

for (int i = 0; i < 200; i++) {

int noteDuration = 1000 / noteDurations\[i\]; // Note duration in milliseconds

tone(9, melody\[i\], noteDuration); // Play the note on pin 8

delay(noteDuration \* 1.3); // Pause between notes

noTone(8); // Stop the tone

}

delay(2000); // Pause before repeating the melody

}
```
- ໃຊ້ຄຳສັ່ງ tone() ເພື່ອເປີດສຽງຈາກບັດຊະທີ່ຄືນຄວາມຖີ່ຕ່າງໆ

#### 4\. ການເຮັດວຽກຂອງໂຄດ

ເມື່ອອັບໂຫລດໂຄດໃສ່ Arduino ແລະເລີ່ມຕົ້ນໃຊ້ງານ, ເພງຈະຫຼິ້ນຕາມເມໂລດີ້ທີ່ກຳນົດໄວ້.

### 5\. ຂໍ້ສັງເກດ

ຖ້າຕ້ອງການໃຫ້ມີການປ່ຽນຄວາມຍາວຂອງສຽງ, ສາມາດປ່ຽນຄ່າ delay() ได้.

### 6\. ຮູບວົງຈອນ
<img width="468" alt="image" src="https://github.com/user-attachments/assets/def6c22e-0ca4-4c52-993c-8408922e6c32" />

### 7\. ສະຫຼຸບ

- ໂຄດນີ້ເປັນຕົວຢ່າງພື້ນຖານຂອງການຄວບຄຸມ buzzer ເພື່ອຫຼິ້ນສຽງໂດຍໃຊ້ Arduino. ຮຽນຮູ້ວິທີໃຊ້ຟັງຊັນ Arduino ເຊັ່ນ: pinMode(), digitalWrite(), ແລະ tone() ເພື່ອສ້າງເພງທີ່ມ່ວນ ແລະເຂົ້າໃຈງ່າຍ.

# ບົດທີ 5 Potentiometer

#### ບົດລາຍງານຂອງ Potentiometer & LED Brightness

- ຈຸດປະສົງ: ປັບຄວາມສະຫວ່າງ LED ຕາມ potentiometer.
  - ອຸປະກອນ: Arduino, Potentiometer, LED.
  - ໂຄດທີ່ໃຊ້: analogRead(A0); ແລະ map(value, 0, 1023, 0, 255);

### 1\. ບົດນໍາ

ໂຄ້ດນີ້ເປັນຕົວຢ່າງການນໍາໃຊ້ Potentiometer (ຕົວຕ້ານທານປັບຄ່າໄດ້) ໃນການຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED ໂດຍໃຊ້ Arduino ແລະ ຟັງຊັນ analogRead() ແລະ analogWrite()

- Potentiometer ຈະໃຫ້ຄ່າໄຟຟ້າເປັນໄຟສັນຍານອະນາລັອກທີ່ປ່ຽນໄປໄດ້ລະຫວ່າງ 0V - 5V ແລະ Arduino ຈະປ່ຽນເປັນຄ່າດິຈິຕອນໃນຊ່ວງ 0 - 1023
- ຄ່ານີ້ຈະຖືກແປງໃຫ້ເປັນຄ່າຄວາມສະຫວ່າງຂອງ LED ໂດຍໃຊ້ map() ເພື່ອປ່ຽນໃຫ້ຄ່າຢູ່ໃນຊ່ວງ 0 - 255 ແລະສົ່ງໄປຄວບຄຸມ LED ຜ່ານ analogWrite()

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno ຫຼື ບອດທີ່ຮອງຮັບການອ່ານຄ່າອະນາລັອກ
2. Potentiometer (10kΩ) ຕໍ່ໃສ່ຂາ A0
3. LED ພ້ອມຕົວຕ້ານທານ 220Ω ຕໍ່ໃສ່ຂາ 11
4. ສາຍໄຟ ແລະ Breadboard

### 3\. ການອະທິບາຍໂຄ້ດ

#### 3.1 ກໍານົດຕົວແປເລີ່ມຕົ້ນ
```
int analogValue = 0; // ຄ່າທີ່ອ່ານໄດ້ຈາກ Potentiometer (0 - 1023)

int ledValue = 0; // ຄ່າທີ່ໃຊ້ໃນການປັບຄວາມສະຫວ່າງຂອງ LED (0 - 255)

- analogValue ຄືຄ່າທີ່ຖືກອ່ານຈາກ Potentiometer
- ledValue ຄືຄ່າທີ່ໃຊ້ເພື່ອປັບຄວາມສະຫວ່າງຂອງ LED
```
#### 3.2 ຟັງຊັນ setup()
```
void setup() {

Serial.begin(9600); // ເປີດ Serial Monitor ເພື່ອກວດສອບຄ່າ

pinMode(11, OUTPUT); // ກໍານົດຂາ 11 ໃຫ້ເປັນ OUTPUT ສໍາລັບ LED

}
```
- Serial.begin(9600); ເປີດ Serial Monitor ເພື່ອເບິ່ງຄ່າທີ່ອ່ານໄດ້
- pinMode(11, OUTPUT); ກໍານົດຂາ 11 ເປັນ OUTPUT ໃຫ້ LED

#### 3.3 ຟັງຊັນ loop()
```
void loop() {

analogValue = analogRead(A0); // ອ່ານຄ່າຈາກ Potentiometer

Serial.println(analogValue); // ສະແດງຄ່າທີ່ອ່ານໄດ້

- analogRead(A0); ອ່ານຄ່າຈາກ Potentiometer ລະຫວ່າງ 0 - 1023

ledValue = map(analogValue, 0, 1023, 0, 255); // ແປງຄ່າໃຫ້ຢູ່ໃນຊ່ວງ 0-255

Serial.println(ledValue); // ສະແດງຄ່າທີ່ແປງໄດ້

- ນໍາຄ່າທີ່ອ່ານໄດ້ໃຫ້ຂະຫຍາຍຂອບເຂດໄປຢູ່ໃນຊ່ວງ 0 - 255 ໃຫ້ເຂົ້າກັບ LED

analogWrite(11, ledValue); // ຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED

delay(10); // ໜ່ວງເວລາ 10ms ເພື່ອຫຼຸດຄວາມໄວໃນການອ່ານຄ່າ

}
```
- analogWrite(11, ledValue); ໃຊ້ PWM ເພື່ອຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED

### 4\. ການເຮັດວຽກຂອງໂຄ້ດ

- ເມື່ອໝູນ Potentiometer
  - ຖ້າໝູນສູງຂຶ້ນ LED ຈະສະຫວ່າງຂຶ້ນ,
  - ຖ້າໝູນລົງ LED ຈະຈາງລົງ.

### 5\. ການສັງເກດ

- ຈຸດທີ່ເຮັດວຽກຢ່າງຖືກຕ້ອງ

- ໃຊ້ analogRead() ເພື່ອອ່ານຄ່າຈາກ potentiometer ຢ່າງຖືກຕ້ອງ

- ໃຊ້ map() ເພື່ອປ່ຽນຄ່າຈາກໄລຍະ 0 - 1023 ຫາ 0 - 255 ຢ່າງຖືກຕ້ອງ

- ໃຊ້ analogWrite() ເພື່ອຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED ຕາມການອ່ານ

### 6\. ຮູບວົງຈອນ
<img width="468" alt="image" src="https://github.com/user-attachments/assets/32971e21-8417-4ca2-8602-347fddf700dd" />
<img width="291" alt="image" src="https://github.com/user-attachments/assets/73a2c5df-6dc0-48cf-8018-61efc3cfa2ed" />


### 7\. ສະຫຼຸບ

- ຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED ຕາມ Potentiometer ໄດ້ຖືກຕ້ອງ
- ປ່ຽນຄ່າຂອງ LED ໄດ້ອອກມາຄ້າຍຄືຄ່າທີ່ອ່ານໄດ້
- ໃຊ້ analogRead() ແລະ analogWrite() ຢ່າງຖືກຕ້ອງ

💡 ເຄັດລັບ: ຖ້າຕ້ອງການໃຫ້ LED ຄ່ອຍໆ ປ່ຽນຄວາມສະຫວ່າງໄດ້ນຸ່ມນວນຂື້ນ, ສາມາດໃຊ້ຄ່າສະເລ່ຍຂອງຄ່າທີ່ອ່ານໄດ້ໃນຫຼາຍໆຮອບກ່ອນສົ່ງໃຫ້ LED.

# ບົດທີ 6 Relay

### ບົດລາຍງານຂອງ Relay Control

- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການໃຊ້ Relay ກັບ Arduino.
  - ອຸປະກອນ: Arduino, Relay, LED.
  - ໂຄດທີ່ໃຊ້: digitalWrite(relayPin, HIGH/LOW);

### 1\. ບົດນໍາ

ໂຄ້ດນີ້ເປັນຕົວຢ່າງການຄວບຄຸມ Relay ຜ່ານ Arduino ໂດຍໃຊ້ digitalWrite() ໃນການເປີດ-ປິດ (ON/OFF) ຕົວ Relay.

- Relay ຄືອຸປະກອນທີ່ໃຊ້ໃນການຄວບຄຸມການເປີດ-ປິດອຸປະກອນໄຟຟ້າດ້ວຍ ສັນຍານດິຈິຕອນ
- ໃນໂຄດນີ້, ພວກເຮົາໃຊ້ LED ຂອງ Arduino (LED_BUILTIN) ສໍາລັບທົດສອບໂຄດ

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno
2. Relay Module 5V
3. LED (ຖ້າຕ້ອງການທົດສອບປິດ-ເປີດ Relay)
4. ສາຍໄຟ ແລະ Breadboard

### 3\. ການອະທິບາຍໂຄ້ດ

#### 3.1 ຟັງຊັນ setup()
```
void setup()

{

pinMode(LED_BUILTIN, OUTPUT); // ກໍານົດຂາ LED_BUILTIN ໃຫ້ເປັນ OUTPUT

}
```
- pinMode(LED_BUILTIN, OUTPUT); ຕັ້ງຄ່າຂາ LED ຂອງ Arduino ເປັນ OUTPUT
- ໃນການນໍາໃຊ້ຄວບຄຸມ Relay, ສາມາດປ່ຽນ LED_BUILTIN ເປັນຂາອື່ນເຊັ່ນ pinMode(7, OUTPUT) ຖ້າເຊື່ອມຕໍ່ Relay ທີ່ຂາ 7.

#### 3.2 ຟັງຊັນ loop()
```
void loop()

{

digitalWrite(LED_BUILTIN, HIGH); // ປ່ອນສັນຍານ HIGH (ເປີດ LED/Relay)

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

digitalWrite(LED_BUILTIN, LOW); // ປ່ອນສັນຍານ LOW (ປິດ LED/Relay)

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

}
```
- digitalWrite(LED_BUILTIN, HIGH);
  - ປ່ອນສັນຍານ HIGH (5V) ໃຫ້ LED/Relay
  - LED ຈະເປີດ (ເມື່ອໃຊ້ Relay ມັນຈະເປີດວົງຈອນໄຟຟ້າ)
- delay(1000); ລໍຖ້າ 1 ວິນາທີ
- digitalWrite(LED_BUILTIN, LOW);
  - ປ່ອນສັນຍານ LOW (0V)
  - LED ຈະປິດ (Relay ປິດວົງຈອນໄຟຟ້າ)
- delay(1000); ລໍຖ້າ 1 ວິນາທີ ກ່ອນທີ່ຈະເລີ່ມວົງຈອນຄືນ

### 4\. ຜົນທີ່ຄາດຫວັງ

- LED ຂອງ Arduino ຈະໄຟຕິດ-ດັບທຸກ 1 ວິນາທີ
- ໃນການເຊື່ອມຕໍ່ Relay, ມັນຈະເປີດ-ປິດ ຄວບຄຸມອຸປະກອນໄຟຟ້າໄດ້.

### 5\. ຮູບວົງຈອນ
<img width="468" alt="image" src="https://github.com/user-attachments/assets/a614ee30-fbf8-4c68-a376-bcf44c4c7753" />
<img width="315" alt="image" src="https://github.com/user-attachments/assets/03f211f0-780e-4da6-ab3b-a502ce2b1467" />

### 6\. ສະຫຼຸບ

- ໂຄດນີ້ເປັນສິ່ງພື້ນຖານສໍາລັບການຄວບຄຸມ Relay ໃນລະບົບ IoT ຫຼື Smart Home
- ສາມາດປັບແຕ່ງໄດ້ໂດຍປ່ຽນ PIN ແລະ delay ຕາມຄວາມຈໍາເປັນ
- ໃຊ້ Relay ເພື່ອຄວບຄຸມອຸປະກອນໄຟຟ້າໄດ້ໂດຍຜ່ານ Arduino

ເມື່ອຮຽນຮູ້ການຄວບຄຸມ Relay ຜ່ານ Arduino, ພວກເຮົາສາມາດນໍາໄປປະຍຸກຕ໌ໃນການຄວບຄຸມ Smart Home, ປະຕູອັດຕະໂນມັດ, ແລະລະບົບ IoT ໄດ້.

# ບົດທີ 7 Servo

#### ບົດລາຍງານຂອງ Servo Motor Control

- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການເຊື່ອມຕໍ່ ແລະ ຄວບຄຸມ Servo Motor.
  - ອຸປະກອນ: Arduino, Servo Motor, Potentiometer.
  - ໂຄດທີ່ໃຊ້: servo.write(angle).

### 1\. ບົດນໍາ

- ໂຄ້ດນີ້ໃຊ້ສໍາລັບຄວບຄຸມ Servo Motor ຜ່ານ Potentiometer ໂດຍ Arduino

 - Servo Motor ເປັນມໍເຕີທີ່ຄວບຄຸມມຸມຫັນໄດ້ແນ່ນອນ (0° - 180°)
 - Potentiometer ເປັນຕົວຕ້ານທານປັບຄ່າໄດ້ ໃຊ້ເພື່ອກຳນົດມຸມຂອງ Servo
 - Arduino ຈະອ່ານຄ່າ Potentiometer ແລ້ວໃຊ້ map() ໃນການປັບສັດສ່ວນເພື່ອຄວບຄຸມ Servo

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno
2. Servo Motor (SG90 ຫຼື MG995)
3. Potentiometer 10kΩ
4. ສາຍໄຟ ແລະ Breadboard

### 3\. ການເຊື່ອມຕໍ່ (Wiring Diagram)

| **Servo Motor** | **Arduino** |
| --- | --- |
| VCC (ແດງ) | 5V  |
| GND (ດໍາ) | GND |
| Signal (ເຫຼືອງ/ຂາວ) | 9   |

| **Potentiometer** | **Arduino** |
| --- | --- |
| Left Pin | 5V  |
| Middle Pin | A0  |
| Right Pin | GND |

### 4\. ອະທິບາຍໂຄດ

#### 4.1 ສ່ວນ setup()
```
#include <Servo.h>; // ນຳໃຊ້ໄລບຣາຣີ Servo

Servo myservo; // ສ້າງອອບເຈັກ Servo

int potpin = A0; // ຂາ Analog ທີ່ເຊື່ອມ Potentiometer

int val; // ຕົວປ່ຽນເກັບຄ່າຈາກ Potentiometer

void setup() {

Serial.begin(9600); // ສົ່ງຂໍ້ມູນຜ່ານ Serial Monitor

myservo.attach(9); // ເຊື່ອມ Servo ທີ່ຂາ 9

}
```
- #include <Servo.h> ໃຊ້ໄລບຣາຣີ Servo
- Servo myservo; ສ້າງອອບເຈັກ Servo
- potpin = A0; ກຳນົດ Potentiometer ໃຫ້ເຊື່ອມຂາ A0
- Serial.begin(9600); ເປີດ Serial Monitor
- myservo.attach(9); ເຊື່ອມ Servo ທີ່ຂາ 9

#### 4.2 ສ່ວນ loop()
```
void loop() {

val = analogRead(potpin); // ອ່ານຄ່າຈາກ Potentiometer (0 - 1023)

Serial.print("pot = ");

Serial.print(val);

Serial.print(", servo = ");

val = map(val, 0, 1023, 0, 180); // ປັບສັດສ່ວນໃຫ້ເປັນ 0 - 180°

Serial.println(val);

myservo.write(val); // ປັບມຸມ Servo

delay(15); // ລໍຖ້າໃຫ້ Servo ປັບມຸມສໍາເລັດ

}
```
- analogRead(potpin); ອ່ານຄ່າຈາກ Potentiometer (0-1023)
- map(val, 0, 1023, 0, 180); ແປງຄ່າ 0-1023 ເປັນ 0-180°
- myservo.write(val); ສັ່ງ Servo ໃຫ້ຫັນໄປມຸມທີ່ກໍານົດ
- delay(15); ລໍຖ້າກ່ອນທີ່ Servo ຈະຂັບເຄື່ອນ

### 5\. ຜົນທີ່ຄາດຫວັງ

- ເມື່ອໝູນ Potentiometer, Servo Motor ຈະໝູນຕາມ (0° - 180°)
- Serial Monitor ຈະສະແດງຄ່າເຊັ່ນ pot = 512, servo = 90
- ສາມາດນໍາໄປປະຍຸກໃນລະບົບຄວບຄຸມປະຕູອັດຕະໂນມັດ…

### 6\. ຮູບວົງຈອນ
<img width="468" alt="image" src="https://github.com/user-attachments/assets/6738eb81-4edd-4d16-85d3-b06e3b1e532b" />
<img width="294" alt="image" src="https://github.com/user-attachments/assets/8e7aa2fc-ee0a-4fee-a361-2e6c468b6296" />


### 7\. ສະຫລຸບ

- ໂຄດນີ້ ຈະຄວບຄຸມ Servo Motor ດ້ວຍ Potentiometer ໂດຍໃຊ້ Arduino

- Potentiometer ໃຊ້ສໍາລັບກຳນົດມຸມ (0° - 180°) ໃຫ້ Servo

- analogRead() ອ່ານຄ່າຈາກ Potentiometer (0 - 1023

- map() ປັບຄ່າ 0-1023 ເປັນ 0-180

- myservo.write() ຄວບຄຸມການໝູນຂອງ Servo

#### ຜົນລັບ: Servo Motor ຈະໝູນຕາມການປັບ Potentiometer

# ບົດທີ 8 7-Segment

#### ບົດລາຍງານຂອງ Seven Segment Display

- ຈຸດປະສົງ: ຄວາມເຂົ້າໃຈການສະແດງຂໍ້ມູນໃນ 7-Segment.
  - ອຸປະກອນ: Arduino, 7-Segment Display, Resistor.
  - ໂຄດທີ່ໃຊ້: digitalWrite(segmentPins\[i\], HIGH/LOW);

### 1\. ບົດນໍາ

####ໂຄ້ດນີ້ໃຊ້ສໍາລັບຄວບຄຸມ Seven Segment Display ດ້ວຍ Arduino ໃນການສະແດງຕົວເລກ 0 - 9 ທີ່ຈະປ່ຽນເລກໃນທຸກ 1 ວິນາທີ.

- Seven Segment Display 1 ໂຕ ແບບ Common Cathode
- Arduino ຈະສົ່ງສັນຍານໄຟຟ້າໃຫ້ເມື່ອເຮັດການສະແດງຕົວເລກ
- ການຄວບຄຸມ 7 segments (a-g) ໃຊ້ 7 GPIO pins

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno
2. Seven Segment Display (Common Cathode)
3. Resistors 220Ω _(ສໍາລັບຈຳກັດໄຟຟ້າເຂົ້າ LED ຂອງຈໍ)_
4. ສາຍໄຟ ແລະ Breadboard.

### 3\. ການເຊື່ອມຕໍ່ (Wiring Diagram)

| **Seven Segment Pin** | **Arduino Pin** |
| --- | --- |
| a   | 2   |
| b   | 3   |
| c   | 4   |
| d   | 5   |
| e   | 6   |
| f   | 7   |
| g   | 8   |
| Common Cathode (CC) | GND |

### 4\. ອະທິບາຍໂຄດ

#### 4.1 ກຳນົດ PIN ແລະ ຂໍ້ມູນຂອງຕົວເລກ
```
// ກຳນົດຂາຂອງ Seven Segment Display

int segmentPins\[\] = {2, 3, 4, 5, 6, 7, 8}; // ປັບຕາມການເຊື່ອມຂອງເຈົ້າ

// ສະແດງຕົວເລກ 0 - 9 ສໍາລັບຈໍ Common Cathode

byte digits\[\] = {

B11111100, // 0

B01100000, // 1

B11011010, // 2

B11110010, // 3

B01100110, // 4

B10110110, // 5

B10111110, // 6

B11100000, // 7

B11111110, // 8

B11110110 // 9

};
```
- segmentPins\[\] ກຳນົດຂາທີ່ໃຊ້ເຊື່ອມໄປ Seven Segment Display
- digits\[\] ແມ່ນຮູບແບບຂອງຕົວເລກ 0-9 ທີ່ເຮັດໃຫ້ LED ON/OFF

#### 4.2 ການກຳນົດຂາ output ຂອງ Arduino
```
void setup() {

// ຕັ້ງຄ່າໃຫ້ທຸກຂາເປັນ OUTPUT

for (int i = 0; i < 7; i++) {

pinMode(segmentPins\[i\], OUTPUT);

digitalWrite(segmentPins\[i\], LOW); // ປິດທຸກຂາຕອນເລີ່ມຕົ້ນ

}

}
```
- ເຮັດໃຫ້ທຸກຂາເປັນ OUTPUT
- ປິດ Seven Segment ຂອງທຸກສ່ວນໃນຕອນຄືນໄຟ

#### 4.3 ການສະແດງຕົວເລກ
```
void loop() {

// ສະແດງ 0 - 9

for (int i = 0; i <= 9; i++) {

displayDigit(i);

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

}

// ປິດຈໍ 1 ວິນາທີ

clearDisplay();

delay(1000);

// ສະແດງ 9 - 0

for (int i = 9; i >= 0; i--) {

displayDigit(i);

delay(1000); // ລໍຖ້າ 1 ວິນາທີ

}

// ປິດຈໍ 1 ວິນາທີ

clearDisplay();

delay(1000);

}
```
- ໃຫ້ຈໍ Seven Segment ເລີ່ມຈາກ 0-9
- ປິດຈໍ 1 ວິນາທີ
- ສະແດງຄືນ ເລກ 9-0
- ປິດຈໍ 1 ວິນາທີກ່ອນເລີ່ມໃໝ່

#### 4.4 ຄຳສັ່ງສະແດງຕົວເລກ
```
void displayDigit(int num) {

byte segments = digits\[num\];

for (int i = 0; i < 7; i++) {

digitalWrite(segmentPins\[i\], bitRead(segments, 7 - i) ? HIGH : LOW);

}

}
```
- bitRead(segments, 7 - i) ໃຊ້ໃນການເປີດ/ປິດ LED ຂອງ Seven Segment
- HIGH ເປີດ LED, LOW ປິດ LED

#### 4.5 ຄຳສັ່ງປິດຈໍ
```
void clearDisplay() {

for (int i = 0; i < 7; i++) {

digitalWrite(segmentPins\[i\], LOW); // ປິດທຸກເສັ້ນ LED

}

}
```
- ປິດທຸກຂາທີ່ເຊື່ອມກັບ Seven Segment Display

### 5\. ຜົນທີ່ຄາດຫວັງ

- ຈໍ Seven Segment ສະແດງຕົວເລກ 0-9 ແລ້ວປິດ 1 ວິນາທີ
- ສະແດງຄືນ ຕົວເລກ 9-0 ແລ້ວປິດ 1 ວິນາທີ
- ນຳໃຊ້ໃນ ໂປໂຣແກຣມນັບເວລາ, ນັບຈຳນວນ, ລະບົບຄວບຄຸມດ້ວຍຕົວເລກ

6\. ຮູບວົງຈອນ

<img width="468" alt="image" src="https://github.com/user-attachments/assets/3a36164a-a7ec-4814-81ae-ba62fb89ebe3" />

7\. ສະຫລຸບ

#### ໂຄ້ດນີ້ເຮັດການຄວບຄຸມ Seven Segment Display ເພື່ອສະແດງຕົວເລກ 0 ເຖິງ 9 ແລະ 9 ເຖິງ 0 ໃນ 1 ວິນາທີ.

- ຄວບຄຸມທຸກຂາຂອງ Display ຜ່ານ Arduino ແລະ 7 pins ໃນການສັບຕົວເລກ
- ເລກ 0–9 ຈະສະແດງໃນຄວາມໄວ 1 ວິນາທີ ແລະ ສະແດງຍ້ອນກັບຈາກ 9 ເຖິງ 0.

**ຄຳສັ່ງ:**

- displayDigit() ສະແດງຕົວເລກ
- clearDisplay() ປິດຈໍ

# Assignment RGB mix with button

### 1\. ບົດນໍາ

#### ໂຄງການນີ້ແມ່ນລະບົບຄວບຄຸມແສງສະຫວ່າງ Lifter Level RGB LED ໂດຍໃຊ້ປຸ່ມກົດເພື່ອປັບລະດັບຄວາມສະຫວ່າງຂອງແຕ່ລະສີ: ສີແດງ, ສີຂຽວແລະສີຟ້າ, ລະບົບໃຊ້ Pulse-Width Modulation (PWM) ເພື່ອປັບລະດັບຄວາມສະຫວ່າງຂອງ LEDs ແລະ ສະຫນອງສຽງເຕືອນຜ່ານ buzzer ເມື່ອກົດປຸ່ມ, ເຊິ່ງອະນຸຍາດໃຫ້ສ້າງການປະສົມສີຕ່າງໆ. ໂຄງການນີ້ແມ່ນເຫມາະສົມສໍາລັບການຮຽນຮູ້ການຄວບຄຸມການປ້ອນຂໍ້ມູນແລະຜົນຜະລິດຂອງ microcontroller ໄດ້. ເຊັ່ນດຽວກັນກັບການດໍາເນີນງານຂອງ PWM

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno
2.  LED x3
3.  Resistor 220Ω
4.  Buzzer x1
5.  Button x3
6.  ສາຍໄຟ ແລະ Breadboard

### 3\. ອະທິບາຍໂຄດ
```
const int buttonRed = 2; // Button for Red

const int buttonGreen = 3; // Button for Green

const int buttonBlue = 4; // Button for Blue

const int pwmLedRed = 11; // Red LED (PWM Pin)

const int pwmLedGreen = 9; // Green LED (PWM Pin)

const int pwmLedBlue = 10; // Blue LED (PWM Pin)

const int ledRed = 7; // Red LED (Non-PWM Pin)

const int ledGreen = 6; // Green LED (Non-PWM Pin)

const int ledBlue = 5; // Blue LED (Non-PWM Pin)

const int buzzer = 12;

// Brightness levels (0-255 for PWM)

int redBrightness = 0;

int greenBrightness = 0;

int blueBrightness = 0;

// Button state tracking

bool lastButtonRed = HIGH;

bool lastButtonGreen = HIGH;

bool lastButtonBlue = HIGH;

const int toneRed = 440; // Red Button Tone (A4)

const int toneGreen = 523; // Green Button Tone (C5)

const int toneBlue = 659; // Blue Button Tone (E5)

void setup() {

// Button input

pinMode(buttonRed, INPUT_PULLUP);

pinMode(buttonGreen, INPUT_PULLUP);

pinMode(buttonBlue, INPUT_PULLUP);

// LED output

pinMode(pwmLedRed, OUTPUT);

pinMode(pwmLedGreen, OUTPUT);

pinMode(pwmLedBlue, OUTPUT);

pinMode(ledRed, OUTPUT);

pinMode(ledGreen, OUTPUT);

pinMode(ledBlue, OUTPUT);

// Initialize LEDs to off

analogWrite(pwmLedRed, 0); // PWM Red off

analogWrite(pwmLedGreen, 0); // PWM Green off

analogWrite(pwmLedBlue, 0); // PWM Blue off

digitalWrite(ledRed, LOW); // Red off

digitalWrite(ledGreen, LOW); // Green off

digitalWrite(ledBlue, LOW); // Blue off

}

void loop() {

// Check Red Button

if (digitalRead(buttonRed) == LOW && lastButtonRed == HIGH) {

redBrightness = (redBrightness + 64) % 256; // Cycle through 0, 64, 128, 192, 255

analogWrite(pwmLedRed, redBrightness);

digitalWrite(ledRed, HIGH); // Turn on Red LED

//tone(buzzer, toneRed, 200); // Play Red Tone (200ms)

delay(200); // Debounce

} else if (digitalRead(buttonRed) == HIGH) {

digitalWrite(ledRed, LOW); // Turn off Red LED

}

lastButtonRed = digitalRead(buttonRed);

// Check Green Button

if (digitalRead(buttonGreen) == LOW && lastButtonGreen == HIGH) {

greenBrightness = (greenBrightness + 64) % 256;

analogWrite(pwmLedGreen, greenBrightness);

digitalWrite(ledGreen, HIGH); // Turn on Green LED

tone(buzzer, toneGreen, 200); // Play Green Tone (200ms)

delay(200); // Debounce

} else if (digitalRead(buttonGreen) == HIGH) {

digitalWrite(ledGreen, LOW); // Turn off Green LED

}

lastButtonGreen = digitalRead(buttonGreen);

// Check Blue Button

if (digitalRead(buttonBlue) == LOW && lastButtonBlue == HIGH) {

blueBrightness = (blueBrightness + 64) % 256;

analogWrite(pwmLedBlue, blueBrightness);

digitalWrite(ledBlue, HIGH); // Turn on Blue LED

tone(buzzer, toneBlue, 200); // Play Blue Tone (200ms)

delay(200); // Debounce

} else if (digitalRead(buttonBlue) == HIGH) {

digitalWrite(ledBlue, LOW); // Turn off Blue LED

}

lastButtonBlue = digitalRead(buttonBlue);

}
```
### 5\. ຮູບວົງຈອນ
<img width="468" alt="image" src="https://github.com/user-attachments/assets/b28bee6a-254c-4b72-900c-b5ac0b51c2cf" />

### 6\. ສະຫລຸບ

#### ໂຄງການນີ້ນໍາສະເຫນີການຄວບຄຸມຂອງໄຟ LED RGB ທີ່ສາມາດປັບລະດັບຄວາມສະຫວ່າງຂອງແຕ່ລະສີ. ໂດຍ​ການ​ນໍາ​ໃຊ້​ປຸ່ມ​ກົດ​ຮ່ວມ​ກັບ​ການ​ດໍາ​ເນີນ​ງານ PWM ແລະ​ເພີ່ມ​ລະ​ບົບ​ການ​ແຈ້ງ​ການ​ສຽງ​. ນີ້ສ້າງລະບົບການໂຕ້ຕອບທີ່ສາມາດສ້າງສີທີ່ແຕກຕ່າງກັນ. ຕາມ​ທີ່​ຕ້ອງ​ການ ໂຄງການນີ້ສາມາດຖືກນໍາໃຊ້ໃນການອອກແບບເຮັດໃຫ້ມີແສງ. ຫຼືລະບົບການຄວບຄຸມແສງສະຫວ່າງໃນຄໍາຮ້ອງສະຫມັກອື່ນໆ.

# Midterm Lifter Level

### 1\. ບົດນໍາ

#### ເເມ່ນລະບົບສໍາລັບປັບອົງສາ lifter ຂອງລົດຂົນດິນ ຕັ້ງເເຕ່ 0°-90° ໂດຍຄອບຄຸມຜ່ານ potentiometer ເເລ້ວສະເເດວຢູ່ 7 segment

### 2\. ອຸປະກອນທີ່ໃຊ້

1. Arduino Uno

2. Potentiometer

3. Servo

4. ສາຍໄຟ ແລະ Breadboard

### 3\. ໂຄດ
```
const potValue = A0;

const int A = 13;

const int B = 12;

const int C = 11;

const int D = 10;

const int E = 9;

const int F = 8;

const int G = 7;

const int H = 6;

void setup()

{

pinMode(A, OUTPUT);

pinMode(B, OUTPUT);

pinMode(C, OUTPUT);

pinMode(D, OUTPUT);

pinMode(E, OUTPUT);

pinMode(F, OUTPUT);

pinMode(G, OUTPUT);

pinMode(H, OUTPUT);

pinMode(BUZZER_PIN, OUTPUT);

}

void zero(void)

{

digitalWrite(A, LOW);

digitalWrite(B, LOW);

digitalWrite(C, LOW);

digitalWrite(D, LOW);

digitalWrite(E, LOW);

digitalWrite(F, LOW);

digitalWrite(G, LOW);

digitalWrite(H, LOW);

}

void one(void)

{

digitalWrite(A, LOW);

digitalWrite(B, LOW);

digitalWrite(C, LOW);

digitalWrite(D, HIGH);

digitalWrite(E, LOW);

digitalWrite(F, LOW);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void two(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, LOW);

digitalWrite(C, HIGH);

digitalWrite(D, HIGH);

digitalWrite(E, HIGH);

digitalWrite(F, HIGH);

digitalWrite(G, LOW);

digitalWrite(H, LOW);

}

void three(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, LOW);

digitalWrite(C, HIGH);

digitalWrite(D, HIGH);

digitalWrite(E, LOW);

digitalWrite(F, HIGH);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void four(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, HIGH);

digitalWrite(C, LOW);

digitalWrite(D, HIGH);

digitalWrite(E, LOW);

digitalWrite(F, LOW);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void five(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, HIGH);

digitalWrite(C, HIGH);

digitalWrite(D, LOW);

digitalWrite(E, LOW);

digitalWrite(F, HIGH);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void six(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, HIGH);

digitalWrite(C, HIGH);

digitalWrite(D, LOW);

digitalWrite(E, HIGH);

digitalWrite(F, HIGH);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void seven(void)

{

digitalWrite(A, LOW);

digitalWrite(B, LOW);

digitalWrite(C, HIGH);

digitalWrite(D, HIGH);

digitalWrite(E, LOW);

digitalWrite(F, LOW);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void eight(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, HIGH);

digitalWrite(C, HIGH);

digitalWrite(D, HIGH);

digitalWrite(E, HIGH);

digitalWrite(F, HIGH);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void nine(void)

{

digitalWrite(A, HIGH);

digitalWrite(B, HIGH);

digitalWrite(C, HIGH);

digitalWrite(D, HIGH);

digitalWrite(E, LOW);

digitalWrite(F, HIGH);

digitalWrite(G, HIGH);

digitalWrite(H, LOW);

}

void displayNumber(int value)

{

if (value == 0)

{

zero();

}

else if (value == 1)

{

one();

}

else if (value == 2)

{

two();

}

else if (value == 3)

{

three();

}

else if (value == 4)

{

four();

}

else if (value == 5)

{

five();

}

else if (value == 6)

{

six();

}

else if (value == 7)

{

seven();

}

else if (value == 8)

{

eight();

}

else if (value == 9)

{

nine();

}

}

void loop()

{

int displayValue = map(potValue, 0, 1023, 0, 9);

displayNumber(displayValue);

delay(50);

}
```
5\. ຮູບວົງຈອນ

<img width="271" alt="image" src="https://github.com/user-attachments/assets/1b46ce35-75f4-4c44-b638-afa0a4c6c1f9" />

All Source Link

<https://docs.google.com/spreadsheets/d/12mSJ2-Kfrz-K-JMLKxfk04L67xmCXRrQxpH3zJPbPO0/edit?usp=sharing>

<img width="245" alt="image" src="https://github.com/user-attachments/assets/5cc23ddd-a586-4488-a458-73d2b41ac235" />
