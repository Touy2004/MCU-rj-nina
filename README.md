# ສາລະບານ

**ບົດນຳ** ..................................................................................................................................

**ບົດທີ 0** Blink .......................................................................................................................

**ບົດທີ 1** Experiment Blink ....................................................................................................

**ບົດທີ 2** Switch ....................................................................................................................

**ບົດທີ 3** RGB .......................................................................................................................

**ບົດທີ 4** Buzzer ...................................................................................................................

**ບົດທີ 5** Potentiometer ........................................................................................................

**ບົດທີ 6** Relay .....................................................................................................................

**ບົດທີ 7** Servo .....................................................................................................................

**ບົດທີ 8** Seven Segment .....................................................................................................

**ບົດທີ 9** Color Matching Sound Alarm System ...................................................................

**ບົດທີ 10** See Battery with LED and Seven Segment ………………………………………...............

# ບົດນຳ

ໄມໂຄຣໂປຣເຊສເຊີ ແລະ ໄມໂຄຄອມພີວເຕີ ເປັນອົງປະກອບທີ່ສຳຄັນໃນຄອມພິວເຕີສະໄໝໃໝ່. ລະບົບອັດຕະໂນມັດ ແລະລະບົບຝັງຕົວ. ໄມໂຄຣໂປຣເຊສເຊີ (microprocessor) ເຮັດຫນ້າທີ່ເປັນຫນ່ວຍປະມວນຜົນກາງ (CPU) ທີ່ປະຕິບັດຄໍາສັ່ງ ແລະ ຄວບຄຸມການເຮັດວຽກຕ່າງໆ. ໄມໂຄຄອມພີວເຕີ (microcomputer) ແມ່ນການປະສົມປະສານຂອງ microprocessor ກັບຫນ່ວຍຄວາມຈໍາ ແລະ ອຸປະກອນເສີມເພື່ອເຮັດໃຫ້ມັນປະຕິບັດຫນ້າວຽກສະເພາະໃດຫນຶ່ງປະສິດທິພາບ.

ບົດ​ລາຍ​ງານ​ນີ້​ໄດ້ສຳຫຼວດການ​ທົດ​ລອງ​ທີ່​ສໍາ​ຄັນ​ທີ່​ສະ​ແດງ​ໃຫ້​ເຫັນ​ເຖິງການ​ເຮັດວຽກ​ພື້ນ​ຖານ​ຂອງ microcontroller ໄດ້​. ລວມມີການຄວບຄຸມການປ້ອນຂໍ້ມູນ/ການສົ່ງອອກແບບດິຈິຕອນ. ການເຊື່ອມຕໍ່ເຊັນເຊີ ແລະ ການສື່ສານກັບອຸປະກອນຕ່າງໆ. ການທົດລອງເຫຼົ່ານີ້ນໍາສະເໜີການໃຊ້ງານຕົວຈິງທີ່ຊ່ວຍໃຫ້ເຂົ້າໃຈການເຮັດວຽກ ແລະ ການປະຍຸກໃຊ້ຂອງ microcontrollers ໃນສະຖານະການຈິງ.

ຫຼັງຈາກຜ່ານການທົດສອບເຫຼົ່ານີ້, ນັກສຶກສາຈະໄດ້ຮັບປະສົບການທາງດ້ານປະຕິບັດຕົວຈິງໃນການເຊື່ອມຕໍ່ໄມໂຄຣຄອນໂທຣອນເລີກັບອຸປະກອນຕ່າງໆ, ການນຳໃຊ້ເຊັນເຊີ ແລະ ການພັດທະນາໂປຣແກຣມ, ເຊິ່ງເປັນພື້ນຖານສຳຄັນໃນການອອກແບບ ແລະ ພັດທະນາລະບົບທີ່ຊັບຊ້ອນຂຶ້ນໃນອະນາຄົດ.

# ບົດທີ 0 Blink

### 1. **ບົດນຳ**

- ຈຸດປະສົງ:
  - ຮຽນຮູ້ທີ່ຈະຄວບຄຸມ LED ເປີດແລະປິດໂດຍໃຊ້ Arduino.
  - ເຂົ້າໃຈຫຼັກການການເຮັດວຽກຂອງຄໍາສັ່ງ digitalWrite() ແລະ delay()

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- LED ໃນຕົວ (ຢູ່ pin 13)

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- LED: ໃຊ້ໄຟ LED ໃນຕົວຢູ່ pin 13 ຂອງ Arduino.
- ການສະຫນອງພະລັງງານ: Arduino ສະຫນອງພະລັງງານໃຫ້ກັບວົງຈອນທັງຫມົດ.

### 4. **ໂຄດທີ່ໃຊ້**
```
// C++ code

void setup()
{

    // put your setup code here, to run once:

    pinMode(LED_BUILTIN, OUTPUT); // PIN 13
}

void loop()
{

    // put your main code here, to run repeatedly:

    digitalWrite(LED_BUILTIN, HIGH);

    delay(1000); // Wait for 1000 millisecond(s) = 1 second

    digitalWrite(LED_BUILTIN, LOW);

    delay(1000); // Wait for 1000 millisecond(s) = 1 second
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- ກຳນົດ PIN:
- Pin 13 ຖືກຕັ້ງເປັນ OUTPUT ເພື່ອຄວບຄຸມການເປີດ ແລະປິດ LED.
- ເປີດ/ປິດ LED:
- ໃຊ້ຄໍາສັ່ງ digitalWrite(13, HIGH) ເພື່ອເປີດໄຟ LED.
- ໃຊ້ຄໍາສັ່ງ digitalWrite(13, LOW) ເພື່ອປິດໄຟ LED.
- ໃຊ້ delay(1000) ເພື່ອລໍຖ້າ 1 ວິນາທີກ່ອນທີ່ຈະເປີດ ຫຼື ປິດ LED.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/1OA5NuSi3UV-lab-0-blink>

# ບົດທີ 1 Experiment Blink

### 1. **ບົດນຳ**

ການທົດລອງ "Blink" ເປັນການແນະນໍາເບື້ອງຕົ້ນກ່ຽວກັບການຂຽນໂປຣແກຣມ microcontroller. ໂດຍການຄວບຄຸມ output ດິຈິຕອລໂດຍການໃຊ້ LEDs, ການທົດລອງນີ້ເປັນພື້ນຖານສໍາລັບຄວາມເຂົ້າໃຈກ່ຽວກັບການຈັດການ pin GPIO.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- LED
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

LED ແມ່ນເຊື່ອມຕໍ່ກັບ pin output ໂດຍຜ່ານຕົວຕ້ານທານ. ດ້ວຍຂາລົບທີ່ເຊື່ອມຕໍ່ກັບ GND, Microcontroller Arduino ຈະປ່ຽນສະຖານະຂອງ output ເພື່ອເຮັດໃຫ້ໄຟ LED ກະພິບ.

### 4. **ໂຄດທີ່ໃຊ້**
```
// C++ code

void setup()
{

    // put your setup code here, to run once:

    pinMode(LED_BUILTIN, OUTPUT); // PIN 13
}

void loop()
{

    // put your main code here, to run repeatedly:

    digitalWrite(LED_BUILTIN, HIGH);

    delay(1000); // Wait for 1000 millisecond(s) = 1 second

    digitalWrite(LED_BUILTIN, LOW);

    delay(1000); // Wait for 1000 millisecond(s) = 1 second
}
```

### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Arduino ກຳນົກ pin LED ເປັນ output.
- ໂປຣແກຣມເຂົ້າໄປໃນ loop ຢ່າງຕໍ່ເນື່ອງ.
- ໄຟ LED ຖືກເປີດໂດຍຕັ້ງ pin output ເປັນ HIGH.
- Delay 1 ວິນາທີ.
- ໄຟ LED ຖືກປິດໂດຍການຕັ້ງ pin output ເປັນ LOW.
- Delay 1 ວິນາທີ.
- ຂະ​ບວນ​ການ​ນີ້​ແມ່ນເຮັດ​ຊ​້​ໍ​າ​ຢ່າງ​ບໍ່​ມີ​ກໍາ​ນົດ, ເຮັດໃຫ້ເກີດໄຟກະພິບ​.

### 6. **ແຫຼ່ງອ້າງອີງ** <https://www.tinkercad.com/things/kHyeIreJXGU-mouktavanh-vonglokham>

# ບົດທີ 2 Switch

### 1. **ບົດນຳ**

ການທົດລອງ "ສະວິດ" ສະແດງໃຫ້ເຫັນເຖິງການໃຊ້ສະວິດເພື່ອຄວບຄຸມຜົນເອົ້າພຸດເຊັ່ນ: LED ໂດຍໃຊ້ microcontroller. ນີ້ແມ່ນແນວຄວາມຄິດທີ່ສໍາຄັນໃນການຂຽນໂປຣແກຣມ ເນື່ອງຈາກວ່າມັນສະແດງໃຫ້ເຫັນວິທີການອ່ານສະຖານະຂອງ input ທາງກາຍະພາບ ແລະ ຕອບສະຫນອງຕາມຄວາມເຫມາະສົມ.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Pushbutton (Switch)
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ປຸ່ມກົດແມ່ນເຊື່ອມຕໍ່ກັບ pin 2 (ການປ້ອນຂໍ້ມູນດິຈິຕອນ) ຂອງ Arduino.
- ຂາຫນຶ່ງຂອງປຸ່ມກົດແມ່ນເຊື່ອມຕໍ່ກັບ GND ແລະ ຂາອື່ນແມ່ນເຊື່ອມຕໍ່ກັບ pin 2.
- LED ແມ່ນເຊື່ອມຕໍ່ກັບ pin LED ໃນຕົວ (ຫຼື pin ດິຈິຕອນອື່ນ) ຜ່ານຕົວຕ້ານທານ. ຂາລົບແມ່ນເຊື່ອມຕໍ່ກັບ GND.

### 4. **ໂຄດທີ່ໃຊ້**

```
int buttonState = 0;

void setup()

{

    pinMode(2, INPUT);

    pinMode(LED_BUILTIN, OUTPUT);

    Serial.begin(9600);
}

void loop()

{

    // read the state of the pushbutton value

    buttonState = digitalRead(2);

    // check if pushbutton is pressed. if it is, the

    // buttonState is HIGH

    if (buttonState == HIGH)
    {

        // turn LED on

        Serial.println("Button HIGH");

        digitalWrite(LED_BUILTIN, HIGH);
    }
    else
    {

        // turn LED off

        Serial.println("Button LOW");

        digitalWrite(LED_BUILTIN, LOW);
    }

    delay(10); // Delay a little bit to improve simulation performance
}
```

### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Arduino ເລີ່ມຕົ້ນ pin 2 ເປັນ input ສໍາລັບປຸ່ມກົດ ແລະ pin LED ໃນຕົວເປັນ output.
- ໂປຣແກຣມເຂົ້າສູ່ loop ແລະ ຕິດຕາມສະຖານະຂອງປຸ່ມກົດຢ່າງຕໍ່ເນື່ອງ.
- ຖ້າປຸ່ມກົດ (buttonState ແມ່ນສູງ), LED ໃນຕົວຈະເປີດ.
- ຖ້າປຸ່ມບໍ່ໄດ້ກົດ (buttonState ຕໍ່າ), LED ຈະປິດ.
- ຂະບວນການນີ້ເຮັດຊ້ຳຢ່າງຕໍ່ເນື່ອງ, ຕອບສະໜອງຕາມສະຖານະຂອງປຸ່ມກົດ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/1eFpRFe7adp-lab-2-switch->

# ບົດທີ 3 RGB

### 1. **ບົດນຳ**

ໃນບົດນີ້, ພວກເຮົາຈະສຶກສາກ່ຽວກັບການຄວບຄຸມ RGB LED ໂດຍໃຊ້ Arduino. LED RGB ປະກອບດ້ວຍ LED 3 ຕົວ (ສີແດງ, ສີຂຽວ ແລະ ສີຟ້າ) ເຊິ່ງສາມາດປະສົມກັນເພື່ອສ້າງສີທີ່ແຕກຕ່າງກັນໂດຍການປັບຄວາມສະຫວ່າງຂອງແຕ່ລະສີ. ເຊິ່ງບົດນີ້ຈະສະແດງໃຫ້ຮູ້ເຖິງວິທີການຄວບຄຸມ RGB LED ໂດຍໃຊ້ຄໍາສັ່ງຈາກ Serial Input ເພື່ອເປີດ ຫຼື ປິດສີຕ່າງໆ ຫຼື ປະສົມສີເຫຼົ່ານີ້ເພື່ອສະແດງສີທີ່ແຕກຕ່າງ.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- RGB LED (ประเภท Common Cathode หรือ Common Anode)
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

RGB LED ມີ 4 pins ຄື: pin ສໍາລັບແຕ່ລະສີ (ສີແດງ, ສີຂຽວ, ສີຟ້າ) ແລະ pin ສໍາລັບດິນ (ສໍາລັບ Common Cathode) ຫຼື VCC (ສໍາລັບ Common Anode), ແຕ່ລະສີແມ່ນເຊື່ອມຕໍ່ກັບ pin ດິຈິຕອລຂອງ Arduino ໂດຍໃຊ້ຕົວຕ້ານທານໃນວົງຈອນນີ້:

- Pin 9: ສີແດງ
- Pin 10: ສີຂຽວ
- Pin 11: ສີຟ້າ
- Cathode ທົ່ວໄປ: ເຊື່ອມຕໍ່ກັບ GND

### 4. **ໂຄດທີ່ໃຊ້**

```
int ledPins\[\] = {11, 10, 9};

void setup()
{

    // put your setup code here, to run once:

    Serial.begin(9600);

    for (int i = 0; i < 3; i++)
    {

        pinMode(ledPins\[i\], OUTPUT);
    }

    // exercise

    // change foreach to for loop
}

void loop()
{

    // put your main code here, to run repeatedly:

    while (Serial.available() > 0)
    {

        // read input from serial monitor

        String input = Serial.readStringUntil('\\n'); // Read until newline

        for (int i = 0; i < 3; i++)
        {

            digitalWrite(ledPins\[i\], LOW);
        }

        delay(10);

        if (input == "on" or input == "rgb" or input == "rbg" or input == "grb" or input == "gbr" or input == "brg" or input == "bgr")
        {

            // turn all LEDs on

            for (int i = 0; i < 3; i++)
            {

                digitalWrite(ledPins\[i\], HIGH);
            }
        }

        else if (input == "off")
        {

            // turn all LEDs off

            for (int i = 0; i < 3; i++)
            {

                digitalWrite(ledPins\[i\], LOW);
            }
        }

        else if (input == "r")
        {

            digitalWrite(ledPins\[0\], HIGH);
        }

        else if (input == "g")
        {

            digitalWrite(ledPins\[1\], HIGH);
        }

        else if (input == "b")
        {

            digitalWrite(ledPins\[2\], HIGH);
        }

        else if (input == "rg" or input == "gr")
        {

            digitalWrite(ledPins\[0\], HIGH);

            digitalWrite(ledPins\[1\], HIGH);
        }

        else if (input == "rb" or input == "br")
        {

            digitalWrite(ledPins\[0\], HIGH);

            digitalWrite(ledPins\[2\], HIGH);
        }

        else if (input == "gb" or input == "bg")
        {

            digitalWrite(ledPins\[1\], HIGH);

            digitalWrite(ledPins\[2\], HIGH);
        }

        else
        {

            allColors();
        }
    }
}

void allColors()
{

    // WHITE

    for (int i = 0; i < 3; i++)
    {

        digitalWrite(ledPins\[i\], HIGH);
    }

    delay(100);

    for (int i = 0; i < 3; i++)
    {

        digitalWrite(ledPins\[i\], LOW);
    }

    delay(100);

    // RED, GREEN, BLUE

    for (int i = 0; i < 3; i++)
    {

        digitalWrite(ledPins\[i\], HIGH);

        delay(100);

        digitalWrite(ledPins\[i\], LOW);

        delay(100);
    }

    // RED + GREEN index 0 and index 1

    for (int i = 0; i < 2; i++)
    {

        digitalWrite(ledPins\[i\], HIGH);
    }

    delay(100);

    for (int i = 0; i < 2; i++)
    {

        digitalWrite(ledPins\[i\], LOW);
    }

    delay(100);

    // RED BLUE index 0 and index 2

    for (int i = 0; i < 3; i += 2)
    {

        digitalWrite(ledPins\[i\], HIGH);
    }

    delay(100);

    for (int i = 0; i < 3; i += 2)
    {

        digitalWrite(ledPins\[i\], LOW);
    }

    delay(100);

    // GREEN + BLUE index 1 and index 2

    for (int i = 1; i < 3; i++)
    {

        digitalWrite(ledPins\[i\], HIGH);
    }

    delay(100);

    for (int i = 1; i < 3; i++)
    {

        digitalWrite(ledPins\[i\], LOW);
    }

    delay(100);
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Serial Input: ລະບົບລໍຖ້າການປ້ອນຂໍ້ມູນຈາກ Serial ເຊັ່ນ "on", "off" ຫຼື ຄໍາສັ່ງແຕ່ລະສີເຊັ່ນ "r", "g", "b".
- ການຄວບຄຸມ LED: ຂຶ້ນກັບຄໍາສັ່ງປ້ອນຂໍ້ມູນ, ລະບົບຈະເປີດ ຫຼື ປິດ LED ທີ່ສອດຄ້ອງກັນເຊັ່ນ: ເມື່ອຄໍາສັ່ງແມ່ນ "r", LED ສີແດງຈະເປີດ.
- ການປະສົມສີ: ລະບົບສາມາດປະສົມສີໂດຍການເປີດໄຟ LED ຫຼາຍອັນໃນເວລາດຽວກັນ, ຕົວຢ່າງ "rg" ຈະເປີດສີແດງ ແລະ ສີຂຽວ ເຊິ່ງຈະເປັນສີເຫຼືອງ
- ເອັບເຟັກສີທັງໝົດ: ຟັງຊັ່ນ allColors() ໝູນວຽນຜ່ານສີຕ່າງໆເຊັ່ນ: ສີຂາວ, ສີແດງ, ສີຂຽວ, ສີຟ້າ, ແລະ ການປະສົມຂອງສີເຫຼົ່ານີ້ເພື່ອການສະແດງຜົນແບບຄົບວົງຈອນ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/kVTnRe9RDUO-lab-3-rgb-or-led-with-serial>

# ບົດທີ 4 Buzzer

### 1. **ບົດນຳ**

ໃນນີ້, ພວກເຮົາຈະໃຊ້ buzzer (ຫຼື ລໍາໂພງ) ເພື່ອສ້າງສຽງທີ່ແຕກຕ່າງກັນໂດຍອີງໃສ່ໂນດດົນຕີ. ພວກເຮົາຈະໃຊ້ຄໍາສັ່ງ tone () ເພື່ອສ້າງສຽງໂດຍອີງໃສ່ຄວາມຖີ່ທີ່ກໍານົດໄວ້.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Buzzer
- Jumper wires
- Breadboard (ຖ້າຕ້ອງການ)

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ເຊື່ອມຕໍ່ pin buzzer ກັບ pin 9 ຂອງ Arduino.
- ເຊື່ອມຕໍ່ຂາອື່ນຂອງ buzzer ກັບ GND.

### 4. **ໂຄດທີ່ໃຊ້**
```
// Notes frequencies (in Hz) for different pitches

#define SPEAKER 10

#define BTN 2

#define NOTE_C2 65

#define NOTE_D2 73

#define NOTE_E2 82

#define NOTE_F2 87

#define NOTE_G2 98

#define NOTE_A2 110

#define NOTE_B2 123

#define NOTE_C3 130

#define NOTE_D3 146

#define NOTE_E3 164

#define NOTE_F3 174

#define NOTE_G3 196

#define NOTE_A3 220

#define NOTE_B3 246

#define NOTE_C4 261

#define NOTE_D4 293

#define NOTE_E4 329

#define NOTE_F4 349

#define NOTE_G4 392

#define NOTE_A4 440

#define NOTE_B4 493

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

void setup()
{

    Serial.begin(9600);

    pinMode(SPEAKER, OUTPUT);

    pinMode(LED_BUILTIN, OUTPUT);

    pinMode(BTN, INPUT);
}

void loop()
{

    btnState = digitalRead(BTN);

    Serial.println(btnState);

    if (btnState == HIGH)
    {

        delay(500);

        digitalWrite(LED_BUILTIN, HIGH);
    }

    for (int i = 0; i < 200; i++)
    {

        int noteDuration = 1000 / noteDurations\[i\]; // Note duration in milliseconds

        tone(9, melody\[i\], noteDuration); // Play the note on pin 8

        delay(noteDuration \* 1.3); // Pause between notes

        noTone(8); // Stop the tone
    }

    delay(2000); // Pause before repeating the melody
}
```

### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- ການຫຼິ້ນ Melody: ໃຊ້ຟັງຊັນ tone() ເພື່ອຫຼິ້ນໂນດທີ່ແຕກຕ່າງກັນຜ່ານ buzzer ທີ່ເຊື່ອມຕໍ່ກັບ pin 9 ຂອງ Arduino, ຄວາມຖີ່ຂອງໂນດແມ່ນຖືກກໍານົດຕາມພາລາມິເຕີທີ່ລະບຸ ແລະ ຄວາມຍາວຂອງໂນດແມ່ນຄວບຄຸມໂດຍຜ່ານ array noteDurations\[\].
- ການຢຸດສຽງ: ຟັງຊັນ noTone() ຖືກນໍາໃຊ້ເພື່ອຢຸດສຽງເມື່ອໂນດໄດ້ສໍາເລັດການຫຼິ້ນ ແລະ ຈະມີ(delay()) ເພື່ອໃຫ້ທຸກໆໂນດມີເວລາຢຸດທີ່ເຫມາະສົມ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/lXYQiqLB7aJ-lab-4-active-buzzer>

# ບົດທີ 5 Potentiometer

### 1. **ບົດນຳ**

Potentiometer ຫຼື ຕົວປັບແຮງດັນແມ່ນຕົວຕ້ານທານທີ່ສາມາດປັບໄດ້, ສາມາດເຊື່ອມໂຍງກັບຄ່າຕ່າງໆເຊັ່ນ: ການຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED ຫຼື ຄວາມໄວຂອງມໍເຕີ, ຂຶ້ນຢູ່ກັບການປັບຂອງຜູ້ໃຊ້. ການທົດລອງນີ້ຈະແນະນໍາວິທີການອ່ານຈາກອະນາລັອກ ແລະ ວິທີການໃຊ້ງານ ເພື່ອຄວບຄຸມການດໍາເນີນງານໃນແອັບພິເຄຊັ່ນຕ່າງໆ.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Potentiometer
- LED
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ເຊື່ອມຕໍ່ potentiometer ກັບ Arduino ດັ່ງຕໍ່ໄປນີ້:
- ຂາ potentiometer ຊ້າຍໄປຫາ 5V ໃນ Arduino.
- ຂາ potentiometer ຂວາໄປຫາ GND.
- pin ກາງ (wiper) ຂອງ potentiometer ແມ່ນເຊື່ອມຕໍ່ກັບ Analog A0 pin ຂອງ Arduino.
- ເຊື່ອມຕໍ່ LED ກັບ pin 11 ໃນ Arduino.
- ຂາຍາວ (Anode pin) ຂອງ LED ໄປກັບ pin 11.
- ຂາສັ້ນ (ຂາ Cathode) ຂອງ LED ໂດຍຜ່ານ 220Ω resistor ຕໍ່ກັບ GND.

### 4. **ໂຄດທີ່ໃຊ້**
```
int analogValue = 0;

int ledValue = 0;

void setup()
{

    Serial.begin(9600);

    pinMode(11, OUTPUT);
}

void loop()
{

    analogValue = analogRead(A0);

    Serial.println(analogValue);

    ledValue = map(analogValue, 0, 1023, 0, 255);

    Serial.println(ledValue);

    analogWrite(11, ledValue);

    delay(10);

    Serial.print("Potentiometer: ");

    Serial.println(map(1023, 0, 1023, 0, 255)); // 255

    Serial.print("LED: ");

    Serial.println(map(255, 0, 255, 0, 1023)); // 1023
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- potentiometer ແມ່ນເຊື່ອມຕໍ່ກັບ pin A0 ຂອງ Arduino ແລະ LED ແມ່ນເຊື່ອມຕໍ່ກັບ pin 11.
- ການອ່ານຄ່າຈາກ potentiometer: ຟັງຊັນ analogRead(A0) ອ່ານຄ່າຈາກ potentiometer ເຊິ່ງຈະໄດ້ຮັບຄ່າລະຫວ່າງ 0 ຫາ 1023
- ການແປງຄ່າ Potentiometer ຈະຖືກປ່ຽນຈາກຊ່ວງ 0-1023 ເປັນ 0-255 ໂດຍໃຊ້ຟັງຊັນ map().
- ການຄວບຄຸມຄວາມສະຫວ່າງຂອງ LED: ຟັງຊັນ analogWrite(11, ledValue) ຈະປັບຄວາມສະຫວ່າງຂອງ LED ໂດຍອີງໃສ່ຄ່າທີ່ປ່ຽນໄດ້.
- ຈໍສະແດງຜົນ Serial: ຄ່າ Potentiometer ແລະ ຄວາມສະຫວ່າງ LED ຖືກສະແດງຢູ່ໃນ Serial Monitor.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/d72uq8bFCdH-lab-5-potentiometer-volume>

# ບົດທີ 6 Relay

1. **ບົດນຳ**

ຣີເລ (Relay) ແມ່ນອຸປະກອນທີ່ໃຊ້ເພື່ອຄວບຄຸມວົງຈອນໄຟຟ້າແຮງດັນສູງດ້ວຍສັນຍານຄວບຄຸມແຮງດັນຕໍ່າຈາກ Arduino ເຊິ່ງເຮັດໃຫ້ພວກເຮົາສາມາດເປີດ-ປິດອຸປະກອນໄຟຟ້າພາຍນອກເຊັ່ນ: ດອກໄຟ, ມໍເຕີ, ຫຼື ອຸປະກອນທີ່ໃຊ້ໄຟຟ້າໃນຄົວເຮືອນ.

ໃນບົດນີ້, ພວກເຮົາຈະໃຊ້ relay 5V ເພື່ອຄວບຄຸມການເປີດ-ປິດຂອງ LED ໂດຍໃຊ້ Arduino.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Relay Module
- LED
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ເຊື່ອມຕໍ່ Relay ກັບ Arduino.
- IN PIN (ສັນຍານຄວບຄຸມ) ຂອງ Relay → LED_BUILTIN pin (pin 13) ຂອງ Arduino.
- GND pin ຂອງ relay → GND ຂອງ Arduino
- VCC pin ຂອງ relay → 5V ຂອງ Arduino
- ເຊື່ອມຕໍ່ LED ກັບ relay ໄດ້.
- COM (ທົ່ວໄປ) pin ຂອງ relay →ເຊື່ອມຕໍ່ກັບ pole ບວກຂອງ LED ໄດ້.
- NO (ເປີດປົກກະຕິ) pin of relay → ເຊື່ອມຕໍ່ກັບ 5V ຂອງ Arduino.
- ຂົ້ວລົບຂອງ LED → 220Ω resistor → GND ຂອງ Arduino.

### 4. **ໂຄດທີ່ໃຊ້**

```

// C++ code

void setup()

{

    pinMode(LED_BUILTIN, OUTPUT);
}

void loop()

{

    digitalWrite(LED_BUILTIN, HIGH);

    delay(1000); // Wait for 1000 millisecond(s)

    digitalWrite(LED_BUILTIN, LOW);

    delay(1000); // Wait for 1000 millisecond(s)
}
```

### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Arduino ຄວບຄຸມ relay: ເມື່ອສັນຍານ HIGH ຖືກສົ່ງໄປຫາ LED_BUILTIN (pin 13), relay ຈະປິດວົງຈອນ (ເປີດ LED).
- Delay 1 ວິນາທີ: Arduino ຈະລໍຖ້າ 1 ວິນາທີກ່ອນທີ່ຈະປ່ຽນສະຖານະ.
- ປ່ຽນສະຖານະ: Arduino ປ່ຽນສັນຍານເປັນ LOW, ເຊິ່ງເຮັດໃຫ້ Relay ເປີດວົງຈອນ (ປິດໄຟ LED).
- ເຮັດຊ້ຳ: ລະບົບເປີດ ແລະ ປິດໄຟ LED ທຸກ 1 ວິນາທີ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/c0SurfXM1nl-lab-6-relay-with-12v>

# ບົດທີ 7 Servo

### 1. **ບົດນຳ**

ມໍເຕີເຊີໂວ (Servo Motor) ແມ່ນມໍເຕີທີ່ສາມາດ rotate ກັບຕໍາແຫນ່ງທີ່ຊັດເຈນ. ມັນຖືກນໍາໃຊ້ທົ່ວໄປໃນຫຸ່ນຍົນ ຫຼື ລະບົບການຄວບຄຸມອັດຕະໂນມັດ. ບົດນີ້ແມ່ນກ່ຽວກັບວິທີການຄວບຄຸມ servo motor ໂດຍໃຊ້ Potentiometer

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Servo motor
- Potentiometer
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ເຊື່ອມຕໍ່ຂາ VCC ຂອງ servo ກັບ 5V ໃນ Arduino.
- ເຊື່ອມຕໍ່ GND pin ຂອງ servo ກັບ GND ຂອງ Arduino.
- ເຊື່ອມຕໍ່ສາຍສັນຍານຂອງ servo ກັບ pin 9 ຂອງ Arduino.
- ເຊື່ອມຕໍ່ pin 1 ຂອງ potentiometer ກັບ 5V ໃນ Arduino.
- ເຊື່ອມຕໍ່ pin 2 (ກາງ) ຂອງ Potentiometer ກັບ A0 ຂອງ Arduino.
- ເຊື່ອມຕໍ່ pin 3 ຂອງ Potentiometer ກັບ GND ຂອງ Arduino.

### 4. **ໂຄດທີ່ໃຊ້**

```
#include <Servo.h>;

Servo myservo; // create servo object to control a servo

int potpin = A0; // analog pin used to connect the potentiometer

int val; // variable to read the value from the analog pin

void setup()
{

    Serial.begin(9600);

    myservo.attach(9); // attaches the servo on pin 9 to the servo object
}

void loop()
{

    val = analogRead(potpin); // reads the value of the potentiometer (value between 0 and 1023)

    Serial.print("pot = ");

    Serial.print(val);

    Serial.print(", servo = ");

    val = map(val, 0, 1023, 0, 180); // scale it to use it with the servo (value between 0 and 180)

    Serial.println(val);

    myservo.write(val); // sets the servo position according to the scaled value

    delay(15); // waits for the servo to get there
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Arduino ອ່ານຄ່າຈາກ potentiometer ທີ່ມີລະດັບ 0-1023.
- ໃຊ້ຟັງຊັນ map(val, 0, 1023, 0, 180); ແປງຄ່າເປັນມຸມ 0-180 ອົງສາ.
- ໃຊ້ myservo.write(val); ເພື່ອສັ່ງໃຫ້ servo motor ໝຸນໄປກັບມຸມທີ່ຕ້ອງການ
- ຄ່າມຸມແມ່ນສະແດງຢູ່ໃນ Serial Monitor.
- ໃນເວລາທີ່ໝຸນ potentiometer ເຫັນໄດ້ວ່າ servo motor ໝຸນຕາມມຄ່າທີ່ໄດ້ຮັບ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/ggDfNy4C7iI-lab7-sweep-and-knob-servo-motor->

# ບົດທີ 8 Seven Segment

### 1. **ບົດນຳ**

7-Segment Display ເປັນອຸປະກອນສະແດງຜົນທີ່ໃຊ້ກັນຢ່າງກວ້າງຂວາງເຊັ່ນ: ໃນເຄື່ອງຄິດເລກ ຫຼື ໂມງດິຈິຕອນ ເຊິ່ງກ່ຽວກັບການນຳໃຊ້ 7-Segment Display ແບບ1 ຫຼັກດ້ວຍ Arduino ເພື່ອສະແດງຕົວເລກ 0-9.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- 7-Segment Display LED
- Resistor (220Ω)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

ຈໍສະແດງຜົນ 7-Segment ມີ 7 pins (a-g) ເພື່ອສະແດງຕົວເລກ ແລະ common cathode (CC) ຫຼື common anode (CA) pin ເພື່ອກໍານົດປະເພດຂອງການດໍາເນີນງານ.

- ເຊື່ອມຕໍ່ pins a-g ຂອງ 7-Segment ກັບ Arduino pins:

a → 2, b → 3, c → 4, d → 5, e → 6, f → 7, g → 8

- ເຊື່ອມຕໍ່ cathode ທົ່ວໄປ (CC) ຫຼື anode ທົ່ວໄປ (CA) pin ກັບ GND ຫຼື 5V ຕາມປະເພດຂອງ 7-Segment.
- ໃຊ້ຕົວຕ້ານທານ 220Ω ເປັນຊຸດກັບແຕ່ລະ pin a-g ເພື່ອຫຼຸດຜ່ອນກະແສໄຟຟ້າ.

### 4. **ໂຄດທີ່ໃຊ້**

```
// Define the pins for each segment of the display

int segmentPins\[\] = {2, 3, 4, 5, 6, 7, 8}; // Adjust based on your wiring

// Digits representation for common cathode display

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

void setup()
{

    // Set all segment pins as OUTPUT

    for (int i = 0; i < 7; i++)
    {

        pinMode(segmentPins\[i\], OUTPUT);

        digitalWrite(segmentPins\[i\], LOW); // Turn off all segments initially
    }
}

void loop()
{

    // Display numbers 0 to 9

    for (int i = 0; i <= 9; i++)
    { // Start from 0

        displayDigit(i);

        delay(1000); // Wait for 1 second
    }

    // Turn off the display for 1 second

    clearDisplay();

    delay(1000);

    // Display numbers 9 to 0

    for (int i = 9; i >= 0; i--)
    { // Go down to 0

        displayDigit(i);

        delay(1000); // Wait for 1 second
    }

    // Turn off the display for 1 second

    clearDisplay();

    delay(1000);
}

void displayDigit(int num)
{

    byte segments = digits\[num\];

    for (int i = 0; i < 7; i++)
    {

        digitalWrite(segmentPins\[i\], bitRead(segments, 7 - i) ? HIGH : LOW); // Update each segment
    }
}

void clearDisplay()
{

    for (int i = 0; i < 7; i++)
    {

        digitalWrite(segmentPins\[i\], LOW); // Turn off all segments
    }
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- Arduino ສົ່ງສັນຍານໄປຫາ 7-Segment Display ຜ່ານ pins ທີ່ກໍານົດໄວ້.
- ໃຊ້ອາເຣ digits\[\] ເພື່ອກໍານົດລໍາດັບທີ່ LED ແຕ່ລະອັນຈະເປີດແລະປິດເພື່ອສະແດງຕົວເລກທີ່ຖືກຕ້ອງ.
- ໃນວົງ()
- ສະແດງຕົວເລກ 0-9, ແຕ່ລະຕົວເລກໃຊ້ເວລາ 1 ວິນາທີ.
- ປິດໄຟທັງໝົດເປັນເວລາ 1 ວິນາທີ.
- ສະແດງຕົວເລກ 9-0 ໂດຍແຕ່ລະຕົວເລກໃຊ້ເວລາ 1 ວິນາທີ.
- ປິດໄຟທັງໝົດເປັນເວລາ 1 ວິນາທີ.
- ໃຊ້ຟັງຊັນ displayDigit(int num) ເພື່ອສະຫຼັບແຕ່ລະ 7-Segment ເປີດ/ປິດ.
- ໃຊ້ຟັງຊັນ clearDisplay() ເພື່ອລ້າງຈໍສະແດງຜົນ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/jlZg5vfRxFs-lab-7segment>

# ບົດທີ 9 Color Matching Sound Alarm System

### 1. **ບົດນຳ**

Color Matching Sound Alarm System ເປັນລະບົບເຕືອນໄພທີ່ໃຊ້ RGB LEDs ແລະ Buzzer ເພື່ອຊີ້ບອກສະຖານະການເຕືອນໄພຕ່າງໆ ໂດຍອີງ​ຕາມ​ລະ​ດັບ​ຄວາມ​ຮຸນ​ແຮງ​ ມັນປ່ຽນສີຂອງໄຟ LED RGB ແລະ ສຽງຕາມຈໍານວນທີ່ກົດປຸ່ມ.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Push Button
- LED RGB
- Resistor (220Ω)
- Buzzer
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

| **ອຸປະກອນ** | **ຂາຂອງ Arduino** | **ໝາຍເຫດ** |
| --- | --- | --- |
| ປຸ່ມກົດ | 7   | ໃຊ້ INPUT_PULLUP ເພື່ອຫຼຸດສຽງລົບກວນ. |
| RGB LED - Red Pin (R) | 3   | ໃຊ້ PWM ສໍາລັບການຄວບຄຸມສີ. |
| RGB LED - ສີຂຽວ pin (G) | 4   | ໃຊ້ PWM ສໍາລັບການຄວບຄຸມສີ. |
| RGB LED - Blue Pin (B) | 5   | ໃຊ້ PWM ສໍາລັບການຄວບຄຸມສີ. |
| Buzzer | 6   | ຖືກນໍາໃຊ້ສໍາລັບເປັນສຽງເຕືອນ. |
| LED | 2   | ສະຖານະ LED ຖືກນໍາໃຊ້ສໍາລັບການກະພິບແຈ້ງເຕືອນໃນແຕ່ລະລະດັບ. |

### 4. **ໂຄດທີ່ໃຊ້**
```
#define BUTTON_PIN 7

#define RED_PIN 3

#define GREEN_PIN 4

#define BLUE_PIN 5

#define BUZZER_PIN 6

#define LED_PIN 2

int buttonState = 0;

int lastButtonState = 1;

int pressCount = 0;

int currentAlertLevel = 0;

unsigned long lastPressTime = 0;

unsigned long lastBlinkTime = 0;

const unsigned long pressTimeout = 1000; // 1 second for rapid presses

unsigned long blinkInterval = 500; // Default for green state

unsigned long beepDuration = 200;

unsigned long beepInterval = 300;

bool ledState = false; // Keep track of the LED state

void setup()
{

    pinMode(BUTTON_PIN, INPUT_PULLUP); // Internal pull-up resistor

    pinMode(RED_PIN, OUTPUT);

    pinMode(GREEN_PIN, OUTPUT);

    pinMode(BLUE_PIN, OUTPUT);

    pinMode(BUZZER_PIN, OUTPUT);

    pinMode(LED_PIN, OUTPUT);

    setRGBColor(0, 255, 0); // Start in Green state (Normal)
}

void loop()
{

    unsigned long currentTime = millis();

    buttonState = digitalRead(BUTTON_PIN);

    // Detect button press (LOW means pressed)

    if (buttonState == LOW && lastButtonState == HIGH)
    {

        pressCount++; // Increment press count

        lastPressTime = currentTime; // Reset the timeout timer

        delay(50); // Debounce delay
    }

    lastButtonState = buttonState;

    // If time since last press exceeds pressTimeout, update the state

    if (currentTime - lastPressTime > pressTimeout)
    {

        updateAlertLevel();

        pressCount = 0; // Reset press count after handling
    }

    // Handle blinking LED and buzzer non-blocking

    if (currentTime - lastBlinkTime >= blinkInterval)
    {

        ledState = !ledState; // Toggle LED state

        digitalWrite(LED_PIN, ledState);

        if (ledState)
        {

            tone(BUZZER_PIN, 1000, beepDuration); // Beep during LED ON
        }

        lastBlinkTime = currentTime;
    }
}

// Function to update the alert level and set appropriate colors, intervals, etc.

void updateAlertLevel()
{

    if (pressCount == 1)
    {

        currentAlertLevel = 0; // Green (Normal state)

        setRGBColor(0, 255, 0); // Green color

        blinkInterval = 500; // Slow blink

        beepDuration = 200; // Long beep

        beepInterval = 300; // Longer gap
    }
    else if (pressCount == 2)
    {

        currentAlertLevel = 1; // Blue (Warning state)

        setRGBColor(255, 255, 255); // Blue color

        blinkInterval = 250; // Medium blink

        beepDuration = 100; // Medium beep

        beepInterval = 150; // Shorter gap
    }
    else if (pressCount >= 3)
    {

        currentAlertLevel = 2; // Red (Danger state)

        setRGBColor(255, 0, 0); // Red color

        blinkInterval = 100; // Fast blink

        beepDuration = 50; // Quick beep

        beepInterval = 100; // Rapid gap
    }
}

// Function to set RGB color using PWM

void setRGBColor(int red, int green, int blue)
{

    analogWrite(RED_PIN, red);

    analogWrite(GREEN_PIN, green);

    analogWrite(BLUE_PIN, blue);
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- ຄ່າເລີ່ມຕົ້ນເປັນໂໝດປົກກະຕິ (ສີຂຽວ, ໄຟກະພິບຊ້າ, ສຽງຍາວ)
- ກົດປຸ່ມ 1 ເທື່ອ → ສະຖານະປົກກະຕິ (ສີຂຽວ, ກະພິບຊ້າ, ສຽງຍາວ)
- ກົດປຸ່ມ 2 ເທື່ອ → ໂໝດເຕືອນ (ສີຟ້າ, ກະພິບປານກາງ, ສຽງດັງແຮງຂຶ້ນ)
- ກົດປຸ່ມ 3 ເທື່ອ ຫຼືຫຼາຍກວ່ານັ້ນ → ໂໝດອັນຕະລາຍ (ສີແດງ, ກະພິບໄວ, ສຽງດັງໄວ ແລະ ຖີ່)
- ທຸກໂໝດປ່ຽນສີໄຟ LED ແລະສຽງ buzzer ຕາມລະດັບການແຈ້ງເຕືອນ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/f6CRznSWixS-midterm-1>

# ບົດທີ 10 See Battery with LED and Seven Segment

### 1. **ບົດນຳ**

ລະບົບນີ້ສະແດງລະດັບແບັດເຕີຣີໂດຍໃຊ້ LED ແລະ 7-segment display ໂດຍອີງໃສ່ການອ່ານຈາກ potentiometer. Potentiometer ໃຊ້ເພື່ອຈຳລອງຄ່າລະດັບແບັດເຕີຣີ ເຊິ່ງສະແດງໃນຮູບແບບຕົວເລກໃນຫນ້າຈໍ 7-segment ແລະ ຄວບຄຸມໄຟ LED ຕາມລະດັບທີ່ກໍານົດໄວ້.

### 2. **ອູປະກອນ**

- Microcontroller (Arduino)
- Potentiometer
- LED 3 colors (Red, Yellow, Green)
- Resistor (220Ω)
- 7-sagment (common cathode)
- Jumper wires
- Breadboard

### 3. **ການເຊື່ອມຕໍ່ວົງຈອນ**

- ການເຊື່ອມຕໍ່ potentiometer:
- ເຊື່ອມຕໍ່ pin VCC ຂອງ potentiometer ກັບ 5V.
- ເຊື່ອມຕໍ່ pin GND ຂອງ potentiometer ກັບ GND.
- ເຊື່ອມຕໍ່ pin ກາງຂອງ potentiometer (Wiper) ກັບ A0 (pin analog).
- ການເຊື່ອມຕໍ່ 7-segment display:
- ເຊື່ອມຕໍ່ pins a, b, c, d, e, f, g ຂອງ 7-segment display ກັບ pins 2-8 ຂອງ Arduino.
- pins ເຫຼົ່ານີ້ຄວບຄຸມການສະແດງຕົວເລກຈາກ 0-9.
- ການເຊື່ອມຕໍ່ LED:
- ເຊື່ອມຕໍ່ LED ສີແດງກັບ pin 10 ຂອງ Arduino, ຂາ Anode ຕໍ່ກັບ pin ແລະ pin Cathode ກັບ GND ຜ່ານຕົວຕ້ານທານ.
- ເຮັດເຊັ່ນດຽວກັນສໍາລັບ LED ສີເຫຼືອງ ແລະ ສີຂຽວ ຢູ່ pins 11 ແລະ 12.
- ການ​ເຊື່ອມ​ຕໍ່​ວົງ​ຈອນ​ໄຟ​ຟ້າ​:
- ເຊື່ອມຕໍ່ GND ຂອງ Arduino ກັບ GND ຂອງທຸກພາກສ່ວນ.
- ໃຫ້ແນ່ໃຈວ່າການສະຫນອງພະລັງງານຂອງ Arduino ແມ່ນເຊື່ອມຕໍ່ກັບ 5V.

### 4. **ໂຄດທີ່ໃຊ້**

```
// Pin definitions

const int potPin = A0; // Potentiometer pin

const int ledRed = 10; // Red LED

const int ledYellow = 11; // Yellow LED

const int ledGreen = 12; // Green LED

const int segPins\[\] = {2, 3, 4, 5, 6, 7, 8}; // 7-segment pins: a, b, c, d, e, f, g

// 7-segment patterns for numbers 0–9 (common cathode)

const bool digits\[10\]\[7\] = {

    {1, 1, 1, 1, 1, 1, 0}, // 0

    {0, 1, 1, 0, 0, 0, 0}, // 1

    {1, 1, 0, 1, 1, 0, 1}, // 2

    {1, 1, 1, 1, 0, 0, 1}, // 3

    {0, 1, 1, 0, 0, 1, 1}, // 4

    {1, 0, 1, 1, 0, 1, 1}, // 5

    {1, 0, 1, 1, 1, 1, 1}, // 6

    {1, 1, 1, 0, 0, 0, 0}, // 7

    {1, 1, 1, 1, 1, 1, 1}, // 8

    {1, 1, 1, 0, 0, 1, 1} // 9

};

void setup()
{

    // Initialize 7-segment pins

    for (int i = 0; i < 7; i++)
    {

        pinMode(segPins\[i\], OUTPUT);
    }

    // Initialize LED pins

    pinMode(ledRed, OUTPUT);

    pinMode(ledYellow, OUTPUT);

    pinMode(ledGreen, OUTPUT);

    // Start serial communication (optional for debugging)

    Serial.begin(9600);
}

void loop()
{

    // Read the potentiometer value

    int potValue = analogRead(potPin);

    // Map the potentiometer value to 0–9

    int digit = map(potValue, 0, 1023, 0, 9);

    // Display the digit on the 7-segment display

    displayDigit(digit);

    // Control LEDs based on the digit range

    controlLEDs(digit);

    // Debugging info (optional)

    Serial.print("Potentiometer Value: ");

    Serial.print(potValue);

    Serial.print(" | Digit: ");

    Serial.println(digit);

    delay(100); // Small delay to stabilize
}

// Function to display a digit on the 7-segment display

void displayDigit(int digit)
{

    for (int i = 0; i < 7; i++)
    {

        digitalWrite(segPins\[i\], digits\[digit\]\[i\]);
    }
}

// Function to control LEDs based on the digit range

void controlLEDs(int digit)
{

    if (digit >= 0 && digit <= 3)
    {

        digitalWrite(ledRed, HIGH);

        digitalWrite(ledYellow, LOW);

        digitalWrite(ledGreen, LOW);
    }
    else if (digit >= 4 && digit <= 6)
    {

        digitalWrite(ledRed, LOW);

        digitalWrite(ledYellow, HIGH);

        digitalWrite(ledGreen, LOW);
    }
    else if (digit >= 7 && digit <= 9)
    {

        digitalWrite(ledRed, LOW);

        digitalWrite(ledYellow, LOW);

        digitalWrite(ledGreen, HIGH);
    }
}
```
### 5. **ການເຮັດວຽກຂອງວົງຈອນ**

- ການອ່ານຄ່າແຮງດັນໄຟ
- potentiometer ແມ່ນໃຊ້ເພື່ອຈໍາລອງແຮງດັນທີ່ປ່ຽນແປງ.
- Arduino ອ່ານການປ້ອນຂໍ້ມູນແບບອະນາລັອກ (0-1023) ຈາກ potentiometer.
- ການແປງຄ່າແຮງດັນເປັນລະດັບພະລັງງານ
- ການອ່ານຈາກ potentiometer ແມ່ນຈະຖືກ map ເປັນຄ່າລະຫວ່າງ 0-9.
- ຄ່າເຫຼົ່ານີ້ຖືກສະແດງຢູ່ບົນໜ້າຈໍ 7-segment.
- ຕົວຊີ້ບອກສະຖານະດ້ວຍ LED
- ຄ່າພະລັງງານແບ່ງອອກເປັນ 3 ລະດັບຄື:
- 0-3 (ພະລັງງານຕໍ່າ): LED ສີແດງເປີດ.
- 4-6 (ພະລັງງານປານກາງ): LED ສີເຫຼືອງເປີດ
- 7-9 (ພະລັງງານສູງ): LED ສີຂຽວເປີດ.

### 6. **ແຫຼ່ງອ້າງອີງ:** <https://www.tinkercad.com/things/1xraBZea3Rn-midterm-2>
