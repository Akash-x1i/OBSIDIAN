# Features:

1. 2ch 32bit DAC
	- 128 times Oversampling
	- 32-bit High Quality Sound Low Group Delay Digital Filter
	- Single Ended Output, Smoothing Filter
	- THD+N: 91dB- DR, S/N: 108dB
	- Channel Isolation Digital Volume (12dB to -115dB, 0.5dB Step, Mute)
	- Soft Mute
	- Audio I/F Format: MSB justified, LSB justified, I2S, TDM
2. Sampling Frequency
	- Normal Speed Mode: 8kHz to 48kHz
	- Double Speed Mode: 48kHz to 96kHz
	- Quad Speed Mode: 96kHz to 192kHz
3. Master Clock:
	256fs, 384fs, 512fs or 768fs         (Normal Speed Mode: fs=8kHz to 48kHz)
	256fs or 384fs                              (Double Speed Mode: fs=48kHz to 96kHz)128fs or 192fs                  (Quad Speed Mode: fs=96kHz to 192kHz)
4. ɥP Interface: 3-wire Serial (7MHz max)I2C bus (Fast Mode: 400kHz, Fast Mode Plus: 1MHz)
5. Power Supply- Analog: AVDD = 3.0 to 3.6V- Input/Output Buffer: LVDD = 3.0 to 3.6V- Integrated LDO for Digital Power Supply
6. Power Consumption: 7.8mA (fs=48kHz)
7. Operational Temperature: Ta = - 40 to 105°C
8. Package: 16-pin TSSOP (0.65mm pitch)

# Recommended External Circuits

## Official datasheet:

![[Pasted image 20250817152937.png]]

## Eval-Kit Schematics:

![[Pasted image 20250817221741.png]]

## AC-3 detection for 5.1 audio:

![[Pasted image 20250817222724.png]]


## I2S Headers:


![[Pasted image 20250817223218.png]]



## Schmitt Trigger: SN74LVC2G14
####  - Ideal for applications where the input signal is noisy or has slow rise/fall times, such as clock signal conditioning, debouncing mechanical switches, or in noisy environments.

![[Pasted image 20250817232118.png]]


## Logic Level Shifter: PCA9306DP1 

![[Pasted image 20250817231854.png]]


## Mux TC7MBL3257: for switching between different input methods.

![[Pasted image 20250817232429.png]]



## Power : digitall and analog power distribution

12V diagram:
![[Pasted image 20250817233027.png]]

two different buck converter for analog and digital power source. and GND is splitted into two to provide all of the D/A supply from there (to maintain single point of connection b/w analog and digital)







# References: 

Digikey : https://www.digikey.in/en/products/detail/asahi-kasei-microdevices-akm/AK4432VT/5287017

Datasheet: https://www.akm.com/content/dam/documents/products/audio/audio-dac/ak4432vt/ak4432vt-en-datasheet.pdf#page=40.3


Evalkit Datasheet: https://www.akm.com/content/dam/documents/products/audio/audio-dac/ak4432vt/ak4432vt-en-evaluationmanual.pdf  (above schematics).

