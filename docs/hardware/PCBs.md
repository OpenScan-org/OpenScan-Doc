# PCBs

## Pi Shield

The OpenScan Pi Shield can be used to control two independent stepper motors and a variety of different cameras (Pi Camera, various Arducams, DSLR - via GPhoto and external Cameras like Smartphone and others). The mechanism can be used in various forms (see for example OpenScan Mini + Classic and it could be easily adapted to be used as a camera slider or in other mechanisms.

![image](https://user-images.githubusercontent.com/57842400/181233777-a679768e-08b9-406b-9027-11ad7a09ff09.png)


### BOM

| Nr. | Picture | Count | Name |
| - | - | - | - |
| 1 | ![image](https://user-images.githubusercontent.com/57842400/181232345-e3ba03e4-4131-4e7d-a505-69cd9948e4a7.png) | 1x | Raspberry Pi Shield
|2 |![image](https://user-images.githubusercontent.com/57842400/181233128-fb792cf0-689e-410b-ade6-6d495498db20.png) |4x | Pin Header female, 8p, 2.54 |
|3 |![image](https://user-images.githubusercontent.com/57842400/181233187-0d979498-513d-489e-abc1-bcbca4f6503f.png) |1x |Pin Header female, 2p, 2.54 |
|4 |![image](https://user-images.githubusercontent.com/57842400/181233214-6d651a9e-7e07-42bb-96c7-d7927dcab969.png) |1x |Pin Header male, 3p, 2.54 |
|5 |![image](https://user-images.githubusercontent.com/57842400/181233236-95104096-3b04-4816-b43b-6a8693a4179e.png) |2x |Pin Header male, 4p, 2.54 |
|6 |![image](https://user-images.githubusercontent.com/57842400/181233254-b91bea8a-7f77-4b05-9eaf-b0461dfcd1d3.png) |1x |Pin Header female, 2x20p, 2.54 |
|7 |![image](https://user-images.githubusercontent.com/57842400/181233282-917e3a05-3125-48aa-8c89-b857469948f9.png) |1x | JST-XH-3P 90° |
|8 |![image](https://user-images.githubusercontent.com/57842400/181233293-5cc34136-8dae-4fa0-8371-d85864689ab2.png) |1x  | DCDC converter, 12V->5V, >2.5A |
|9 |![image](https://user-images.githubusercontent.com/57842400/181233315-7ebac355-ca41-4194-993f-59567603bee0.png) |2x | IRLZ34N |
|10 |![image](https://user-images.githubusercontent.com/57842400/181233339-20873acf-0240-4a1b-a6f5-bf5d60941132.png) |1x | Barrel Connector, 5.5-2.1mm |
|11 |![image](https://user-images.githubusercontent.com/57842400/181233366-bef85c9e-26a4-49f9-8d56-a5915ab4ba9d.png) |1x | Switch |
|12 |![image](https://user-images.githubusercontent.com/57842400/181233464-29f688ae-6a19-42ce-befa-e92e502883fc.png) |2x | Capacitor 100uF, 16V |
|13 |![image](https://user-images.githubusercontent.com/57842400/181233504-3fc4ae5e-32b6-4750-aa88-77acf6d37c32.png) |1x | Resistor 220 Ohm |
|14 |![image](https://user-images.githubusercontent.com/57842400/181233530-1df6dcf2-ea36-4b3c-ac07-ba3ddc086bc4.png) | 1x | Optocoupler PC817|


### Important remarks

#### DCDC converter

**FOLLOW THIS STEP CAREFULLY AS ANY ERROR CAN DESTROY THE RASPBERRY PI**

**The voltage regulator IS NOT set to 5V by default, which you will have to do as shown here:**

* solder the pin header (4) to the pi shield pcb
* check the back of the voltage regulator (8). The 5V solder pads (A) must be bridged. The connection at point (B) must be disconnected by scratching. This should set the converter to 5V
* Alternatively you can adjust the potentiometer on the front to set the correct output voltage of 5V. 

![image](https://user-images.githubusercontent.com/57842400/181231953-b7b89bba-bd65-4ae1-abc2-d71b3b937a57.png)


* When soldering the voltage regulator to the pin headers, make sure to have the right orientation and leave the uppermost hole free

![image](https://user-images.githubusercontent.com/57842400/181232069-adf541a2-9c41-4a13-8842-338f52982cb4.png)


#### Control the Voltage!!

**Before connecting any motors or the Raspberry Pi, you need to check if the voltage regulator is set to the right output of 5V. This can be done by connecting the PCB to 12V power supply through the barrel connector, switching (11.) to the lower position and checking the voltage between point (C) and (D), which must be 5.1V (±0.1V). If this is not the case, you have to use the potentiometer on the voltage regulator (8.) to change the output voltage accordingly.**


#### Capacitors

(12) make sure to orient the capacitors in the right way due to their polarity. The negative side is labeled both on the PCB and on the capacitor itself.

#### Optocoupler

(14) Make sure to orient the optocoupler correctly. There is a small dot in one of the corners, which should face the resistor. see the following closeup:

![image](https://user-images.githubusercontent.com/57842400/181231774-282af073-89bf-41d4-b494-9732231c90f0.png)

### Soldering

**PLEASE MAKE SURE TO CHECK OUT THE IMPORTANT REMARKS EARLIER**

Back:

![image](https://user-images.githubusercontent.com/57842400/181250607-cf94d9c8-04c8-41f1-ab25-912ff00ef82e.png)

Front:

![image](https://user-images.githubusercontent.com/57842400/181232248-42a45376-cdb9-4d61-a03c-289fd0c9a3ce.png)


## Ringlight v1

### BOM

| Nr. | Picture | Count | Name |
| - | - | - | - |
|1 |![image](https://user-images.githubusercontent.com/57842400/181234096-d83531fe-71d2-42a0-9b0c-7e51dad079fd.png) | 1x | Raspberry Pi Ringlight PCB |
|2 |![image](https://user-images.githubusercontent.com/57842400/181234123-69b1bc75-5c62-41eb-bad8-f0a22a96a46b.png) | 8x | LED 1W |
|3 | ![image](https://user-images.githubusercontent.com/57842400/181234149-8eddef58-8755-4e11-9798-4029cf8fde60.png) | 2x | Resistor 1Ohm |
|4 |![image](https://user-images.githubusercontent.com/57842400/181233282-917e3a05-3125-48aa-8c89-b857469948f9.png) |1x | JST-XH-3P 90° |

### Important remarks

#### LED orientation

Make sure that all LEDs are aligned correctly as shown in the following close-up. The hole on one side of the LED has to be facing the printed circle on the PCB.

![image](https://user-images.githubusercontent.com/57842400/181234449-2c3de7ec-2c2b-4201-8a84-0819bd179ffb.png)

### Soldering

![image](https://user-images.githubusercontent.com/57842400/181234329-ba1774f6-7169-4c99-a9ac-20b6e8927c0f.png)

You can test the circuit's functionality by applying 12V directly to the Ringlight PCB as shown in the following images:

![image](https://user-images.githubusercontent.com/57842400/181256232-6a5cbe1f-4d3c-4e08-982f-6841a3be668f.png)

   