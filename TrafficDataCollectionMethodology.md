#Open Traffic Survey
**Methodology for automating a citizen traffic survey**

**Hardware Set-up**

USB digital camera or other video camera

Computer to analyse data

1 yard stick

**Software Requirement**

Avidemux video editor

LibreOffice Spreadsheet software


**Open Traffic Survey - Methodology**  

Position the camera at a suitable place to video record the traffic, preferably side on.  
  
Should the positioning be restrictive a wide angle lens can be used to increase the analysis distance travelled by the vehicles.  
Record video of the traffic.  

For a high rate of traffic, i.e. greater than 300 vehicles an hour, this would be about 10 minutes, for manual analysis.  

It is not necessary to take high resolution video, 640 x 480 is fine to identify when a car is entering or leaving the analysis "box".  

It is advisable to keep additional video evidence for later analysis, if necessary.  

**Measuring the distance travelled**

Using the yardstick (I manufactured one from a extendible plastic mop/broom handle), measure the distance on the pavement of the street being monitored. I was able to measure 25yards from one side of the video image to the other.  

**Measuring the time for a vehicle to travel a set distance**

The video can now be analysed using a video editor such as Avidemux.  

As each vehicle enters the frame, the spreadsheet is updated with the frame number from the video.  As each vehicle leaves the (25yard) frame, the spreadsheet is updated with the frame number from the video and a direction indicator field is set to 0 for left right traffic and 1 for right left.

Various lengths and frame rates were tested, it was possible to get accurate results, with a reasonable "calculated" error level with 25 yards measurement and a 5 frames per second video.  


