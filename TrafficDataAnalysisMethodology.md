#Open Traffic Survey
**Methodology for analysing the Traffic data with the citizen traffic survey spreadsheet**

**Fields of the spreadsheet**

**Information fields for the Spreadsheet.**

Lines 4, 5 and 6 of the spreadsheet store the identification data for the survey and total and average information collated from the subsequent analysis columns

**On the Template sheet**

Cell 4E  - Address of Traffic Survey location 

Input the Address and postcode of the position the video of traffic was taken

Cell 5E & 5F - Distance  25yards

Measured distance travelled by the vehicles entering and leaving the analysis box.

Cell 6E 6F - Video - 2016-01-09-1-15.00-1.avi

Name of the Traffic Flow Evidence video that is being analysed

Cell E7 - Time

Time the analysis was initiated.

Cell E7 - Date 

Date the analysis was initiated.

**Example collated average and totals / information for the full period of the Traffic Analysis**

Description of Calculation | Example Value
-------------------------- | -------------
Vehicles Per Hour   |	306.00  
Average Speed MPH   |	29.17  
MaxSpeed MPH   |	51.14  
MinSpeed MPH   |	12.78  
Traffic Flow VPH Max   |	592.11  
Traffic Flow VPH Min   |	71.54  
MaxDistanceBetweenVehicles   |	0.00  
MinDistanceBetweenVehicles   |	0.00  
Traffic Flow VPH Avg   |	733.24  
AvgStoppingDistance   |	24.61  
MaxStoppingDistance   |	60.63  
MinStoppingDistance   |	5.44  
AvgDistanceBetweenVehicles Yds   |	88.83  

**Columns of the spreadsheet**

**Input the video frame number for each vehicle entering and leaving the measurement "box"**

Start Frame |   End frame
----------- |   ---------
0          |      
14         |    21  
239	   |    259  

At Cell C8 is where you input data into the spreadsheet. The template is set up to input data for 25yards survey at 5 frames per minute. Even so the figures rapidly increase in value, so cutting the frame number (Cntr-C) from the frame number box in Avidemux and pasting it into the spreadsheet, saves time and prevents errors.

*Note : It important to mark each vehicle "as it enters the Box".*   

Care needs to be taken when vehicles are arriving in the box, to input them in order into the spreadsheet. On the video, one vehicle arrives from left, you must input the arrival frame and exit frame of that vehicle, whilst noting to go back, because another vehicle was behind it or arriving from the other direction....

**Calculating the time to Traverse the measurement "Box"**

Frames	|    Accurate Time (secs)
------- |   ---------------------
7	| 1.40  
20	| 4.00  
8	| 1.60  
9	| 1.80  
  
The next two columns, frames and Time, are calculated from the input data, the number of frames it took the vehicle's bonnet to enter the 25 yards, to when it's bonnet exits the 25 yards measurement box. Care must be taken, however it can soon be seen that an error of 1 frame at 5 frames per second, does not actually effect the required accuracy of results.  

**Vehicle direction**  

0 = Left to Right   |  
-----------------  |  
0   | 
1   |  
0   |  
0   |  
0   |  
  

The "left right" column holds the information on which direction the traffic is travelling.   

The spreadsheet currently averages data from left and right for some "insight" into instantaneous.   

0 = Entered from Left  
1 = Entered from Right  

In order to do that each event is also noted a 0 left to right and 1 right to left. This leaves the possibility that the data can be split and analysed in one direction later, but doesn't add the confusion of using separate sheets, for left and right traffic.  

**Method for dividing the traffic into left and right**

In the test case the traffic was  evenly divided in each direction. It was possible to total the in each direction, for each data set. The method is show in cell G62, was to sum the 1s in the left / right direction column G, then take this value from the total number of vehicles. 

Into Town R to L =SUM(G10:G60)
Out of Town L to R ==((COUNT(G10:G60)-G62))

In order to produce separate charts for each direction, 

First make a copy of the data sheet.

Use the sort facilty (menu / data sort), to sort all the columns in order of Column G primary and  with C as secondary. 

The charts can be copied and the new ranges set for each direction. It will be necessary to delete a couple of the last 5 vehicles calculations, to compensate for less vehicles in each side, after the split.  

*Note : Using the Template sheet, setting the ranges of your data.*

Some of the calculations require the setting of ranges, or start and end of cell positions, to count the vehicles, or find the maximum. It is usual to check each calculated column, updating the start and end position accordingly. Then copy the corrected cell down all the cells of the column. 

You can use the shift key highlight a block of cells then past the new equation into the whole column.

*Note : Using the template sheet for your case*

The current sheet is an example sheet set up for 25yards and 5 frames per second video. However, as the sheet is being generalised from a real sheet it is recommended you study how the calculations were done and wither they fit your case. An alternative sheet  to reduce the work, but quickly show flow levels is "in development" i.e it is just a cut down version of the current spreadsheet.  

**Vehicle speed and error calculations**  
  
Err – 1 Frame	| Vehicle Speed MPH over 25yds	|  Err + 1 Frame  
-------------   | ----------------------------  |  -------------
42.61   |   36.53   |   31.96  
13.46   |   12.78   |   12.18  

The vehicle speed is calculated from the exact time, calculated from the number of frames the vehicle took to traverse the 25 yards of the measurement distance. The error is calculated for 1 frame when a video frame rate of 5 frames per second is used. The system was tested and has to be converted from 24 frames per second, where even using a 5 frame error the video method was accurate.  


**Calculating the percentage errors the sample survey case above :**  

*The error at normal vehicle speeds*  

36.53 - 31.96 = 4.57   gives an error of (4.57 / 36.53) * 100 = 12 %  maximum error in speed  
42.6 - 36.53 = 6.07    gives an error of (6.07 / 36.53) * 100 = 17 %  maximum error  

*The error for slow speed vehicles*  

12.78 - 12.18 = 0.6  which gives a lower maximum error of  (0.6 / 12.78) * 100 = 4.7 %  maximum error  
13.46 - 12.78 = 0.68 which gives a  maximum error of       (0.68 / 12.78) * 100 = 5.32%  maximum error  

In which case the error was calculated for 5 frames was in fact the same as one frame at 5 frames/sec. if the additional accuracy and storage space no object the error can by reduced by a fifth by using 25 frames a second or greater video frame rates.  
  

**Vehicles flow rate per hour and per last 5 vehicles**  
  
Vehicles Per Hour (Each  last 5 cars)   |   Vehicles Per Hour (10 minutes Sample) 
-------------------------------------   |   -------------------------------------
        |                                306.00  
        |                                306.00  
        |                                306.00  
        |                                306.00  
        |                                306.00  
165.14	|                                306.00  
166.36	|                                306.00  
260.12	|                                306.00  
  

Vehicles per hour is calculated by totalling the vehicles for the sample period in this case 10 mins. This is then multiplied by how many times the sampling period fits into one hour. In the example case there are 6 10minutes in One Hour.  

Vehicles per hour last 5 cars, calculates the time for 5 cars to pass, then the time for one car to pass is 1/5th of that. Dividing the time for one car into one hour gives the number of cars per hour, for the last 5 cars.  

The vehicles per hour calculation could be extended to 10 vehicles, that would damp further the indication of peak traffic levels as traffic bunches which the smaller sample gives. Ideally it should be for each 2 vehicles, to measure absolute "bunching" factor.  

Note : the calculation cannot start till five vehicles have passed, which is why the first 5 fields of Vehicles per hour (last 5 vehicles) are empty.  

It is noted that it would be possible to calibrate pollution levels to the instantaneous or "5 car average" flow rates, these being much higher when vehicles are "bunched".  

**Calculating the distance between vehicles**

Distance between Vehicles Error – 1 frames  |   Distance between vehicles (yds) avg last 5 Vehicles |   Distance between Vehicles Error + 1 frames
------------------------------------------  |   --------------------------------------------------- |   ------------------------------------------
 	| |
60.12   |   57.62   |   55.31


Distance between the vehicles is estimated from speed of the vehicles, and how far that would have travelled in the time for the 5 vehicles to pass. There is an add complication of averaging left and right hand traffic in the example sheet. However, the average is re-calculated for every vehicle which shows the assumptions are reasonable in the test case where traffic was evenly balanced left to right.  

It is noted that a method of splitting the left and right sheets for some results would be advantageous, or a more advanced sheet to get over that problem / extra work, some other way.  

**Safe stopping distance calculations**

Safe Stop Distance For Speed -Yds   |   Safe Stop Distance For Speed – F    |   Distance between vehicles (yds) min last 5 Vehicles  
---------------------------------   |   --------------------------------    |   ---------------------------------------------------
34.41   |   103.23  |   
6.99    |   20.96   |   
27.68   |  83.03   |  
22.92   |  68.76   |  
27.68   |  83.03   |  
5.44   |  16.33   |  11.52  


Safe stop distance uses the speed reading and the standard speed v. stopping distance equation to generate the safe stop distance for that vehicle (dry conditions).   

After 5 vehicles pass it is then possible calculate or extract the min, max or average distance between cars. As there are various causes of bunching and sometimes vehicles stop to allow passing the spreadsheet includes the Average distance.  

**Example of a simple simulation 2 x traffic level**

Vehicles per Hour – with Twice / X times  the Trafiic   |   Vehicles Per Hour (Each last 5 cars) – With Simulated Traffic  
-----------------------------------------------------   |   -------------------------------------------------------------
612.00  |	 
612.00  |	 
612.00  |	


**Example of more complex Traffic Simulations methods**

For the test case it was calculated that extra traffic between 8:15 and 9:00 would more than triple the level of traffic at that time. In this case a copy of the data sheet was made and 2 extra vehicles were added "automatically" using a simulation equations in Columns A and B to find the time of the two vehicles between each set of vehicles.
The simulation isnt included as it will be site specific.


Time between Simulated Vehicles – Minutes   |   Calculated Frames  Between Vehicles	|    Start Frame |   End frame
-----------------------------------------   |   -----------------------------------  |  -----------    |   ---------
	|  |	| 0.00	
0.0467	|    |   14.00	|    21.00
0.2967	|    75.00	| 89.00   |   96.00
0.5467	|    75.00	| 164.00	|    171.00
0.7967	|    |	239.00    |	259.00
0.8089	|    3.67    |	242.67    |	262.67
0.8211	|    3.67    |	246.33    |	266.33


The new arrival times are calculated with =(C13-C10)/3 in Cell B11  and =(C13-C10)/3 in B12.  

The new start frame and end frame is the previous vehicle + the new time between vehicles, = C10+B11, the end frame =D10+B11.   

Cell A shows the time in minutes between vehicles =C10/(60*5) , shows the time each vehicle arrives and confirms the length of the simulation.  

**Charts from the input and calculated traffic Data available in the template spreadsheet**

Sheet 1 is called Data input and Calculations.  
Sheet 2 contains the speed charts with errors.  
Sheet 3 covers vehicle overall and short term flow rates.  
Sheet 4 shows separation of vehicles compared to safe stopping distance for the vehicle speeds.  




