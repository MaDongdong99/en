# Price Overview

## Bandwidth
<table>
<tr>
    <td>Billing Mode<br/>
    <td>Biling Ladder</td>
    <td>Price (CNY/Mbps/day)</td>
</tr>
<tr>
    <td rowspan="3"> Peak Bandwidth<br/>
    <td>0-512Mbps (included)</td>
    <td>1</td>
</tr>
<tr>
    <td>512Mbps-5Gbps (included)</td>
    <td>0.9</td>
</tr>
  <tr>
    <td>>5Gbps</td>
    <td>0.75</td>
</tr>
</table>

**Description:**    
1. The peak bandwidth consumed is billed per day. A bandwidth is counted per 5 minutes and 288 points are counted per day in total. For each billing, the maximum bandwidth (peak bandwidth) of the user in this billing period is billed as per the daily tier. If additional storage and calculation cost is produced by using transcode, snapshot and record functions, charges will be collected as per corresponding product price.  
2. By default, only the downlink play fees shall be charged. In case of any imbalance between the uplink and the downlink (uplink pushing streaming: downlink play >1:30), fees for uplink pushing streaming shall be charged, and the uplink billing price is the same as the downlink unit price.      
3. If your monthly consumption amount is more than RMB 100,000, you can use the monthly 95 bandwidth peak billing method provided by CDN.

## Traffic  
<table>
<tr>
    <td>Billing model<br/>
    <td>Unit Price (RMB/GB/Day)</td>
</tr>
<tr>
    <td> Cost of VOD Play Acceleration<br/>
    <td>0.15</td>
</tr>
</table>

**Description:**   
1. Live traffic will be deducted as per actual traffic consumed per day.
2. By default, only the downlink play fees shall be charged. In case of any imbalance between the uplink and the downlink (uplink pushing streaming: downlink play >1:30), fees for uplink pushing streaming shall be charged, and the uplink billing price is the same as the downlink unit price.        

## Live Transcode-Jingxiang Super Definition 
<table>
<tr>
    <td>Coding Mode<br/>
    <td>Resolution</td>
    <td>Price (RMB/Minute)<br><= 30fps output</td>
</tr>
<tr>
    <td rowspan="5">H.264<br/>
    <td>360P (640 x 360) (inclusive) and below </td>
    <td>0.01 </td>
</tr>
<tr>
    <td>360P(640 x 360) -720P(1280 x 720) (inclusive) </td>
    <td>0.03 </td>
</tr>
<tr>
    <td>720P(1280 x 720)-1080P(1920 x 1080) (inclusive) </td>
    <td>0.05 </td>
</tr>
<tr>
    <td>1080P(1920 x 1080) -2k(2560×1440) (inclusive) </td>
    <td>0.10 </td>
</tr>
<tr>
    <td>2k(2560×1440)-4k(3840×2160) (inclusive) </td>
    <td>0.20 </td>
</tr>        
<tr>
    <td rowspan="5">H.265<br/>
    <td>360P (640 x 360) (inclusive) and below </td>
    <td>0.10 </td>
</tr>
<tr>
    <td>360P( 640 x 360 ) -720P( 1280 x 720 ) (inclusive) </td>
    <td>0.15</td>
</tr>
<tr>
    <td>720P( 1280 x 720 )-1080P( 1920 x 1080 ) (inclusive) </td>
    <td>0.30</td>
</tr> 
<tr>
    <td>1080P(1920 x 1080) -2k(2560×1440) (inclusive) </td>
    <td>0.60 </td>
</tr>
<tr>
    <td>2k(2560×1440）-4k(3840×2160) (inclusive) </td>
    <td>1.20 </td>
</tr>     
<tr>
    <td>Encapsulation Conversion</td>
    <td>Rtmp, Hls and flv provide error detection </td>
    <td>FREE </td>
</tr>    
<tr>
    <td>Covert to audios</td>
    <td>AAC/MP3 Volume Optimization </td>
    <td>FREE </td>
</tr>      
</table>  

**Description:**    
1. Billing is based on encoding method, resolution of transcode request and duration of transcode output file, taking every day as billing period.  

## Live Snapshot
<table>
<tr>
    <td>Billing Type<br/>
    <td>Unit Price (RMB/1,000 Pieces)</td>
</tr>
<tr>
    <td>Key Frame Snapshot<br/>
    <td>0.1</td>
</tr>
</table>  

**Description:**    
1. Charges will be collected as per snapshot number actually produced by the customer with the snapshot function and will be settled by days.   

