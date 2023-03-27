# Communication-Board

JLCPCB is a company that constructs PCBs and prints 3D mechanical designs, they give us great offers with cheap prices for high quality precision PCBs. I would like to thank JLCPCB for their sponsorship and for supporting me in creating and innovating schematics, and improving my PCBs designs.

Every organism has different ways for communication,humans have different languages, also Microcontrollers have too different tools, among these last it has:
I2C, I2S, SPI, UART, CAN Bus, Bluetooth, Wifi,and AXI Bus. 
We can find it as separate modules for every tool.

This PCB is designed to separate different tools included in esp32.

UART ( universal asynchronous receiver transmitter ): as the name indicates its serial communication  and asynchronous protocol which does not use any clock source for synchronizing the data,so there are more chances of losing the data over UART protocol. UART has two wires for its transmitting and receiving ends.

I2C ( inter integrated circuit ): It is a half-duplex bi-directional two-wire bus system for transmitting and receiving data between masters and slaves. In I2C only two signals are used regardless of the number of devices on the bus. Signals used are 
SCL (Serial clock) and SDA(Serial Data).Both these signals are pulled up to a positive power supply voltage. 

SPI ( Synchronous Peripheral Interface ): it’s a full-duplex uni-directional in sens of the Master who initiates communication,it use 4 wires for it:
RCLK( Serial clock ): clock generated by Master.
MOSI( Master Output Slave Input ): data wire from Master to Slave.
MISO( Master Input Slave Output ): Data wire from slave to master.
SSn( Slave Select n ): wire for selecting the receiver.

I2S (Inter-IC Sound):  is a serial and synchronous communication protocol that is usually used for transmitting audio data between two digital audio devices.
on the ESP32 microcontroller These peripherals can be configured to input and output sample data via the I2S driver.
MCLK: Master clock line. It’s an optional signal depending on the slave side, mainly used for offering a reference clock to the I2S slave device.
BCLK: Bit clock line. The bit clock for the data line.
WS: Word(Slot) select line. It is usually used to identify the vocal tract except PDM mode.
DIN/DOUT: Serial data input/output line.

CAN Bus (Controller Area Network): can bus is half duplex generally used in automotive, avionics and industrial machines. The transmission consists of a differential peer, it has 2 wires CAN-High and CAN-Low.Each equipment it's a node.

The ESP32 contains a  CAN Controller that can process all the information to and from the CAN bus.

We added an SN65HVD231DR CAN transceiver that can translate the logic level messages from the controller into the CAN differential on the CANH and CANL pins of the CAN transceiver.


Bluetooth: Bluetooth technology allows devices to communicate with each other without wires. Bluetooth relies on short-range radio frequency, and any device that incorporates the technology can communicate as long as it is within the required distance.
ESP32 supports two bluetooth modes: simple bluetooth and bluetooth low energy.

WIFI: Wi-Fi is a wireless technology used to connect computers, tablets, smartphones and other devices to the internet.

ESP32 has 2 WiFi modes: 
STATION ( WIFI_STA ): The Station mode (STA) is used to connect the ESP32 module to a WiFi access point. The ESP32 behaves like a computer that is connected to our router.

AP (Access Point): In Access Point mode, the ESP32 behaves like a WiFi network other devices can connect to it.In this mode, the ESP32 is not connected to any other network and is therefore not connected to the Internet.

Also it has pins for touch sensors. Pins of those protocols can be used as normal pins in case we don't need that communication.

It contains pins connected with ADC (Analog Digital Converter) and DAC(Digital Analog Converter), each pin is a pwm pin (pulse width modulation pin).

To upload code on the microcontroller we made pins for ftdi programmers and we have 2 buttons used for  boot and reset the ESP32.Also 2 Outputs voltage in choice can be 3.3v,5v and Vin it depends where we put the jumper.
JLCPCB link: https://jlcpcb.com/HAR
