# Custom ATmega328P LED Blinker PCB
This project demonstrates how to design a custom PCB using the ATmega328P microcontroller to blink an LED at 1-second intervals. It is a beginner-friendly project aimed at learning the basics of schematic design, component selection, PCB layout, and microcontroller programming.

## 🚀 Project Goal
Design and build a standalone ATmega328P-based LED blinker circuit with:
- Crystal oscillator clock source
- Power regulation (5V)
- ISP programming header
- LED output to demonstrate code upload success

## 🧠 Learning Outcomes
✅ Schematic design using Altium Designer  
✅ Microcontroller integration  
✅ Power and clock circuitry  
✅ Basic PCB layout and routing  
✅ Preparing files for PCB fabrication  
✅ Testing and uploading code via ISP  


## 🖼️ Schematic and PCB Layout

All files are included under the `/Schematic` and `/PCB_Layout` folders.

**Highlights:**
- Decoupling capacitors near VCC  
- Crystal and caps placed close to XTAL pins  
- GND and VCC planes separated  
- Proper trace width and clearance maintained  

## 🔧 Firmware

### Blinking Code (Arduino IDE Compatible):

```cpp
void setup() {
  pinMode(13, OUTPUT); // PB5 (Digital pin 13)
}

void loop() {
  digitalWrite(13, HIGH);
  delay(1000);
  digitalWrite(13, LOW);
  delay(1000);
}
````
Use **USBasp** or **Arduino as ISP** to upload the code.

## 🛠️ Testing Procedure
1. Power the board with 7–12V input
2. Verify 5V output from the regulator
3. Flash code using ISP header
4. Confirm LED blinks at 1Hz
5. If LED doesn’t blink, check for shorts, missing solder joints, or upload errors

## 📦 Folder Structure
```
ATmega328P_LED_Blinker_PCB/
├── Schematic/
│   └── LED_Blink_Schematic.pdf
├── PCB_Layout/
│   └── LED_Blinker_PCB_Top_Bottom.Gerber
├── Firmware/
│   └── LED_Blink.ino
├── Project Outjobs/
│   └── LED_Blink gerber and NC drill files
├── Images/
│   └── PCB_View.png
├── BoM/
│   └── Smart PDF.pdf
├── Documentation/
│   └── README.md
│   └── Final_Report.pdf
```

## 🌱 Future Improvements
* Add USB-to-Serial interface (e.g., CH340 or FTDI)
* Add power LED and polarity protection diode
* Add tactile switch or sensor input
* Use SMD ATmega328P to reduce PCB size

## ✨ Credits
* Designed by: \Roaida Binta Ali
* Tool Used: Altium Designer
* Year: 7-18-2025

