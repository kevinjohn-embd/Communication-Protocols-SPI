# Communication-Protocols-SPI
Learning and exploring SPI

## Briefing
+ Serial Peripheral Interface
+ Synchronous (Clock based)
+ Full-Duplex; Main <--> Slave (Subnode)
+ 4 signals - CLK, /CS (Chip Select), MOSI (Main Out, Slave In), MISO (Main In, Slave Out)

## Clock 
(refer to the timing diagram below for clarity in CPOL and CPHA)

+ Main controls clock using CPOL (Clock Polarity; chooses idle state 1/0) and CPHA (Clock Phase; decides sampling instant) bits.
+ CPOL 0 (clock is LOW when idle) & CPOL 1 (clock is HIGH in idle state)
+ CPHA 0 (sampling of data on first clock edge) & CPHA 1 (sampling of data on 2nd edge)

![SPI](https://github.com/user-attachments/assets/5a0dbcb6-0dd2-4c5a-94a6-ed3ddb38ab5a) - SPI Modes Timing diagram 

# | Mode | CPOL | CPHA | First Edge       | Sampling Instant | Data Change     |
  | 0    | 0    | 0    | Rising           | Rising           | Falling         |
  | 1    | 0    | 1    | Rising           | Falling          | Rising          |
  | 2    | 1    | 0    | Falling          | Falling          | Rising          |
  | 3    | 1    | 1    | Falling          | Rising           | Falling         |

  
