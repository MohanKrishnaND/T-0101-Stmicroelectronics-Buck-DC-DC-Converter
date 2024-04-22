# ✅ T-0101-Stmicroelectronics-Buck-DC-DC-Converter ✅

## :book: ABOUT THE REPOSITORY
This Repository contains all the information regarding the project along with the respective code .


<p >
  <img src="https://github.com/MohanKrishnaND/T-0101-Stmicroelectronics-Buck-DC-DC-Converter/assets/156279619/938d672c-609e-460a-846b-8ba6baab81ee" width=800 >
</p>


# TABLE OF CONTENTS

+ [Task 1️⃣ : Interfacing Mikroe USB type C SInk Click 3 Board with raspberry pi](#interfacing-mikroe-usb-type-c-sink-click-3-board-with-raspberry-pi)
  - SOC Design and OpenLane
  - Get Familiar to OpenSource EDA Tools

+ [Task 2️⃣ : I2C communication with mikroe click 3 sink board to send VSEL voltage values.](#i2c-communication-with-mikroe-click-3-sink-board-to-send-vsel-voltage-values)
  - Chipfloor Planning Considerations
  - Library Binding and Placements
  - Cell Design & Characterization flows
  - General Timing Characterization Parameters

+ [Task 3️⃣ : SPI communication with mikroe click 3 sink board to send VSEL voltage values](#design-library-cell-using-magic-layout-and-ngspice-characterization)
  - Labs for CMOS inverter ngspice simulations
  - Inception of layout and CMOS Fabrication Process
  - Sky130 Tech file labs

+ [Task 4️⃣ : Interfacing I2C multiplexer with the raspberry pi](#interfacing-i2c-multiplexer-with-the-raspberry-pi)
  - Timing Modelling using Delay Tables
  - Timing analysis with Ideal Clocks(OpenSTA)
  - Clock Tree Synthesis TritonCTS and signal integrity
  - Timing analysis with Real Clocks(OpenSTA)
 
+ [Task 5️⃣ : Interfacing I/O expander with the raspberry pi](#interfacing-i/o-expander-with-the-raspberry-pi)
  - Timing Modelling using Delay Tables
  - Timing analysis with Ideal Clocks(OpenSTA)
  - Clock Tree Synthesis TritonCTS and signal integrity
  - Timing analysis with Real Clocks(OpenSTA)

+ [Task 6️⃣ : Integrating I2C multiplexer, 2 mikroe usb type c sink click 3 baord along with all the peripherals](#integrating-i2c-multiplexer-2-mikroe-usb-type-c-sink-click-3-baord-along-with-all-the-peripherals)
  - Routing and Design Rule Check (DRC)
  - Power Distribution Network (PDN) & Routing
  - Triton Route Features

<br>
<br>


# CONTENT INFORMATION

# 📌 TASK-1

# Interfacing Mikroe USB type C SInk Click 3 Board with raspberry pi

code : 

```
import smbus
from smbus2 import SMBus, i2c_msg
import time
import RPi.GPIO as GPIO     #import RPi.GPIO module

bus = smbus.SMBus(1)
time.sleep(1) #wait here to avoid 121 IO Error

while True:
    data = input("Enter the Input")
    data_PIR=[00]
    write_CR = bus.write_i2c_block_data(65,3,[int(data)]) # writing the data value into the configuration register
    read_CR = bus.read_i2c_block_data(65,3,1)
    print("COnfiguration Port Register Value :", read_CR)
    result = 0
    for b in read_CR:
        result = result * 256 + int(b)
    print(result)
    time.sleep(1)

```


[Back to main](#table-of-contents)




# 📌 TASK-2

# I2C communication with mikroe click 3 sink board to send VSEL voltage valuess

[Back to main](#table-of-contents)




# 📌 TASK-3

# SPI communication with mikroe click 3 sink board to send VSEL voltage values


[Back to main](#table-of-contents)






# 📌 TASK-4

#  Interfacing I2C multiplexer with the raspberry pi
<br>


[Back to main](#table-of-contents)




# 📌 TASK-5

#  Interfacing I/O expander with the raspberry pi


[Back to main](#table-of-contents)




# 📌 TASK-6

# Integrating I2C multiplexer, 2 mikroe usb type c sink click 3 baord along with all the peripherals


[Back to main](#table-of-contents)
