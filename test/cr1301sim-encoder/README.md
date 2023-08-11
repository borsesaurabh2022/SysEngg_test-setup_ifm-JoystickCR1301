# CR1301 IFM Simulator

A simple simulator to test the [CR1301](https://www.ifm.com/de/de/product/CR1301) ifm joystick. The software allows to to simulate the data that the joystick sends and recieves over CAN with the [Seedstudio USB-CAN Analyzer](https://www.seeedstudio.com/USB-CAN-Analyzer-p-2888.html).

Instead of using the CR1301 you can use this software to test your CAN implementation by connecting your MCP2515 module directly to the Seedstudio USB-CAN Analyzer. The simulator will send the same type of CAN message and value format. 

## Requirements

- Windows 10
- [Seedstudio USB-CAN Analyzer](https://www.seeedstudio.com/USB-CAN-Analyzer-p-2888.html)

## How to Use

- Download the [files](https://git.fh-aachen.de/systemsengineering_81617/cr1301sim/-/archive/v1.0.0/cr1301sim-v1.0.0.zip) from this repository or the release section.
- Execute `CR1301Simulator.exe` Make sure that the file `CR1301.ui` is in the same directory.

## How to Use

1. Connect your USB-CAN analyzer.

1. Execute CR1301Simulator.exe

1. Select the Correct Serial Port and click connect.
  - If you connect the USB-CAN Analyzer after executing `CR1301Simulator.exe`, click the Update button to refresh the list of devices

1. Once connected you can use the integrated buttons and Rotary Encoder to simulate the CR1301 joystick
  - The encoder can be rotated by click over it but must be released to update the value.
  - You can only click and release one button at the time.
  - There is a central button which simulates the encoder Enter button.
  - LED simulation is done by changing the color of the buttons. The circular LED rings are simulated with 4 rectangles that are located behind the rotary encoder. Each of these rectangles correspond to each one of the circular LEDs. To change the LED value check the datasheet of the CR1301 device.
  - Rotary Tilt buttons are implemented as push buttons with an arrow symbol.

  

Note: The real device keeps the LED status and Color while the device is connected to its power supply. After disconnecting it from the power supply,the LED state will be off and the color configuration will be lost.

## Bug reports

Report any bugs by opening an issue in this repository
