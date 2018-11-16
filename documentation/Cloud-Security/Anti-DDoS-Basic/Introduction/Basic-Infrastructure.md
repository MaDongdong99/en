# Basic Architecture

    The Anti-DDoS Basic architecture consists of three modules: management center equipment, detection equipment and cleaning equipment.
    
## Business Architecture

The Anti-DDoS Basic business structure is shown in the following figure:

![Create Instance](https://github.com/jdcloudcom/cn/blob/Anti-DDoS/image/Basic%20Anti-DDos/Infrastructure01.png)

Note: </br>
      1. The image flow to the detection device </br>
      2. The detection device detects an attack, and notifies the management center of the attack information.</br>
      3. After receiving the attack information, the management center shall notify the cleaning equipment to open and clean.</br>
      4. Drain the flow to the cleaning equipment for traffic cleaning and re-inject clean flow after cleaning.</br>
      5. Normal flow</br>

|Name|Description|
| - | - |
|Management Center|Mainly responsible for receiving attack information and sending a cleaning strategy to the cleaning equipment to guide the cleaning equipment to carry out traffic cleaning.
| Cleaning Equipment | Mainly responsible for washing the flow of attack based on the cleaning strategy issued by the management center, and re-injecting the cleaned clean flow.
|Detection Device|Mainly repsonsible for analyzing the traffic components to determine if an attack occurred, and sending attack information to that management centre, if an attack occurs.

## Related Reference

- [What is Anti-DDoS Basic](Product-Overview.md)
- [Core Concepts](Core-Concepts.md)
- [Application Scenarios](Application-Scenarios.md)
- [Features](Features.md)
- [Restrictions](Restrictions.md)
