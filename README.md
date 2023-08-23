# ECE306_PROJ7
a car that follows a circle made out of black electrical tape

NC State University ECE 306
ECE Department Introduction to Embedded Systems Jim Carlson
Project 7
See course website for due date.

Overall Project Goal:
The plan is to create a car that can follow a black electrical tape line after navigating via a Wi-Fi 
connection. The creation of the car is broken into ten projects. 

The first project is building the battery power system. Verification will be performed using Either 
Analog Discovery or other Lab test equipment.

The second project is the installation of the LCD onto the Control Board and the material to attach 
it to the FRAM board. Demo your working LCD with the Project 2 code. 

The third project is the creation of the car with the Forward only part of the H-bridge control for 
the wheels. Successful verification will be movement of the car and appropriate car labeling.

The fourth project is the controlled movement of the car with the forward only part of the H-bridge 
control for the wheels. Successful verification will be of the car moving in predetermined shapes 
within a 24” x 21.5” area. This is made with 6 sheets overlapped by ½ inch in 2 rows of 3 sheets.

The fifth project is adding full control of the H-Bridge allowing the vehicle to travel forward and 
reverse. Verification will be with timed travel forward followed by timed travel in reverse; ending 
with spinning motion.

The sixth project is the addition of the emitter / detector circuit that will detect the black line, and 
the code to resolve the Thumbwheel to a digital value to verify ADC configuration. Verification 
will be manual display of ADC values as your vehicle transitions from white to black and black to 
white, independent tracking of the Thumbwheel. Your vehicle must travel from inside the 16-inch 
Diameter circle and stop when it detects the circle. After circle detection, your car must turn and 
be detecting the black line.

The seventh project will be adding traveling around the circle twice and an exit into the middle of 
the circle after two times around.

Project 7 Details:
The seventh project is the use of both Thumb Wheel and the Emitter / Detector circuit to detect 
and provide the guidance to follow the black line. Verification will be by adding the timed travel 
around the detected circle from Project 6; a 16-inch circular black line. Once detected and car 
rotated as from Project 6, the vehicle must travel around the circle twice.

In Project 6, you added the Thumb Wheel, Detectors and Emitter hardware and code. The Thumb 
Wheel aids in debugging ADC code, and you should now be able to identify when you are on or 
off the black line. In Project 7, the Emitter and Detectors will be used to follow the Black Line
circle. Once intercepted, your vehicle must follow the black line circle traveling around the circle 
twice. Direction is your preference. Upon finishing the traveling around the circle twice have your 
car automatically turn into the circle center and stop.

Hardware:
You may need to bend and change the orientation / angle of the detectors to improve performance.
How are you going to orient your emitter / detectors? Will ambient light affect operation? This 
aspect is totally up to you on how you will mount your IR LED/detectors to get it to work. You 
may need straws or shields to help isolate the emitter and detectors; again, you will need to figure 
this out for your own car. The height, angle, etc. may all play into operation of your vehicle. 
The oscilloscopes in the lab, or your Analog Discovery will be of help if you need them.

Software:
You may use any part of the previous code that you have developed. No magic numbers allowed. 
A random sampling of a file will occur by the TA. 

Start with the software from Project 6. Use the display to provide feedback to what your software 
is doing or about to do; display the ADC values.

Make sure you can turn on and off the emitter. Do not leave it on all the time as it will discharge 
your batteries. The emitter will barely glow red when on, and is easily detected on many cell phone 
cameras that do not have an IR filter. 

Debug the detectors while using USB power. Use your Black Electrical tape on a blank piece of 
plain white copy paper. Some students have found it advantageous to create a square made from 
black tape and make sure their car can move back and forth staying inside the square. Use this to 
see the change between detection of the line and detection of the white paper. You may find it 
convenient to manually move your vehicle and leave your motors disconnected so that accidental 
drives off the desk do not occur.

Think about the emitter as being a small flash light. The closer to the paper, the more focused will 
be the bounce of light back up toward the detectors. Focus the detectors on the spot that the emitter 
is illuminating. You will not be able to see the spot, but you should be able to estimate where it is. 
The light from the Emitter controls the values in the detectors; Left half for left Detector and Right 
have for the Right Detector. Just pointing the detector to the emitter is NOT optimum.
You should have a calibration mode to identify the ambient light condition, as the readings will be 
greatly affected if you are inside, outside, or in front of a device that emits a lot of IR [like sunlight 
through windows]. Do this by taking readings of the IR conditions from the detectors when the 
emitter is off. Then turn the emitter on and take readings from the ADC when on white paper and 
then when on a black line. Use Electrical tape to create the black line. You will need to be able to 
display all three values. Your code should use the current readings and calculate the best threshold 
for black to gray and gray to white. Black transition to gray is best.
The best way to control is to know what a black line value is when your detector is right over the 
black line. Slowly move away and see how rapidly it changes. Small changes are more important 
than large changes.

You will place your vehicle into the center of the circle; move forward, intercept the circle; turn
and travel around the circle twice; end with a turn into the circle and stop. Prior to starting in the 
center of the circle, calibrate your vehicle to the white area, the black line and ambient conditions.
Your vehicle placed inside a black lined circle should:

1 Travel forward until detection of the black line, as with Project 6.
2 Make the turn [either direction] as with Project 6.
3 Travel around the circle twice.
4 Turn your vehicle into the circle center and stop.
The display should identify the state of the motion, Intercepting, Waiting, Turning, Circling, 
Stopped. In addition, a 0.2 second clock must be displayed on the screen to display time up to 
999.8 seconds. It will only be updated with the display, so it will be updated every 200msec.
Stop updating the timer when your car stops.
NC State University ECE 306
ECE Department Introduction to Embedded Systems Jim Carlson
Demonstration Procedure:
Arrange a time through the message board to demonstrate your system to a TA. Make sure 
you have the TA sign your grade sheet. The TA’s will have specifics to look for in each 
write-up. These will be discussed in class.
Grading Scale for Project 7:
Demo 100%
Item Description Points
 1 Code inspection of Intercept function 10
 2 Black Calibration Mode 10
 3 White Calibration Mode 10
 4 Vehicle can Travel forward until Black Line Intercept 10
 5 Vehicle can stop near / on Black Line 10
 6 Vehicle can turn and follow Black Line 10
 7 Vehicle can travel around twice 20
-5 if it takes longer than 5 minutes per circle
-10 if it takes longer than 10 minutes per circle
-15 if it takes longer than 15 minutes per circle
[ Time is from display. No time display -20]
 8 Vehicle turns into circle center 10
 9 Display shows relevant information 10
100
