## Design choices
My main goal was to apply my EEE course theory and make a compact, feature rich and comparable pedal to what is in the market.

- TL081 for a classic rock sound due to its slow slew rate. Used it as a high gain input stage straight into a clipping distortion stage that has 4 separate modes toggled by switches. Clipping has 2 modes with 2 options for soft and hard clipping using diodes in the feedback loop or post gain stage.
- Input high resistance resistor to eliminate loud pops when plugging in a guitar and a 7.9kHz input filter to eliminate noise.
- 2 NE5532's were used due to their very fast slew rate and dual amp design, allowing the entire tone stack and volume to be made using 2 chips saving space on the PCB and prototype breadboard design used for testing. I used a mix of the NE5532 with passive filters post gain to shape the post high gain stage sound.
- The power delivery is handled by a 7660 charge pump IC delivering 9V and around -8.7V from a 9V barrel jack or 9V battery input. The slightly lower -V is due to losses in the IC but as the headroom is so large it doesn't affect the sound. The large 17.7V swing allows for the battery to discharge if used and not affect the output sound as well as a massive amount of gain to be delivered and true biasing on the op amps.
- All chips feature de-coupling capacitors for immediate power draw and to keep fluctuating power inputs to a minimum. The charge pump IC also features some LC filters to eliminate wall power noise and any noise from entering its supply rails or being output on the power rails. 
- The board is a 4 layer design with a ground plane, a dedicated power plane and 2 signal planes. My main goal with a 4 layer design over a 2 layer one was to improve signal integrity and to keep the PCB small.


## Noise management

I aimed to reduce noise with a dedicated ground plane, short traces and filters. My input has a low pass filter with a cut-off frequency of 7kHz to eliminate high frequency noise from reaching my high gain stage. During my active tone stack the gain is around 7x when a setting is maxed out providing enough room for my SNR to be large enough to where fizz noise can't be heard at the output. My power delivery has LC filters for both 9V and -9V power rails to keep noise to a minimum. 2 signal planes and a ground plane keep my signal traces shorter than a 2-layer PCB and provide a lower return impedance.


## Improvements/takeaways

- During my current review I've noticed some traces routed under capacitors that are signal traces. This in hindsight is a bad design as noise from the caps would be introduced even if tiny would worsen the output sound. 
- The charge pump IC I'm also using is operating on the edge of what it can supply in terms of current output, it functions but a more capable IC would be better
- The project overall cemented the use of filters and op amps post theory, showing me that even if the math is perfect component tolerances play a big part in the finished product and need to be take into account during the design
- It taught me transfer functions pre learning them in my course and helped me tremendously during the teaching of filter and transfer function theory
- My first project involving a PCB, which has taught me valuable concepts and constraints I didn't really think about before making my own PCB like a ground plane and its benefits etc.
- Learnt that mixing signals requires extra components other than just connecting multiple lines to one point like output resistors on my op amp outputs in my tone stack to keep signals from mixing into each others feedback loops
- Valuable experience reading, digesting and designing IC circuits according to their datasheets and modifying those circuits to serve my purpose while following constraints like max current and voltage ratings
