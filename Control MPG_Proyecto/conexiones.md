Mach3 Red handwheel 10 socket port:

             +5v | o   o | GND
               X | o   o | Y
             ACH | o   o | BCH
               Z | o   o | A
            X100 | o   o | X10
            
//Para MPG generico que se vende  https://www.youtube.com/watch?v=dtTE6CQRhdc
Standard MPG with ESTOP  Wire Colors:

(Red - Green/black) -- 5v
(Black - White/Black - Orange/Black) -- GND
(Yellow) -- X
(Yellow/Black) -- Y
(Green) -- A CH (Encoder)
(White) -- B Ch (Encoder)
(Brown) -- Z
(Brown/Black) -- A
(Orange) -- X100
(Gray/Black) -- X10
(Blue & Blue/Black) -- IN1 & DCM in BOB
_____________________________________________________
2- Config -- ports & pins -- Input signal:

OEM Trig#1 port -- 3 , pin -- 5
OEM Trig#2 port -- 3 , pin -- 6
OEM Trig#3 port -- 3 , pin -- 7
OEM Trig#4 port -- 3 , pin -- 8
OEM Trig#5 port -- 3 , pin -- 9
OEM Trig#6 port -- 3 , pin -- 10
_____________________________________________________
3- Config -- ports & pins -- Encoder/MPG's:

Encoder1 -- Enabled
MPG#1 -- Enabled
_____________________________________________________
4- Config -- System hotkeys:

Trigger 1 -- oem code 185 To select X axis
Trigger 2 -- oem code 186 To select y axis
Trigger 3 -- oem code 187 To select z axis
Trigger 4 -- oem code 188 To select a axis
Trigger 5 -- oem code 192 To select x10 jog step
Trigger 6 -- oem code 193 To select x100 jog step
_____________________________________________________
5- Config -- General Config... -- Jog Increments in cycle Mode:

Position1 -- 1
Position1 -- 10
Position1 -- 100
_____________________________________________________
6- Program Run Alt1 -- Tab key -- Jog  Mode MPG
_____________________________________________________
Notes:

0- Just use 5v pulse generator (encoder) , higher than this will damage your BOB.
1- Plugin control -- RnRMoton "MPG disable" must not selected
2- Check Encoder in Setting Alt6 -- MPG Diagnstic -- MPG1 ,by rotating encoder you can see count and velocity ; just by settings in step 3, you can check encoder test
3- In Program Run Alt1 -- Tab key -- Jog  Mode MPG, you can see selected axis and jog step
4- to select axis and jog step you must push side key
5- Default jog step is 1 for encoder without pressing side key , pressing side key equal to selected jog step
6- To calibrate your MPG: Function Cfg's -- Calibration of MPG's
7- Do not forget to save any changes in Config -- save settings..
8- If all things work ok but you have problems with the encoder only (if it is not working) , check your board microchip, It must be STM32 series. most other chips not working.