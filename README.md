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
          <td>RPM</td>
          <td>240</td>
        </tr>
        <tr>
          <td>Speed</td>
          <td> ?? m/s</td>
        </tr>
        <tr>
          <td>Mass</td>
          <td> ?? kg</td>
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

<p align="center">
  <img src="https://github.com/user-attachments/assets/b7ac72f9-31ec-4863-a756-b961791c01ae" width="600" height="550" />
</p>


<table border="1"> 
        <tr> 
            <td><img src= 
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png" 
                alt="GFG Logo" width="100" 
                height="100"> 
            </td> 
          <td><img src= 
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png" 
                alt="GFG Logo" width="100" 
                height="100"> 
            </td> 
        <tr> 
            <td><img src= 
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png" 
                alt="GFG Logo" width="100" 
                height="100"> 
            </td> 
          <td><img src= 
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190710102234/download3.png" 
                alt="GFG Logo" width="100" 
                height="100"> 
            </td> 
        </tr> 
    </table> 

<a href="https://store-usa.arduino.cc/products/arduino-uno-rev3?srsltid=AfmBOorpQkAFCFV9pK8a8AKKXCVHNyX5GI4hv3l4IM5aVDzLocPXSwW7" target="_blank">
    <img src="https://github.com/user-attachments/assets/86e5e12c-7286-4164-8783-b7ca691af8b1" width="550" height="400">
</a>
