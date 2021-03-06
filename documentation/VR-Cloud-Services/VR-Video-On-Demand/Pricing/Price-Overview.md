# Price Overview

## A. VR Video Storage  
### Charging Items  
Total Storage Usage of VR VOD Video  
### Billing Prices  
<table>
<tr>
    <td>Charge Items<br/>
    <td>Price (RMB/GB/day)</td>
</tr>
<tr>
    <td> Storage Capacity<br/>
    <td>0.003</td>
</tr>
</table>

### Billing Instructions
•	Payment method: Pay-As-You-Go.  
•	Billing rules: Charge is based on actual usage, which taking the daily bucket capacity peak as the billing value of the day.  
•	Billing period: Billing is based on day. The billing period is from 0:00 to 24:00. Settlement, bill output and deduction for cost generated on previous day will be conducted at 12:00 a.m. - 18:00 p.m. every day.  
•	Billing formula: Accumulated storage capacity (GB) * corresponding storage unit price.  
### Billing Instance
For example, if you used VR VOD service on June 18 and the file peak storage capacity was 100GB, then the cost you needed to pay for VR VOD storage on June 19 is shown as below:
Accumulated storage capacity (100GB) * corresponding tiered unit price (0.003) = RMB 0.3

## B. VR Video Transcoding
### Charging Items
Processing Duration of VR VOD Transcoding
### Billing Prices
<table>
<tr>
    <td>Coding Mode<br/>
    <td>Resolution</td>
    <td>Unit Price (RMB/minute)<= 30fps output</td>	
</tr>
<tr>
    <td> H.264<br/>
    <td>4K (3840 x 2160) or below</td>
    <td>0.2</td>	
</tr>
<tr>
    <td> H.264<br/>
    <td>2K (2560 x 1440) or below</td>
    <td>0.1</td>
</tr>
<tr>
    <td> H.264<br/>
    <td>Super Definition FHD (1920x1080) and below</td>
    <td>0.05</td>	
</tr>
<tr>
    <td> H.264<br/>
    <td>HD (1280 x 720) or below</td>
    <td>0.03</td>	
</tr>
<tr>
    <td> H.264<br/>
    <td>SD (640 x 360) or below</td>
    <td>0.01</td>	
</tr>
<tr>
    <td> H.265<br/>
    <td>4K (3840 x 2160) or below</td>
    <td>1.2</td>	
</tr>
<tr>
    <td> H.265<br/>
    <td>2K (2560 x 1440) or below</td>
    <td>0.6</td>	
</tr>
<tr>
    <td> H.265<br/>
    <td>Super Definition FHD (1920x1080) and below</td>
    <td>0.3</td>	
</tr>
<tr>
    <td> H.265<br/>
    <td>HD (1280 x 720) or below</td>
    <td>0.15</td>
</tr>
<tr>	
    <td> H.265<br/>
    <td>SD (640 x 360) or below</td>
    <td>0.1</td>
</tr>
<tr>
    <td> Encapsulation Conversion<br/>
    <td>mp4/flv/ts  Provide Error Detection</td>
    <td>free</td>
</tr>
</table>

### Billing Instructions
•	Payment Method: Pay-As-You-Go  
•	Billing rules: Billing is based on encoding method, resolution of transcoding request and duration of transcoding output file, taking every day as billing period.  
•	Billing period: Billing is based on day. The billing period is from 0:00 to 24:00. The billing time stamp of effective date is the completion time of transcoding task, e.g., transcoding is submitted at 23:00 on the day and completed at 0:05 on the next day, then it will be included in the billing period of next day. Settlement, bill output and deduction for cost generated on previous day will be conducted at 12:00 a.m. to 18:00 p.m. every day.  
•	Output duration: Billing of each transcoding output file is based on minute. The file duration is accurate to two decimal places, wherein the second digit is rounded off according to the third digit, and the duration less than 1 second is calculated as 0.02 minutes.  
•	Output specification determination: The long side and short side of the output VR video resolution are determined according to the range defined by the output specification, and the formula is shown as follows:  
Taking output specification of HD (1280 x 720) or below for example, the output VR video with its long side of resolution not greater than 1280 and that of short side not greater than 720 belongs to this output specification.
If the long side of the output VR video is greater than 1280 or the short side of the output VR video is greater than 720, this output VR video belongs to a higher output specification.  
•	Billing Formula:
Output file duration of VR video transcoding (minute) x transcoding unit price of different coding methods/resolutions for VR video (RMB/minute)
### Billing Instance
For example, if you used VR VOD transcode service on June 18 to transcode a video of 2560 x 1440 of resolution and 100 minutes of VR video duration by coding method of H.264, then the cost you needed to pay for transcoding on June 19 is shown as below:  
Output file duration of VR video transcoding (100 minutes) x transcoding unit price of different coding methods/resolutions for VR video (RMB 0.1/minute) = RMB 10
## c. VR VOD Video Acceleration
### Charging Items
Billing by traffic: Traffic generated by accelerating watching of VR VOD content distribution.
### Billing Prices
Traffic cost adopts non-tiered cost mode, which customers directly get discount price:
<table>
<tr>
    <td>Charge Items<br/>
    <td>Unit Price (RMB/GB/day)</td>
</tr>
<tr>
    <td> Cost of VR Video Play Acceleration<br/>
    <td>0.15</td>
</tr>
</table>

### Billing Instructions
•	Payment Method: Pay-As-You-Go  
•	Billing rules: Billing is based on downlink traffic generated by using content distribution network (CDN) acceleration when playing VR videos, taking every day as the billing period.  
•	Billing period: Billing is based on day, from 0:00 to 24:00 every day. Settlement, bill output and deduction for cost generated on previous day from 12:00 a.m. to 18:00 p.m. every day.  
•	Billing formula: Downlink traffic of VR video (GB) x tiered unit price of daily traffic (RMB/GB)
### Billing Instance
For example, if you used VR VOD acceleration service on June 18 and the downlink traffic used was 100GB, then the cost you needed to pay for VR VOD traffic on June 19 is shown as below:  
Downlink traffic of VR video (100 GB) x tiered unit price of daily traffic (RMB 0.15/GB) = RMB 15
