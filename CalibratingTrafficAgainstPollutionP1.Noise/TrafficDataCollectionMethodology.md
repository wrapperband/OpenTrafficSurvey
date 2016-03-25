#Open Traffic Survey
**Data collection Methodology for automating a citizen traffic survey : Test site example survey**

#Calibrating Road Traffic to Pollution : Part 1 : Noise  

#Data Collection   

**Equipment :**

DAWE 1405D Sound Pressure Level Meter - dBA meter BS 5962 Type 2  
DAWE D-1411E BS Pistonphone noise calibrator  
Maplin Sound Level Meter N33GJ dBC meter  
  CE    Measurement Range : 40 - 130 dBC +/- 3.5 dBC @ 1KHz 94dB  
  Frequency Range  31.5 - 8 KHz  
Model 8926 Analog Sound level meter dBA +/- 3.0dBA
IEC 651 Type 2 noise meter with Leq capability  +/- 1.0dB
Logitech USB cameras C920  
Fuji finepix S2000HD Camera   
Powered USB Hub  
Kubuntu  
Avidemux-qt  
Guvcview  
Libre Office Spreadsheet  
1 yard stick   
chalk or charcoal temporary marker  


**Open Traffic Survey - Methodology : Collecting the data**  

**Hardware Set-up**

**Where to place the camera**  

Position the camera at a suitable place to video record the traffic, preferably side on.  

Care needs to be taken with USB cameras, the length of cable is restricted in most cameras. One way to get over this problem is to use a cheep camera with a Laptop.  This means the camera can be placed higher up, to look down on the traffic.  

The other way over this problem is to use the Logitech C920, which compresses the video to MPEG on-board in the camera, so can transmit HD over a slightly longer USB cable. In this case the powered USB was used to ensure enough power to the Camera.
  
In this case a suitable angle was available so an extra wide angle lens wasn't need. It was possible to measure 25 yards along the pavement. The camera was position at an angle so Out traffic travelling Left to Right, enter the box adjacent to the camera and leave 25 yards later. 

The reverse happens with incoming traffic, right to left, it enters 25 yards away and exits close to the camera.


**Record video of the traffic.**  

In this case the traffic samples were 5 minutes, taken in 3 surveys scheduled at different time of the day. Most surveys so far have been during the mid work day, so the three new surveys are mid and evening Weekend and Weekday rush hour.

Recorded to a PC with Kubuntu and used open source Guvcview software to save the video. 800 x 448 resolution gave the best wide screen accuracy of vehicle position but small file size. However, 640 x 480 would also have surfaced if storage space is tight.

A number of extra 5 minute Video samples were taken around the same time, in case further historical analysis is needed.

In addition to recording the traffic at 5 frames per second, in this case additional information was recorded at the same time. A second video camera recorded pollution levels, in this case Noise at 30 fps. These were then synchronized to start at the same point as the Traffic analysis video. 

In survey 01 the extra Noise data was recorded In and Out of the measurement box and a more detailed chart was produced with readings every couple of seconds to show the variation over time. In survey 03 the comparable noise levels were recorded with the traffic at the position closest to the camera for calibration purposes. 

The sound level meters were placed at a hight of 0.5 meters, adjacent to the level of vehicles or the the level one might sit in the garden, in this test case

![alt tag](charts/TrafficSurveyRecordingTheNoiseLevels.dBA.dBC.2016-03-07.jpg) 

**Measuring the distance travelled**  

Using the yardstick the distance on the pavement of the street being monitored was measure and 25 Yards from one side of the video image to the other, on the street.  In this case obvious markers such as the telephone box were used to mark the 25 yards, but chalk marks were used to help measure correctly.

Vehicles were recorded as they entered and left the box. As normal the start and end frames numbers were recorded, but also noise level measurements.

01 - Traffic Survey with detailed noise analysis using (fast averaging) dBC meter  
02 - Traffic Survey, test use of VMPH to noise calibration  
03 - Traffic Survey calibration dBC to dBA  

In the case of survey 01, dBC noise was recorded in and out. In survey 03 the noise was only recorded as vehicles were close to the camera, but value of dBC and dBA were taken.

The video can now be analysed using a video editor such as Avidemux.  

As each vehicle enters the frame, the spreadsheet is updated with the frame number from the video.  As each vehicle leaves the (25yard) frame, the spreadsheet is updated with the frame number from the video and a direction indicator field is set to 0 for left right traffic and 1 for right left.   

**Ensuring correct frame rate index**

Sometimes using cheep cameras or open software to record long periods of video the AVI files can go wrong, files can loose their index. 

However, it is possible to re-index the files using ffmpeg.

Commands for using ffmpeg (Linux terminal)  to repair AVI video files index.

ffmpeg -i 2016-09-24-4.avi -c copy 2016-09-24-4-re-indexed.avi   

**Noise Survey of the Test Site**

Analysis of the noise data gathered during the traffic to noise serioes of surveys of the test site showed that further detail of the level and type of noise generated by traffic would be usefull. It is always good practice to get more information at a baseline surevey for comparison later particularly when the research indicates a health issue (in increasing traffic further at the site).


Methodology of tests.

The Traffic generated Noise level tests were spilt into 3 main types.

**Maximum and minimum Noise Levels**

A model 8926 Analog Sound level meter set to dBA slow was used to capture High and low Noise levels for 15 minute periods at various times for a number of days. The time and levels were recorded.

An IEC 651 Type 2 noise meter with Leq capability was set on various Leq time settings at various times over a number of days. The Leq10 values meaning the valuse was recorded Leq 10 minute average. The time left to monitor the traffic being greater than the avereraging time being, for 10 minutes 15 minutes was averaged.

DAWE 1405D Set at 90 to 100 dBA range to manually capture maximum noise levels off the camera / cross instrument "calibration". 

**Noise levels over time**

A set of readings was planed at a sample period for each hour of the day. A comparison reading included for weekdays, where there are more and heavier traffic.

**Noise levels over geographical area**

A set of readings moving away from the road, to measure the travell of the traffic noise.

