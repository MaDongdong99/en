## Billing Rules<br>
<table>
     <tr align="center">
        <th width="300">Product Name</th>
        <th width="300">Charging Item</th>
     </tr>
      <tr>
         <td rowspan="3" align="center">Stream Hub</td>
         <td>Number of Read/Write</td>
      </tr>
      <tr>
         <td>Throughput</td>
      </tr>
      <tr>
         <td>Storage Time</td>
      </tr>
</table>

<br>

**Noun Explanation**<br>
Number of Read/Write: <br>
The billing unit of the data stream is calculated with a payload of 64KB, and is charged per million records. For example, a 5KB message is charged according to one record, and a 90KB message is charged according to two records<br>
<br>
Throughput: <br>
Each unit of throughput supports a capability of up to 1MB/s write and 2MB/s read, or read/write processing capability of 1000 messages/s write and 2000 messages read\<br>
<br>
Storage Time: <br>
The storage time of the data in the Stream Hub is 1 day by default, with a maximum storage time of 7 days<br>
<br>

## Arrears Rules

* When your Stream Hub service fails to charge for your bill of the previous day, you will be considered to be arrears. <br>
* The data bus service will be automatically stopped immediately after the arrears, and the charge will be stopped. <br>
* If you repay the amount owed within 15 days after the arrears, the service will automatically open and you can continue to use it; if the amount owed has not been repaid for more than 15 days, you will be deemed to have voluntarily given up the Stream Hub service. After the service is stopped, unprocessed message data will be automatically released and the released data will be unrecoverable. <br>
