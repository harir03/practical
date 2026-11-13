

# practical
 Viva ke liye short notes:

1. FPGA vs CPLD: FPGA mein LUTs + flip-flops se complex circuits bante hain. CPLD traditionally macrocells use karta hai, smaller control logic ke liye. Configuration volatile hai ya nahi, device par depend karta hai.

2. 8051 ports: P0-P3, har port 8-bit. P0 ko normal I/O mein external pull-ups chahiye; external memory ke liye address/data bhi carry karta hai. P2 high address; P3 serial/interrupt functions.

3. RISC vs CISC: RISC load/store aur relatively simple instructions par focus karta hai; CISC richer instructions par. ARM vs x86 examples. RISC ka matlab har instruction single-cycle nahi.

4. Verilog modeling: Structural = gates/modules connect; dataflow = assign expressions; behavioral = always/initial blocks; switch-level = transistor primitives.

5. Net vs variable: wire jaise nets driven connections represent karte hain; reg jaise variables procedural assignments ki value rakhte hain.

6. wire vs reg: wire continuous assign/module output se drive ho sakta hai. reg always/initial mein assign hota hai. Naam reg hai toh flip-flop banega, zaroori nahi.

7. Serial communication: Data bits sequence mein transfer hote hain. UART asynchronous; SPI/I2C synchronous examples.

8. UART: Start bit → data → optional parity → stop bit. Separate clock line nahi; baud rate compatible hona chahiye. TX doosre device ke RX se.

9. SPI: SCLK, MOSI, MISO, chip-select. Clocked communication; separate data lines se full-duplex transfer possible.

10. SD card: Microcontroller SPI mode se card read/write kar sakta hai. FAT filesystem files/data logging ke liye use ho sakta hai.

11. LPC2148 vs 8051: LPC2148 = 32-bit ARM7-based MCU, built-in ADC aur peripherals. Classic 8051 = 8-bit MCU; architecture/peripherals alag.

12. Counters: Synchronous mein sab flip-flops ko same clock. Ripple counter mein ek FF ka output next ko clock karta hai. Up/down/mod-N/ring/Johnson variants hain.

13. ADC: Analog voltage ko digital number banata hai. LPC2148 mein 10-bit ADC; classic 8051 ke saath external ADC0804/0808 interface kar sakte hain.

14. Applications: MCU se sensor reading, motor/LED control, alarms aur data logging. Device choice required speed, memory aur peripherals par.

15. Harvard vs Von Neumann: Harvard mein program/data ke separate memory paths; Von Neumann mein shared memory/path concept. Classic 8051 ke code/data address spaces separate hain.

16. Von Neumann bottleneck: Shared instruction/data transfer path throughput limit kar sakta hai.
Verilog + FPGA:

17. ALU: A/B operands + operation-select → arithmetic/logic result. Diagram: A,B → ALU ← Select; ALU → Result. Flags design ke hisaab se optional.

18. MUX: Multiple inputs mein se ek select karke output deta hai. 4:1 MUX mein 4 inputs aur 2 select bits.

19. Combinational vs sequential: Combinational output current inputs par; sequential output stored state par bhi depend karta hai.

20. Flip-flops: D data store karta hai, T toggle karta hai; SR set/reset, JK hold/set/reset/toggle support karta hai.

21. Sync vs async: Reset synchronous ho toh clock edge par apply; asynchronous ho toh edge ka wait nahi. Counter ke context mein same-clock vs ripple distinction hai.

22. JK truth table: JK=00 hold, 01 reset, 10 set, 11 toggle. Clock-triggered operation.

23. SR truth table: Active-high SR ke liye 00 hold, 01 reset, 10 set, 11 forbidden. Active-low version ki table different hoti hai.

24. ALU wala important correction: TERE alu.txt mein A/B 4-bit hain, Sel 3-bit hai. Isliye 8 operations: ADD, SUB, AND, OR, XOR, NOT, left/right shift. Generally '3-bit ALU' operand width batata hai, automatically 8 operations nahi.

25. Switch-level modeling: nmos/pmos jaise primitives se transistor-level circuit describe karna.

26. GPIO: General-purpose input/output pin. Input se switch/sensor read; output se LED/device control.

27. FPGA family: README mein Artix-7 likha hai. Exact chip/board part number unclear hai; guess nahi karna.

28. .v file: Verilog source file, design module ya simulation testbench dono ho sakte hain.

29. FPGA flow: Verilog → synthesis → implementation/place & route → bitstream → board program. .bit final configuration file hai.

30. Clock frequency: Har second clock cycles, unit Hz. Period T=1/f; 100 MHz ka period 10 ns. Apne board ka actual clock number alag verify karna.

31. Verilog vs VHDL: Dono hardware-description languages. Verilog C-like syntax; VHDL strongly typed aur generally more verbose.




Family lo artic 7 
General purpose in/out
5 axilix 236-1


[ChatGPT oral practice](https://chatgpt.com/share/6af66611-0c10-83ee-b13c-f3b425ded99b)

[Practical procedure](https://chatgpt.com/share/6af66c6a-70a8-83ec-9c36-e10384da2229)