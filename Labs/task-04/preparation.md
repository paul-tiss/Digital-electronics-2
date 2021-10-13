<a name="preparation"></a>
## Preparation tasks (done before the lab at home)

Consider an n-bit number that we increment based on the clock signal. If we reach its maximum value and try to increase it, the value will be reset. We call this state an **overflow**. The overflow time depends on the frequency of the clock signal, the number of bits, and on the prescaler value:

&nbsp;
![Timer overflow](Images/timer_overflow.png)
&nbsp;

1. Calculate the overflow times for three Timer/Counter modules that contain ATmega328P if CPU clock frequency is 16&nbsp;MHz. Complete the following table for given prescaler values. Note that, Timer/Counter2 is able to set 7 prescaler values, including 32 and 128 and other timers have only 5 prescaler values.

|   **Module**   | **Number of bits** | **1** | **8**  | **32** | **64**  | **128** | **256**  | **1024** |
| :------------: | :----------------: | :---: | :----: | :----: | :-----: | :-----: | :------: | :------: |
| Timer/Counter0 |         8          |  16u  |  128u  |   --   |  1024u  |   --    |  4096u   |  16384u  |
| Timer/Counter1 |         16         | 4096u | 32768u |   --   | 262144u |   --    | 1048776u | 4194304u |
| Timer/Counter2 |         8          |  16u  |  128u  |  512u  |  1024u  |  2048u  |  4096u   |  16384u  |

2. Shields are boards that can be attached to an Arduino board, significantly expand its capabilities, and makes prototyping much faster. See schematic of [Multi-function shield](../../Docs/arduino_shield.pdf) and find out the connection of four LEDs (D1, D2, D3, D4) and three push buttons (S1-A1, S2-A2, S3-A3).
D1 --> PB5[13]
D2 --> PB4[12]
D3 --> PB3[-11]
D4 --> PB2[-10] 
A1 --> PC1
A2 --> PC2
A3 --> PC3

