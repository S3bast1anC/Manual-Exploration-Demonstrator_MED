# Manual-Exploration-Demonstrator_MED
The Manual Exploration Demonstrator (MED) is a rover developed to test hands-on exploration capabilities. Inspiration from Mechanical Sciences’ - [Design and analysis of a six-wheeled companion robot with mechanical obstacle-overcoming adaptivity](https://ms.copernicus.org/articles/12/1115/2021/). This repo provides an overview of MED's design, components, and operational guidelines to facilitate its use and maintenance.

<p align="center">
  <img src="https://github.com/user-attachments/assets/8327a3b1-5155-4a9e-af3e-ed5bbbbabbe0" width="800" height="400" />
</p>

## About MED
### Motivation
The core design of MED revolves around a six-wheel rover with two independently rotating rear arms. This rover was created for the Mars Habitat at Berkeley (MHAB) software sub-team for autonomous code testing. The rover's modular design allows for future modifications, whether through hardware upgrades or software adjustments. Its six-wheel design allows  navigation across complex terrain, while the rotating rear provide additional mobility for overcoming obstacles.

We aim to share insights and lessons learned from the design, testing, and implementation of the MED rover. We hope that this information will not only assist the MHAB team but also inspire and guide future rover projects.

### Overview
<p align="center">
  <img src="https://github.com/user-attachments/assets/0a59afe7-0a09-47da-bc90-da4362551b3e" width="600" height="350" />
</p>

Development of MED began as part of the Final BLE Vehicle project for the UC Berkeley Summer 2024 DesInv22 class. Over the course of four weeks, myself and Andrew Alatorre engaged in a process of design, testing, iteration, and refinement to bring the rover to its current state.

<div align="center">
<table>
  <tr>
    <td>
      <table>
        <tr>
          <th>Specification</th>
          <th>Details</th>
        </tr>
        <tr>
          <td>Dimension (LxWxH)</td>
          <td>tbd</td>
        </tr>
        <tr>
          <td>Top Speed</td>
          <td> tbd m/s</td>
        </tr>
        <tr>
          <td>Total Mass</td>
          <td> tbd kg</td>
        </tr>
        <tr>
          <td>Wheel Diameter</td>
          <td> 6.9cm (front/rear), 8.61cm (back) </td>
        </tr>
        <tr>
          <td>Operational Range</td>
          <td> tbd </td>
        </tr>
        <tr>
          <td>Climbing Gradient</td>
          <td> tbd </td>
        </tr>
        <tr>
          <td>Cost</td>
          <td> ## </td>
        </tr>
      </table>
    </td>
    <td>
      <a href="https://youtu.be/sea0DLn0pgA" target="_blank">
    <img src="https://github.com/user-attachments/assets/4a8a327f-5c5b-4007-b593-dffaa204a712" alt="Watch the video" width="550" height="400">
</a>
    </td>
  </tr>
</table>
</div>

## Components
### Features

<p align="center">
  <img src="https://github.com/user-attachments/assets/43d78482-e38e-4f1f-85d5-6ead06611cae" width="650" height="400" />
</p>

<ul>
  <li> <b> Six-Wheel Drive: </b> MED is built on a six-wheel drive system, providing improved traction and stability. This configuration ensures balanced weight distribution and allows the rover to handle rough, uneven surfaces with ease.</li>
  <li> <b> Freely Rotating Rear Arms: </b> The two rear arms are capable of rotating freely, giving the rover additional flexibility when navigating obstacles. These arms help stabilize the rover going over inclines and allow for obstacle-overcoming adaptivity in challenging environments.</li>
  <li> <b> Lightweight Build: </b> Constructed from PLA and acrylic, MED’s lightweight chassis allows for easy transportation and reduced energy consumption, while still offering a durable frame for the rover's internal electronics. It was designed this way as an ideal balance between durability and weight, enabling both indoor and outdoor testing.</li>
<li> <b>Rear Storage Compartment:</b> MED includes a simple rear storage compartment, serving as an early look at soil collection concepts. While still remaining simple in design so it can be changed easily." </li>
  
</ul>

### ELECTRONICS
- Arduino Uno Rev3 ([DIGIKEY](https://www.digikey.com/en/products/detail/arduino/A000066/2784006?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-2784006_sig-EAIaIQobChMIl_rivNOGiAMVHQ2tBh29HTAjEAQYASABEgLOA_D_BwE&gad_source=1&gclid=EAIaIQobChMIl_rivNOGiAMVHQ2tBh29HTAjEAQYASABEgLOA_D_BwE)) ([DESC](https://store-usa.arduino.cc/products/arduino-uno-rev3?srsltid=AfmBOorpQkAFCFV9pK8a8AKKXCVHNyX5GI4hv3l4IM5aVDzLocPXSwW7))
- Adafruit Motor Shield V2 ([DIGIKEY](https://www.digikey.com/en/products/detail/adafruit-industries-llc/1438/5353647?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-5353647_sig-EAIaIQobChMI_8uYnc6GiAMVuTetBh3_FTN3EAQYASABEgL3VvD_BwE&gad_source=1&gclid=EAIaIQobChMI_8uYnc6GiAMVuTetBh3_FTN3EAQYASABEgL3VvD_BwE)) ([DESC](https://learn.adafruit.com/adafruit-motor-shield-v2-for-arduino/overview))
  - Bluefruit LE UART BT BLE ([DIGIKEY](https://www.digikey.com/en/products/detail/adafruit-industries-llc/2479/5356835?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-5356835_sig-EAIaIQobChMIztqP7MyGiAMVFh6tBh2mNAVsEAQYASABEgJBQPD_BwE&gad_source=1&gclid=EAIaIQobChMIztqP7MyGiAMVFh6tBh2mNAVsEAQYASABEgJBQPD_BwE)) ([DESC](https://www.adafruit.com/product/2479))
  - Stacking Headers ([DIGIKEY](https://www.digikey.com/en/products/detail/adafruit-industries-llc/85/5154649?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-5154649_sig-EAIaIQobChMInuS39M6GiAMVpRKtBh3lGDP-EAQYASABEgK0NvD_BwE&gad_source=1&gclid=EAIaIQobChMInuS39M6GiAMVpRKtBh3lGDP-EAQYASABEgK0NvD_BwE)) ([DESC](https://learn.adafruit.com/adafruit-motor-shield-v2-for-arduino/install-headers))
- 4 DC Gear Motor TT - 120 RPM ([DIGIKEY](https://www.digikey.com/en/products/detail/seeed-technology-co.,-ltd/114090050/10385087?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-10385087_sig-EAIaIQobChMI8M6mgs6GiAMVdxGtBh0vUSmqEAQYASABEgIGUPD_BwE&gad_source=1&gclid=EAIaIQobChMI8M6mgs6GiAMVdxGtBh0vUSmqEAQYASABEgIGUPD_BwE)) ([DESC](https://grobotronics.com/dc-gear-motor-tt-120-rpm-metal-shaft-blue.html?sl=en))
- 10 AA Batteries (4 for R3 board, 6 for DC motors)

### Other Parts
- 3 Radial Ball Bearings (608ZZ) ([DIGIKEY](https://www.digikey.com/en/products/detail/adafruit-industries-llc/1178/5356858?_gl=1*1i5bfi0*_up*MQ..&gclid=EAIaIQobChMI_8uYnc6GiAMVuTetBh3_FTN3EAQYASABEgL3VvD_BwE))
- 2 4AA Battery Holder with On/Off Switch ([PARTSEXP](https://www.parts-express.com/4-AA-Battery-Holder-with-On-Off-Switch-140-784?quantity=1&utm_source=google&utm_medium=cpc&utm_campaign=21096330877&utm_content=163485008367&gadid=693249752043&gad_source=1&gclid=EAIaIQobChMI4NCnx-mGiAMVVQKtBh3b0yNSEAQYAyABEgL6BPD_BwE))
- 1 2AA Battery Holder with On/Off Switch ([DIGIKEY](https://www.digikey.com/en/products/detail/sparkfun-electronics/PRT-09925/6161750?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Low%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20243063506_adg-_ad-__dev-c_ext-_prd-6161750_sig-EAIaIQobChMIq9-B3caJiAMVm9XCBB0X_xDbEAQYASABEgLW-vD_BwE&gad_source=1&gclid=EAIaIQobChMIq9-B3caJiAMVm9XCBB0X_xDbEAQYASABEgLW-vD_BwE))
<p align="center">
  <img src="https://github.com/user-attachments/assets/b7ac72f9-31ec-4863-a756-b961791c01ae" width="600" height="550" />
</p>

### Notes
The V-in on the the adafruit motor shield was busted (i.e it wouldn't power the arduino which is an issue because that's what runs the code) so to solve this issue a 4 battery pack was soddered onto the bottom of the board to power it (it's a 5V board). Also the arduino is a limited edition [Maker Shed Exclusive](https://makezine.com/article/technology/arduino/maker-shed-exclusive-make-special-edition-arduino-unos/) uno board (no particular reason that's just what was lying around).

## Software
### Setup
The software for MED is designed to run on Arduino BLE software and communicates with the rover's motors and sensors via Bluetooth using the Ada_BLE_RC program. Ensure that the following three files are placed inside this folder:
1. Ada_BLE_RC.ino - This is the main Arduino sketch file that contains the code to control the rover.
2. BluefruitConfig.h - This header file includes configuration settings specific to the Adafruit Bluefruit BLE module, such as connection parameters and pin definitions.
3. packetParser.cpp - This C++ file handles the parsing of incoming data packets from the Bluetooth controller, translating them into motor control commands for the rover.

Once you have these files inside the Ada_BLE_RC folder, the entire folder should be uploaded to the Arduino IDE. To ensure the code runs correctly, you need to install the following libraries:
- Adafruit BluefruitLE nRF51 (Includes Adafruit_BLE, Adafruit_BluefruitLE_SPI, Adafruit_BluefruitLE_UART)
- SPI (Built-in with Arduino IDE)
- SoftwareSerial (Built-in with Arduino IDE)

### Bluetooth
The Bluefruit Connect app by Adafruit allows you to send commands to your rover via Bluetooth using a smartphone. Once the app is installed:
- Enable Bluetooth on your smartphone if it's not already on
- Open the Bluefruit Connect app
- Tap the "Connect" button within the app. It will scan for available Bluetooth devices
- Select your Bluefruit BLE module from the list of available devices (it may be named something like "Bluefruit52" or "UART")
- Once connected, you can access various control options within the app such as Control Pad, Accelerometer, or Color Picker to send commands to the rover

![Untitled-1](https://github.com/user-attachments/assets/ee7e7a2d-93f2-459b-b860-7263f17b6efb)

To change the rpm the motors go at go to lines 302-305 (for example 'L_MOTOR1->setSpeed(##);' ).

## Parameterized Design Model
This drawing presents the geometric parameter model of MED. The diagram highlights the rover's key coordinate frames, geometric parameters, and critical angles.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c7d1c9f2-744d-4b60-a5c9-23852d92105f" width="550" height="400" />
</p>

Coordinate Frames:
- O: The global reference frame. This serves as the origin for measuring key lengths and angles for the system's kinematics.

Key Measurements:
- Width (W): Denotes the total width of the rover, measured from the outer edges of the wheels on the left and right sides.
- Length (L): Refers to the overall length of the rover, including the front and rear sections.
- Arm Radius (R): Represents the distance from the centroid of the arms at O<sub>2</sub> to the tip of the rocker arm wheels.
- Arm Wheel Radius (r<sub>0</sub>): Describes the radius of the arm wheels connected to the rocker arms.
- Rear Wheel radius (r<sub>1</sub>): Denotes the radius of the rear wheels of the rover.
Angles:
- θ<sub>r</sub>: The right arm swing angle, which defines the rotational displacement of the right rocker arm about its pivot point at O<sub>2</sub>.
- θ<sub>l</sub>: The left arm swing angle, representing the rotational displacement of the left rocker arm about its pivot point at O<sub>1</sub>.
- θ<sub>b</sub>: The rear body rotation angle, indicating the tilt or rotation of the rear section of the rover relative to the global reference frame.

The diagram shows the rover's geometric and kinematic structure, focusing on the relationship between the rocker-bogie arms, wheels, and the main body. The rover is depicted with its front and rear sections symmetrically positioned about the center of mass, labeled as C. The length of the rover, L, is measured between the front and rear wheels, while the width W is measured between the outermost points of the left and right wheels. The rocker arms pivot at points O<sub>2</sub>​ and O<sub>1</sub>​, and their movement is characterized by the swing angles θ<sub>r</sub> and θ<sub>l</sub>​. The rotation of the rear section is captured by θ<sub>b</sub>​. 

The radii R and r<sub>0</sub>​ describe the size and positioning of the rocker arm wheels, with R being the length from the rocker arm pivot point to the wheel, and r<sub>0</sub> and r<sub>1</sub> defining the sizes of the arm wheels and rear wheels, respectively. These measurements are essential for understanding how the rover adapts to different terrains, using the rocker-bogie suspension system to maintain stability across uneven surfaces.

The kinematic relationships between these measurements and angles will help model the rover’s behavior, providing insights into its ability to traverse challenging terrain by allowing independent wheel articulation.
