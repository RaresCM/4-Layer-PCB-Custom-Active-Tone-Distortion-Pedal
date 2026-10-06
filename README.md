# Custom 4 Layer PCB Active Tone Distortion Pedal
This is a custom built distortion pedal aiming to apply theoretical knowledge from my EEE course to a real life project including filters, op amps, diode clipping, power management and analog circuitry. It's also my first attempt at designing a circuit from scratch with documentation and online resources as well as diving into PCB design, which are currently outside my courses scope.

<img width="783" height="1013" alt="image" src="https://github.com/user-attachments/assets/f41e8da3-1507-4f7d-99da-4d32a181b55b" />

## Specifications:
- 4 Layer PCB with a dedicated ground copper pour plane, power plane and 2 signal planes
- 9V Barrel jack wall input/9V battery with a ±9V delivery using a charge pump
- 2 Op Amp design using a TL081 for gain and a NE5532 for volume output and 3 active tone stack
- De-coupling capacitors for stable op amp operation and low pass filter input for noise elimination 
- Designed in KiCad 10.0 and verified manufacturable by a JLCPCB quote

<img width="1607" height="1017" alt="image" src="https://github.com/user-attachments/assets/1f2e7798-6c8e-453c-8283-23a33e709526" />
<img width="803" height="1058" alt="image" src="https://github.com/user-attachments/assets/96ed6fdb-11f1-427e-802a-7e14b39602cc" />

## Repository Structure
- /manufacturing - KiCad generated gerber and manufacturing files already zipped
- /Distortion Pedal - KiCad files for the schematic, PCB layout, 3D model etc.
- /designlog - My design walkthrough of coming up with the current version and what could be improved
