# Custom 4 Layer PCB Active Tone Distortion Pedal
Custom distortion pedal design aiming to apply theoretical knowledge from my EEE course to a real life project. Designed from the ground up from schematic to PCB to 3D model by me.

Implements my EEE course theory on filters, op-amps, power delivery and analog circuits.

<img width="783" height="1013" alt="image" src="https://github.com/user-attachments/assets/f41e8da3-1507-4f7d-99da-4d32a181b55b" />

## Specifications:
- 4 Layer PCB with a dedicated ground copper pour plane, power plane and 2 signal planes
- Dual 9V power input from a battery or barrel jack with ±9V delivery using a charge pump
- 3 Op-Amp design using a TL081 for gain and 2 NE5532 for volume output and 3 tone active tone stack
- De-coupling capacitors for stable op amp operation and a low pass filter input for noise elimination
- Designed in KiCad 10.0

<img width="1607" height="1017" alt="image" src="https://github.com/user-attachments/assets/1f2e7798-6c8e-453c-8283-23a33e709526" />
<img width="803" height="1058" alt="image" src="https://github.com/user-attachments/assets/96ed6fdb-11f1-427e-802a-7e14b39602cc" />

## Repository Structure
- /manufacturing - KiCad generated gerber and manufacturing files
- /Distortion Pedal - KiCad files for the schematic, PCB layout, 3D model etc.
- /designlog - My design decisions and what could be improved
