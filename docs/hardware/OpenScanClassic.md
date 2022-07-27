# OpenScan Classic

![OpenScan_small](https://user-images.githubusercontent.com/57842400/181187888-aaf0680c-ba92-4a80-8608-773bb966e791.jpg)


## Overview
The OpenScan Classic is a compact desktop 3D scanner capable of scanning objects up to ~16 cm with an accuracy of up to 0.02 mm. The frame can be fully 3d printed, and all other components are off-the-shelf parts. You should be able to source all parts locally, or chose to support the OpenScan project by ordering (some) parts through [Openscan.eu/shop](https://www.openscan.eu/shop). Currently, the following cameras can be used without any additional modifications: Arducam IMX519 16mp & autofocus, Pi Camera v2 8mp and Pi Camera v1.3 5mp, where the Arducam IMX519 has to be considered the gold standard (for now :). Alternatively, you can even use many DSLR cameras, which can be connected and controlled through the Raspberry Pis USB interface...

### Bill of material (BOM)

* x M3x8 Screws
* x M3x12 Screws
* x M3 Nuts
* 1x Pi Shield
* 1x Nema 17 (>40Ncm)
* 1x Nema 17 (>13Ncm)
* 1x Raspberry Pi 3B+ or 4 (any)
* 1x Micro SD Card (>16GB)
* 1x Camera Ribbon Cable 15cm
* 1x Ringlight
* 1x Camera Module IMX519 (alternatively Pi Camera V2 or V1.3) or DSLR camera
* 2x M2x6 Nylon Screw
* 2x M2x6 Nylon Standoff
* 2x M2 Nuts
* (2x M2x12 Nylon Screw if you use the Pi Camera module)

3d printed parts:

TODO

### 3D Printing
Get the printable .stl (and design) files
TODO

## Assembly

### Control module

**IMPORTANT:**

**Skip this step until "prepare control module" if you intend to use external cameras only**

**Make sure to follow the right setup for your camera module (either Arducam IMX519 or PiCamera V1.3/V2)**

#### Arducam IMX519 16mp with Autofocus

* 1x Ringlight PCB
* 1x Arducam IMX519 16mp camera module 
* 2x M2x6 screws
* 2x M2x6 standoffs
* 2x M2 nuts

See the sequence of the parts: 

![image](https://user-images.githubusercontent.com/57842400/174085376-bd4337ea-9719-4759-b4ed-e29f14d615cb.png)

**Make sure that the lens is properly centered (looking at the ringlight from the front as shown in the right image):**

![arducam](https://user-images.githubusercontent.com/57842400/174086556-5910f154-6780-4acd-94b1-73ce9ca5a6db.jpg)

#### Pi Camera v2.1 or v1.3

* 1x Ringlight PCB
* Pi Camera v2.1 or v1.3 module 
* 2x M2x12 screws
* 2x spacer
* 2x M2 nuts

See the sequence of the parts: 

![image](https://user-images.githubusercontent.com/57842400/174087838-dd806e6d-5823-4748-9241-7bf04aed1ba9.png)

![picamera](https://user-images.githubusercontent.com/57842400/174087769-922aa8e4-7e88-4b05-b342-0912f542a6b9.jpg)

#### Prepare control module

Control Module:
![cm1](https://user-images.githubusercontent.com/57842400/174266033-a81330d0-3ee6-4003-9ea8-c61052450e82.jpg)

Use 8x M3x8 screws to mount the ringlight module and the Pi Shield in the following way:
![cm2](https://user-images.githubusercontent.com/57842400/174266045-947d8560-28cf-4865-a757-6b2b86a89879.jpg)

Connect the ringlight module and the pi shield with the 50cm ringlight cable, connect the motor cables:
![cm3](https://user-images.githubusercontent.com/57842400/174266161-1997a631-11e5-42b6-9b2c-18bf01383317.jpg)

Use the 15cm camera ribbon cable to connect the Raspberry Pi and the camera. Make sure that the ribbon cables side with the metal pins is facing away from the USB ports of the Raspberry Pi.:
![cm3a](https://user-images.githubusercontent.com/57842400/174270185-d77f9e4e-0d06-4ced-bae6-abc95f301ba8.jpg)

Make sure to properly align the Raspberry Pi with the Pin headers on the Pi Shield. **Misalignment might destroy both the Raspberry Pi and the Pi Shield!**:
![cm5](https://user-images.githubusercontent.com/57842400/174270550-4c2011cf-f341-496f-865f-2ff76aa30541.jpg)

Your control module is ready to use and should look something like:
![cm6](https://user-images.githubusercontent.com/57842400/174271651-d889a7b1-677b-444f-bfb7-48d45ed78e58.jpg)

### Main Frame

#### Attach large motor

* Stand1_Nema_17.stl
* Nema 17 (min. 40Ncm)
* M3x8mm (4x)
* Gear_Small.stl (optional v2)

![image](https://user-images.githubusercontent.com/57842400/181202507-cae2e998-d7ed-4bb8-9f3c-16ea4642943f.png)

(left) Mount the stepper motor with four M3x8mm Screws onto the Stand1.stl.

(right) Press the Gear_small.stl onto the motor shaft. Make sure, that the gear and the motor shaft close flush at the front.

Note:
Depending on the printing accuracy, it may be necessary to pre-drill the screw holes with a 3mm drill bit. Furthermore the gear and the motor shaft might have a tight fit and you might have to „gently“ use the help of a hammer.

#### Mount reduction gears

* Stand1_Nema_17.stl (after Step 4a)
* Adapter2.stl
* Steel pin (d=6mm, l>50mm)


![image](https://user-images.githubusercontent.com/57842400/181202744-10dec522-1042-4600-b343-9ea3c8b347ef.png)


(left) The steel pin is pressed into the opening of the side stand. You can use a cordless screwdriver to "drill" the pin into the opening.

(middle) The larger gear (Adapter2.stl) is pressed onto the steel pin.

(right) The steel pin (top) and the motor shaft must NOT protrude forward from the components and should be flush with the surface. Superglue can be used to fix the position of the gears.

Note:
Both gears should match well and rotate relatively resistance free. If this is not the case, it may be necessary to replace the small gear with v2.stl or adjust the printer settings.

#### Prepare Stand2

* Stand2.stl
* Adapter1.stl
* Steel pin (d=6mm, l>50mm)

![image](https://user-images.githubusercontent.com/57842400/181203949-a291a473-3180-4bcb-9613-bbc84c4d8577.png)

(left) The steel pin is pressed into the opening of the side stand. You can use a cordless screwdriver to "drill" the pin into the opening.

(right) The adapter1.stl is pressed onto the steel pin. It is important to ensure that the steel pin does not protrude forward from the adapter.

Note:
The adapter can be fixed with superglue on the steel pin. It must be ensured that the steel pin can rotate freely in the stand.


#### Prepare Turntable

* Turntable_Base_small.stl
* Nema 17 (min. 13Ncm, optional >40Ncm)
* M3x8mm (4x)
* Rotary_Arm.stl (2x)
* Turntable_Adapter.stl

Mount the Nema 17 on Turntable_Base_small.stl using four M3x8mm screws:

![image](https://user-images.githubusercontent.com/57842400/181204799-a38e3a1c-03bd-402e-98c4-51a42f213664.png)

Place the Rotary Arm (2x) on the sides of the turntable_base.stl (red mark) and press any Turntable_Adapter.stl onto the motor shaft:

![image](https://user-images.githubusercontent.com/57842400/181205607-c81b59c5-b085-475d-b68d-e7ea59c50f27.png)

The connections marked red can be fixed with super glue if they are too loose.

#### Tilting mechanism

* Stand 1 (after step 4b)
* Stand 2 (after step 5)
* Turntable_Base_small.stl (after step 6) 
* M3x12mm (2x)

Combine all prepared parts as shown:

![image](https://user-images.githubusercontent.com/57842400/181206244-b244ba78-ec34-4169-a735-40c2ea7ae0ee.png)

The height of the turntable has to be adapted for each scan object.

Optimal height:

![image](https://user-images.githubusercontent.com/57842400/181207044-4aa298ae-cb0f-4b3f-b90d-eaff63bee580.png)

Object to high (left) and to low (right):

![image](https://user-images.githubusercontent.com/57842400/181207572-851b99a7-1af4-41a5-9d0d-cc2f0734763c.png)


Insert two M3x12mm screws laterally into the adapters (red mark), so as to connect the side stands with the rotating arm (Turntable_Base + Rotary_Arm). 

![image](https://user-images.githubusercontent.com/57842400/181208074-b26cfd5a-3c26-458f-a899-d67816f3caf9.png)

#### Wiring the motors

* Control unit (after step 3)
* Tilting mechanism (after step 7/8)
* Stepper motor cable >70cm (2x)

Connect the motors to the control unit:

![image](https://user-images.githubusercontent.com/57842400/181208526-c78a2d4e-7a00-46c4-9a7b-8d41a6b91524.png)


## Whole Setup

### PiCamera/Arducam

TODO add image of the whole setup

### External Camera (via USB)

TODO add image of the whole setup

You can directly connect a camera via USB and use the OpenScan web interface to preview and capture photos automatically. . The functionality is based on the great GPhoto2 Library (see [gphoto.org](http://www.gphoto.org/)) and the number of supported cameras is huge.

NOTE: some cameras need to be set to a different operating mode (PTP mode).

See this [list on gphoto.org](http://www.gphoto.org/proj/libgphoto2/support.php) to check whether your camera is supported. It is necassary that *Image Capture* and *Liveview* are listed.

### External Camera (via Opto)

TODO add image of the whole setup

#### Remote shutter release (I)

For (almost) all cameras you can buy a relatively cheap remote shutter release. These modules can be modified easily and also connected to the Scanner’s main control unit. 

A very extensive source for various camera models and home-made remote shutter release can be found on [doc-diy.net](http://www.doc-diy.net/photo/remote_pinout/). 

An existing remote release can be modified with minimal soldering skill and a total of two soldering points. The following pictures describe the basic procedure:

![image](https://user-images.githubusercontent.com/57842400/181215924-e244af9a-15bc-41ba-b9c1-3d08d013c432.png)

* (left) Infrared Remote Control for Nikon/Canon (ca. 5€)
* (middle) Open the enclosure. See the contact area (red circle)
* (right) The *green circle* shows the contacts that are normally connected by pressing the button (first image). The holes marked by the *red circles* can be used to connect two cables, that can later be connected to the scanner’s control module.

The difficult part is to solder two male jumper wires to the identified contact points (*red circles*). 

![image](https://user-images.githubusercontent.com/57842400/181216688-b8baecdb-1d77-457c-90ad-a2615e7021a4.png)

Shortening those two wires will have the same effect as pressing the button and it should trigger the camera. Connect the modified remote shutter release control to the two pins exposed to the front side of the scanners control module as shown on the first image of this chapter.

#### Remote shutter release (II)

This is another very typical remote shutter release. It contains three metal plates which gets pushed/connected consecutively (*red circle*). Creating a connection between the first and second metal plate will focus the camera. Wheras connecting all plates will trigger the shutter release.

![image](https://user-images.githubusercontent.com/57842400/181221885-a87af87a-ce88-41bb-8447-173d6a4e0929.png)

Connect one wire each to the top and to the bottom metal plate. Shortening those two wires will have the same effect as pressing the button and it should trigger the camera.

Connect the modified remote shutter release control to the two pins exposed to the front side of the scanners control module as shown on the first image of this chapter.

#### Bluetooth trigger (iOS/Android)

A modified Bluetooth trigger can be used to trigger most smartphone cameras. The shown module is operated with a CR2032 button cell, which must be inserted on the back. As soon as the On / Off switch has been flipped, the blue LED lights up at regular intervals. The device must then be paired with the smartphone via Bluetooth. This can be done in the smartphone’s setting menu. The device should be visible as “AB Shutter 3” and has to be coupled accordingly

![image](https://user-images.githubusercontent.com/57842400/181213900-8c24d8a1-db15-471b-bb41-f5635dc9fdb1.png)

Connect the modified remote shutter release control to the two pins exposed to the front side of the scanners control module as shown on the first image of this chapter.

## Operation

TODO