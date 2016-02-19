#Open Traffic Survey
**Methodology for automating a citizen traffic survey**

**Hardware Set-up**

USB digital camera or other video camera

Computer to analyse data

1 yard stick, chalk or charcoal temporary marker.

**Software Requirement**

Avidemux video editor

Libre Office Spreadsheet software


**Open Traffic Survey - Methodology**  

Position the camera at a suitable place to video record the traffic, preferably side on.  
  
Should the positioning be restrictive a wide angle lens can be used to increase the analysis distance travelled by the vehicles.  

**Record video of the traffic.**  

*Where to place the camera*  

I used a Logitech camera, and powered USB extension to allow the camera to be place high in a ground floor window, or in an upper room window looking down at the road.

*How to storing images from remote locations.*   

It was possible to collect data using a Low powered 7 portable Netbook  by installing Ubuntu and open source software. The videos were transferred via wireless to a WD network storage device. This also allowed sample videos from positions with no power by using battery.   

*How long do the videos need to be?*  

For a high rate of traffic, i.e. greater than 300 vehicles an hour, this would be about 10 minutes. This will need manual analysis, which takes effort.  Analysis of the test case shows a number of 30 minute videos, of which, One or more is analysed. This would give a good indication of the scale & type of traffic "problem". It would also stores the video evidence.

To identify when a vehicles is entering or leaving the "Analysis Box" it is not necessary to take high resolution video.

*Note : A Video resolution of 640 x 480 is fine.  The low resolution files are smaller, enabling easy storage of longer sample times.*   

It is advisable to keep additional video evidence for later analysis, if necessary.  Generally, store an hour, then analyse the first 5 minutes. This allows evidence of the accuracy of the method, should it be required to be confirmed at a later date.

It is important to copy files to an analysis area. The original copy of the file will retain the most accurate time data. It becomes difficult to accurately judge the time the videos were taken from the name. In the test case, the video name referred to time since directory was full, on the small data collection computer.    

**Measuring the distance travelled**  

Using the yardstick (I manufactured one from a extendible plastic mop/broom handle), measure the distance on the pavement of the street being monitored. I was able to measure 25 Yards from one side of the video image to the other and leave a 5 Yards+ room for error on each side.  

To decide when a vehicle crosses  : Use one point, say bonnet on a car to decide when it crosses 2 imaginary lines across the road. One each end of a measurement Box.  

It is important to take the angle of viewing into account. For instance, in the test case, different 25 yards were used for left right traffic. The left to right traffic being on the far lane from the camera appears before the right left leaves, due to the angle of the camera. Sometimes the first 25 yards is obscured, so that vehicle was measure from when the boot crossed instead ...  

**Measuring the time for a vehicle to travel a set distance**  

The video can now be analysed using a video editor such as Avidemux.  

As each vehicle enters the frame, the spreadsheet is updated with the frame number from the video.  As each vehicle leaves the (25yard) frame, the spreadsheet is updated with the frame number from the video and a direction indicator field is set to 0 for left right traffic and 1 for right left.   

Various lengths and frame rates were tested, it was possible to get accurate results, with a reasonable "calculated" error level with 25 yards measurement and a 5 frames per second video.  

**Ensuring correct frame rate index**

Sometimes using cheep cameras or open software to record long periods of video the AVI files can loose their index. However, it is possible to re-index the files using ffmpeg.

Commands for using ffmpeg (Linux terminal)  to repair AVI video files index.

ffmpeg -i 2016-09-24-4.avi -c copy 2016-09-24-4-reindexed.avi   

Note : The re-indexed video file will not retain the original file date and time, so it is important to retain the original video.


