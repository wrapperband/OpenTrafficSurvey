#Open Traffic Survey
**Methodology for analysing the Traffic data with the citizen traffic survey spreadsheet**

**Fields of the spreadsheet**

*Information fields for the Spreadsheet.*

Lines 4, 5 and 6 of the spreadsheet store the identification data for the survey and total and average information collated from the subsequent analysis columns

**On the Template sheet**

Cell 4E  - Address of Traffic Survey Rd

Input the Address and postcode of the position the video of traffic was taken

Cell 5E & 5F - Distance  25yards

Measured distance travelled by the vehicles entering and leaving the analysis box.

Cell 6E 6F - Video - 2016-01-09-1-15.00-1.avi

Name of the Traffic Flow Evidence video that is being analysed

Cell E7 - Time

Time the analysis was initiated.

Cell E7 - Date 

Date the analysis was initiated.

*Example collated average and totals / information for the full period of the Traffic Analysis*

Vehicles Per Hour	306.00
Average Speed MPH	29.17
MaxSpeed MPH	51.14
MinSpeed MPH	12.78
Traffic Flow VPH Max	592.11
Traffic Flow VPH  Min	71.54
MaxDistanceBetweenVehicles	0.00
MinDistanceBetweenVehicles	0.00
Traffic Flow VPH Avg	733.24
AvgStoppingDistance	24.61
MaxStoppingDistance	60.63
MinStoppingDistance	5.44
AvgDistanceBetweenVehicles Yds	88.83

**Columns of the spreadsheet**

Start Frame	End frame
0          	
14         	21
239	        259

At Cell C8 is where you input data into the spreadsheet. The template is set up to input data for 25yards survey at 5 frames per minute. Even so the figures rapidly increase in value, so cutting the frame number (Cntr-C) from the frame number box in Avidemux and pasting it into the spreadsheet, saves time and prevents errors.

*Note : It important to mark each vehicle "as it enters the Box".*   

Care needs to be taken when vehicles are arriving in the box, to input them in order into the spreadsheet. On the video, one vehicle arrives from left, you must input the arrival frame and exit frame of that vehicle, whilst noting to go back, because another vehicle was behind it or arriving from the other direction....


Frames	Accurate Time (secs)
7	1.40
20	4.00
8	1.60
9	1.80

The next two columns, frames and Time, are calculated from the input data, the number of frames it took the vehicle's bonnet to enter the 25 yards, to when it's bonnet exits the 25 yards measurement box. Care must be taken, however it can soon be seen that an error of 1 frame at 5 frames per second, does not actually effect the required accuracy of results.


0 = Left to Right
0
1
0
0
0


The left right column holds the information on which direction the traffic is travelling. 

The spreadsheet currently averages data from left and right for some "insight" into instantaneous. In order to do that each event is also noted a 0 left to right and 1 right to left. This leaves the possibility that the data can be split and analysed in one direction later, but doesn't add the confusion of using separate sheets, for left and right traffic.

The current sheet is an example sheet set up for 25yards and 5 frames per second video. However, as the sheet is being generalised from a real sheet it is recommended you study how the calculations were done and wither they fit your case. An alternative sheet  to reduce the work, but quickly show flow levels is "in development" ie it is a cut down version of the current sheet.

