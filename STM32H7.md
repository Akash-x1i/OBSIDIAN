

# Schematics:

## WeAct Studio: 

![[Pasted image 20250818010004.png]]


## Essenceia Github:
![[Pasted image 20250818002447.png]]


## Nucleo 144 H7:

https://www.st.com/resource/en/schematic_pack/mb1364-h743zi-c01_schematic.pdf


## Reddit post:

![[Pasted image 20250818004518.png]]






# Reference: 
WeAct Studio:
- 
- https://robu.in/product/weact-studio-stm32h723vgt6-h723vg-lcd-core-demo-board/
- 

**Libraries:** https://github.com/STMicroelectronics/STM32CubeH7
**Type-C on STM32:** https://community.st.com/t5/stm32-mcus-products/stm32h7-and-usb-c-schematics/td-p/714872
Reddit:  [i heard that the h7 are complex to layout/work with](https://www.reddit.com/r/stm32/comments/m6d1ik/stm32h743_schematic/)
- complex if more complex peripherals used
- configure the chip (init code with the .ioc file) with CubeMX or CubeIDE using their GUI. This is not a simple atmega or even a basic STM32F4. It is much more complex, there is thousands of registers to properly set before the chip even run (The generated init C code is about 2000 lines long...). You should do this before having the board made to make sure that the configuration you want is possible.
- Make sure you set the SupplySource register properly

## Related Projects: 

**Essenceia (Schematics-Gerber in KiCAD):** https://github.com/Essenceia/stm32h750-dev-board

gemini chat
https://www.google.com/search?q=does+AK4454VN+support+SAI%3F&sca_esv=faa806e7e2c2d086&sxsrf=AE3TifMJ3qAQ-2sXLeJMnT-juBizkcxICg%3A1755344718975&ei=Tm-gaKCqO4eYseMP7vGVoQc&ved=2ahUKEwia6-L1oI-PAxVlRmcHHd-rBTUQ0NsOegQIJBAA&uact=5&sclient=gws-wiz-serp&udm=50&fbs=AIIjpHxU7SXXniUZfeShr2fp4giZ1Y6MJ25_tmWITc7uy4KIeoJTKjrFjVxydQWqI2NcOhZVmrJB8DQUK5IzxA2fZbQFrCfZ7DsBw9Vv9Qkv56j2ABF6GkElgaAKyV1xfCXdD_Z15iUVM79T-3xuh1Mj0Peon1PsRAzBxUHExQsK-PeRBwEUDFNzv6TVMSc_t6Cu-NsjQEv7GPCiyb7Qk1pVovxa3C3L_w&aep=10&ntc=1&mtid=tW-gaKKRA5eqseMPnfnboAQ&mstk=AUtExfDZPnsVzgb3q7rN0n7kGhbBvI0awJO48l5KinEmOggvRXAxmuNgHrU3zfYjI1qAYrO5vjv0DobE69q9yGtVUzi5ttvra8AbA2Q-JwNVVQoOp-nIXoEemkJbwDm_bACTycLmchMVlB_O9AxRAlbBpOCSTZHFqpu-t1KXPaDaj6gd5PhXDN7958XH-9zQwd14VoUtSiuB2ZWl8EoMDGexeik5xaYkZTSIYrCwD1XScGtSbt8Bx1MrbAfmTR0c-tmlSpOYUMkzOq-oDs98zUKj2OQ_iG9BWqRhQqvndiYM5fg4CBbf9QO0ruDon662vUpbBTJiOqKSC0L8GQ&csuir=1