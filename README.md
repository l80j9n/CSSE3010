java c
Embedded Systems Design and Interfacing
CSSE3010   Stage   2
RGB   LED   Colour   Control
1            Assessment
•    Git   and   Work   Diagrams   due   3pm   Monday   in   week   5   .
•    Demo   marked   in   your   lab   session   in   week   5   .
•    Course   Marks:   7.5%
2            Resources
•   Nucleo   platform.	
•   LTA1000G   LED   Bar
•   MultiFunctional   Shield   (MFS)
•   RGB   LED   Module
•    SN74HC03N   NAND   gate
•   Logic   Analyser
•   Logic   Probe
3          Academic   IntegrityAll assessments are individual.   You should feel   free to   discuss   aspects   of   C   programming   and   assessment specifications with fellow students   and   discuss   the   related   APIs   in   general   terms.   You should not actively help   (or seek help from) other students with the actual coding of   your assessment.   It   is   cheating to   look   at   another   student’s   code,   and   it   is   cheating to   allow your code   to   be   seen   or   shared   in   printed   or   electronic   form.   You   should   note   that   all   submitted   code will be subject to automated checks for plagiarism and collusion.    If   we detect plagiarism   or collusion   (outside of the base code given   to   everyone),   formal   misconduct   proceedings   will   be initiated against you.   If   you’re having trouble, seek help from a teaching staff member.   Do   not   be   tempted   to   copy   another   student’s   code.   You   should   read   and   understand   the   state-   mentson student misconduct in the course profile and on the school website
3.1          Use   of   AI   ToolsAll   assessment   tasks   evaluate   students’   abilities,   skills   and   knowledge   without   the   aid   of   generative   Artificial   Intelligence   (AI)   or   Machine   Translation   (MT).   Students   are   advised that   the   use   of   AI   technologies   to    develop   responses    (e.g.       code    generation)    is    strictly   prohibited   and   may   constitute   student   misconduct   under   the   Student   Code   of   Conduct.
4          Structure
Your   final   stage   code   must   be   titled   main   . c   and   saved   in   your   s2       folder.   PATH:   csse3010/repo/s2
Listed   below   are   the   required   mylib   libraries,   that   you   will   need   to   develop   for   this   stage.   They   should   be   saved   in   your mylib   folder.
PATH:   csse3010/repo/mylib.
•   MFS   Trimpot   Library
•   MFS   Pushbutton   Library
•   RGB   LED   Library
•   LTA1000G   Library
5            IntroductionThis   stage   will   introduce   the   Timer,   Pulse   Width   Modulation   and   Analog   to   Digital   Con-   verter   (ADC)   Peripherals   of   the   Nucleo   platform.   You   will   use   the   RGB   LED,   SN74HC03N   NAND   gate,   LED   Bar,   and   MFS   Trimpot.
6          Preparation
It   is   recommended   that   you   attempt   the   following   labs   first   before   starting   this   stage.   The   labs   or   lab   quizzes   are   not   assessed.
•    Lab   2.4,   2.5,   2.6,   2.7   -   Analog,   Timers,   PWM
•   Lab   3.1,   3.4   -   RGB   LED,   Logic   Analyser,   MFS
•   Lab   1.5   -   Flow   Charts
6.1          Black   Board   Quiz
The   Blackboard   quiz   contains   helpful   questions   related   to   this   stage.   It   must   be   completed   and   submitted   on   BlackBoard.
7            Design   Tasks
Control   the   colour   and   brightness   of   an   RGB   LED,   using   the   MFS   pushbutton   and   trimpot.   Also,   display   the   current   brightness   on   the   LTA1000G   LED   bar.
7.1          Work   Diagram   TasksFollow   the   work   diagram   guidelines   on   Blackboard.   You   need   to   use   the   hardware   and   flow   chart templates.   You   must   draw the   hardware   schematic   for this   stage.   You   must   draw   and   submit   the   flow   chart   for   the   ‘sxxxxxxx   reg   rgb   brightness   write‘   function. No   other   flow charts   are   to   be   submitted. You   are   encouraged   to   draw   flow   charts   for   the   other   mylib   register   functions.   State   diagrams   are   not   used   for this   stage.   The   work   diagram task   is   due   in   week   5   ,   on   Black   Board.
7.1.1          Timing   DiagramYou   must   use   the   waveform   template   (from   Black   Board)   to   show   the   signals   listed   below.   The   signals   must   be   captured   using   the   logic   analyzer   (e.g.   screenshot).   You   must   show   at   least   5   RGB   colour   changes.
1.    RGB   Brightness   Signal   (PWM)
2.    RGB   Red,   Green,   and   Blue   Signals
3.    SYSMON   CHAN0   signal.   See   Table 5.
4.    SYSMON   CHAN1   signal.   See   Table 5.
7.1.2          mylib   SetupYou MUST FOLLOW the Template Code given in the sourcelib/templates/mylib   folder.   Your mylib code must meet the guidelines specified   in   the   mylib   and   plat-   form   build   guides   on   Blackboard.    You   MUST   create   the   right   file   structure   in   the   mylib   git   folder.
You   will   create   mylib   Register   library   files   to   control   the   RGB   LED   module.      For   details,   refer   to   the   mylib   RGB   register   specifications   on   Blackboard.
7.2          Design   Task   1:   RGB   LED   Control   Circuit
Create   a   circuit   using   the   SN74HC03N   NAND   gate   to   control   the   colour   and   brightness   of   the   RGB   LED.   Note:   the   RGB   LED   V   signal   must   be   connected   to   the   breadboard   power   supply   line   (Vcc)   and   should   not   be   controlled. GPIO   pins   must   be   used   to   control   the 代 写CSSE3010 - Embedded Systems Design and Interfacing Stage 2R
代做程序编程语言  colour   of the   RGB   LED,   using   the   SN74HC03N   NAND   gate. A   PWM   signal   must   be   used   to   control   the   brightness   of   the   RGB   LED.
7.2.1          Logic   Analyzer   Test   PointsYour   circuit   must   include   the   logic   analyser   test   points   (see   lab   3.1)   for   the   RGB   LED.   All   RGB   LED    (red,   green,   blue)   and   brightness   control   signals   must   be   viewed   on   the   logic   analyzer.      The   RGB   LED   pins   must   be   vertically   inserted   into   the   breadboard.      The   test   points   for   the   logic   analyser   must   be   used   to   view   the   RGB   signals.   The   logic   analyser   test   points   must   be   drawn   on   the   hardware   schematic.DO   NOT   cut   any   wires   for   the   breadboard.    Use   male-to-male   jumper   wires.    Spare   jumper wires   are   available   in   the   lab.   Do   not   use   any   of the   wire   spools   (cutters).   Do   not   use   other   breadboard   wires   (e.g.   breadboard   wires   used   in   CSSE2010).
See   section 9   for   the   pins   used.
7.3          Design   Task   2:      RGB   LED   Control   using   the   MFS   Trimpot   and   PushbuttonUse   the   MFS   trimpot   to   control   the   colour   of   the   RGB   LED. Each   complete   turn   of   the   MFS trimpot   must   change   the   RGB   colour   to   the   next   colour   in   the   sequence.   When   the   end   of   the   sequence   is   reached,   the   sequence   should   wrap   around   to   the   start   of the   sequence.   The   sequence   of colours   can   be   seen   in   table 1   and   table 2.   Note   the   initial   colour   is   Black   (off),   before the   first   MFS   trimpot   turn.
Table   1:    Colour   sequence
Sequence
Colour
1
Red
2
Green
3
Blue
4
Cyan
5
Magenta
6
Yellow
7
White
8
Black   (off)
Table   2:   RGB   Primary   Colour   Table
Colour
RGB   Value
Black
0x07
Blue
0x06
Green
0x05
Cyan
0x04
Red
0x03
Magenta
0x02
Yellow
0x01
White
0x00Use   the   MFS   S1   to   control   the   RGB   brightness.      This   involves   controlling   the   brightness   of   the   red,   green,   and   blue   LEDs   of   the   RGB   LED.   Each   time   the   MFS   S1   is   pressed,   the   brightness   must   increase   by   10%   (of   the   duty   cycle).      The   initial   brightness   must   be   0%.   After   10   presses,   the   brightness   must   reset   back   to   0%.
The RGB brightness must be controlled with a PWM signal,   using   the   parameters   in   table   3.   Hint:    use   the   logic   analyzer   to   check   the   PWM   waveform.	
Table   3:    PWM   Brightness   Control   Signal   Parameters
Parameter
Value
Frequency
100Hz
Maximum   Pulse Width
5ms
Minimum   Pulse Width
0ms7.4          Design   Task   3:   RGB   LED   Brightness   Display   using   LTA1000G
LED   BarUse the LTA1000G LED Bar to display   the   brightness   level   (0%   to   100%))   of the   RGB   LED.   Each   LED   segment   represents   a   brightness   level   increase   of   10%.      Only   one   LED   segment   should   be   on   for   a   non-zero   brightness   level).   See   Table 4.
Table   4:    LED   Bar   Segment   Assignment
Segment
RGB   LED   Brightness
0
10%
1
20%
2
30%
3
40%
4
50%
5
60%
6
70%
7
80%
8
90%
9
100%You   will   need   to   use   the   sxxxxxxx   reg   rgb   brightness   read()   function.   You   must   use   your   mfs   pusbhutton,   mfs      trimpot,   rgb   and   LTA1000G   register   mylib   drivers.      See   section 9   for   the   LED   Bar   connections.
Refer   to   gpio/gpio   and   pwm/dynamic   examples.
7.5          Design   Task   4:    TestingYou   must   add   the   following   test   signal   outputs   using   the   system   monitor   (SYSMON).   You   can   view   the   test   signals   using   a   logic   probe,   logic   analyser,   or   oscilloscope   (only   available   in   the   lab).    You   must   use   the   SYSMONCHAN   functions   to   initialise   and   manipulate   the SYSMONCHAN   pins.    You   should   not   create   any   extra   mylib   functions   or   files   relating   to the   system   monitor   .
Table   5:    Test   SignalsSYSMONCHAN
Function
SYSMONCHAN0
Must   toggle   every   time   the   RGB   Brightness   is   changed.
SYSMONCHAN1
Must   toggle   every   time   the   RGB   colour   is   changed.
SYSMONCHAN2
Not   used.    (Can   be   used   for   debugging,   if required)
See   section 9   for   the   board   pins   used   for   the   SYSMONCHAN   signals.   Refer   to   the   getting-started/sysmon.      example
8          Integration
All   design   tasks   should   be   combined   into   the   same   main   . c   file   and   should   function   without   reprograming   the   board   for   each   design   task.
9          Pin   Assignments
NOTE:   The   pins   listed   here   are   Board   Pins   only.   You   must   map   them   to   the   Processor   Pins   using   the   Nucleo   Pinout   for   your   board.
9.1          Nucleo-F429
Board   Pins
Notes
CN11   Connector   pins   62,   64,   66,   68,   70
Connect   to   LED   Bar   pins   0   to   4.
CN12   Connector   pins   62,   64,   66,   68,   70
Connect   to   LED   Bar   pins   5   to   9.
C9   PIN   A0
MFS   Trimpot   Input
C9   PIN   A1
MFS   S1   Pushbutton
CN12   PIN   52
RGB   Brightness   Control
CN12   PIN   56
RGB   Red
CN12   PIN   50
RGB   Green
CN12   PIN   60
RGB   Blue







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
