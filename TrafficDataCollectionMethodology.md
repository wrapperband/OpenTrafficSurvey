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

I used a Logitech camera, and powered USB extension to allow the camera to be place high in a ground floor window, or in an upper room window looking down at the road.
By installing Ubuntu it was possible to collect data using an old, low powered Netbook. Then those videos were transfered via wireless to a WD network storage device. This also allowed short videos where there is no power, on battery. 

For a high rate of traffic, i.e. greater than 300 vehicles an hour, this would be about 10 minutes, for manual analysis.  However, I would advise recording for a full hour if possible, for each 5 or 10 minute close analysis period. This gives the possibility of post or historical analysis should extra evidence be required, for instance to prove the inaccuracy of Vehicle Speed surveys being used to estimate vehicle flow rates.

To identify when a vehicles is entering or leaving the "Analysis Box" it is not necessary to take high resolution video, 640 x 480 is fine.  

It is advisable to keep additional video evidence for later analysis, if necessary.  

**Measuring the distance travelled**

Using the yardstick (I manufactured one from a extendible plastic mop/broom handle), measure the distance on the pavement of the street being monitored. I was able to measure 25yards from one side of the video image to the other.  

Use one point, say bonnet, on the car to decide when it crosses 2 imaginary lines across the road. It is important to take the angle of viewing into account. For instance, in the test case, different 25 yards were used for left right traffic. the left to right being on the far lane appears before the right left leaves, due to the angle of the camera. Sometimes the first 25 yards is obscured, so that vehicle was measure from when the boot crossed instead ...  

**Measuring the time for a vehicle to travel a set distance**

The video can now be analysed using a video editor such as Avidemux.  

As each vehicle enters the frame, the spreadsheet is updated with the frame number from the video.  As each vehicle leaves the (25yard) frame, the spreadsheet is updated with the frame number from the video and a direction indicator field is set to 0 for left right traffic and 1 for right left.

Various lengths and frame rates were tested, it was possible to get accurate results, with a reasonable "calculated" error level with 25 yards measurement and a 5 frames per second video.  

**Ensuring correct frame rate index**

Sometimes using cheep cameras or open software to record long periods of video the AVI files can loose their index. However, it is possible to re-index the files using ffmpeg.

Commands for using ffmpeg (Linux terminal)  to repair AVI video files index.

ffmpeg -i 2016-09-24-4.avi -c copy 2016-09-24-4-reindexed.avi   

Note : The re-indexed video file will not retain the original file date and time, so it is important to retain the original video.


