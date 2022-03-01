# Hardware Setup

Follow these instructions to build your own self driving car.  After you've finished, move on to the [Software Setup](docs/Software_Setup.md).

## Tools

* Phillips screwdriver set
* Hex screwdriver
* Soldering iron
* Drill with 3mm and 6mm drill bits
* Pliers
* Wire strippers
* Acrylic sheet cutter
* Hot air gun (heat gun)


## Phase 1 - Car disassembly 
### Step 1 - Remove shroud from car



<img src="../images/car body removed.jpeg" width="400" >



1. Remove the car shroud.

2. Remove the old esc and battery strap. Desolder the two esc wire which are connected to the motor.

3. Remove the old steering servo. 



### Step 2 - Solder new ESC and fit new Servo motor




<img src="../images/esc solder1.jpeg" width="400" >




1. Solder red (motor out) wire from esc to motor's positive terminal.
 
2. Solder black (motor out) wire from esc to motor's negative terminal.
 
3. Attch the new servo motor in place of old servo motor (make sure to center the servo while attcahing the servo horn).






## Phase 2 - Base-plate/Camera mount
### Step 1 - Base-plate assembly & attaching the components


<a></a>
<img src="../images/main base plate1.jpeg" width="437" >
<img src="../images/completed mounting.jpg" width="500" >



1. Cut acrylic base-plate using acrylic cutter. Base-plate should be slightly bigger than the car.

2. Drill all necessary holes for mounting the components & 4 holes for attaching base plate to the car.

3. Attach all the components on top of the base plate using standoff. 
 


### Step 2 - Camera mount




<img src="../images/camera mount.jpeg" width="500" >



1. Using acrylic cutter cut a piece of acrylic roughly 5cm in width and 20cm in length.

2. Heat the acrylic cutout and bend the top 5cm to a point where, camera points towards the ground.
 
3. Also bend 4cm of the bottom end. This bend should be right angle. This will help us place and stick camera mount to the base-plate.    

4. Align camera mount at the center of the base plate and stick it to the very front of the base-plate. Use very little super glue for this.  

5. Design can be subjective and you can make any design.






## Phase 3 - Car wiring
### Basic wiring diagram & connections


<img src="../images/circuit diagram.jpg" width="1000" >


1. Connect battery to esc as well as to the ubec/stepdown controller.
 
2. Connect ubec/stepdown controller +ve and -ve wires to the jetson nano's 5v pin and gnd pin respectively.
 
3. Connect gnd pin of servo controller to jetson nano's gnd pin.
 
4. Connect VCC pin of servo controller to jetson nano's 3.3V pin.
 
5. Connect SCL pin of servo controller to jetson nano's SCL pin.
 
6. Connect SDA pin of servo controller to jetson nano's SDA pin.
 
7. Connect 3 pin servo cable to the pin 0 of servo controller.
 
8. Connect 3 pin esc cable to the pin 1 of servo controller.
 
9. Connect camera cable to the jetson nano (you can use any one of the two provided connectors on jetson nano).
 
10. Make sure ground is common in the entire circuit.

11. You can also add a switch beetween battery and ubec/stepdown controller/esc.
 
12. With this, wiring is completed.





## Phase 4 - Attaching base plate to the chasis/Final build
### Attaching base plate to the chasis





<img src="../images/assembly 1.jpg" width="500" >


1. Using 4 long standoff attached to the base-plate earlier, mark points on the chasis where these standoffs will be attached.  

2. Drill all these holes and attach the base-plate to the chasis using 4 M3 bolts.

3. Battery can be mounted on the car chasis, so make sure you drill holes accordingly.




### Final build



<a></a>
<img src="../images/finished car.jpeg" width="475" >
<img src="../images/finished car 2.jpg" width="500" >



* After following the above steps your robot should look something like this.




## Next

Next, follow the [Software Setup](docs/Software_Setup.md).

