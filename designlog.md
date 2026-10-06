**Design choices and power delivery**

My main goal was to make a compact, feature rich and comparable pedal to what is in the market. I chose a TL081 for a classic rock sound due to its slow slew rate and used it as a high gain input stage straight into a clipping distortion stage that has 4 separate modes. The NE5532 was used due to its very fast slew rate and quad amp design allowing me to do the entire tone stack and volume around a single chip saving space on the PCB and prototype breadboard design used for testing. I used a mix of the NE5532 with passive filters post gain to shape the input sound and a feedback and output clipping design for my high gain TL081 input. The power delivery is handled by a charge pump IC delivering +9 and around -8.7 volts from my 9V barrel jack or battery input. The slightly lower -V is due to losses in the IC but as the headroom is so large it doesn't affect the sound. The large 17.7V swing allows for the battery to discharge if used and not affect the output sound as well as a massive amount of gain to be delivered. All chips feature de-coupling capacitors for immediate power draw and to keep fluctuating power inputs to a minimum. The charge pump IC also features some LC filters to eliminate wall power noise and any noise from entering its supply rails or being output on the negative rail. The board is a 4 layer design with a ground plane for keeping low impedance and providing as much noise reduction as possible as well as a dedicated power plane, there is 2 signal planes as well and my main goal with a 4 layer design over a 2 layer one was to keep routing and placement concise and close together for space. In the end some decisions made here are in hindsight now not the best and I will discuss them later on.



**Noise management**

As this is a guitar pedal I aimed to reduce noise with the copper ground pour plane as well as short traces and filters. My input has a low pass filter with a cut-off frequency of the highest guitar note achievable which is around 8Khz to eliminate high frequency noise from reaching my high gain stage. During my active tone stack the gain is also high at around 7x peak when a setting is maxed out providing more than enough room for my SNR to be large enough to where fizz noise can't be heard at the output.



**Improvements and my final thoughts**

During my current review I've noticed some traces routed under capacitors that are signal traces. This in hindsight is a bad design as noise from the caps would be introduced even if tiny would worsen the output sound. The use of my LC circuits at the charge pump IC would also drain unnecessary amounts of power while in use and a simple RC circuit would seem to be better to use less power. The charge pump IC I'm also using is operating on the edge of what it can supply in terms of current output, it functions but a more capable IC would be better

