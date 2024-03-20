This page was written based on:
[What is CAN Bus & How to use CAN Interface with ESP32 and Arduino - CIRCUITSTATE Electronics](https://www.circuitstate.com/tutorials/what-is-can-bus-how-to-use-can-interface-with-esp32-and-arduino/)

CAN stands for Controller Area Network, and it’s widely used in the automotive industry due to its safety and reliability. CAN have a shared bus in which distributed CAN Nodes communicate through without a “master device”.

### CAN Bus Topology

![[Pasted image 20231103103527.png]]

The bus is a differential pair of wires, twisted to prevent EMI. If both wires are distorted by the same degree, it does not affect the CAN signals. Each end of the bus includes terminating resistors of 120 ohms to prevent signal reflections.

### CAN Message Arbitration

Each CAN node has an ID, and it will transmit its ID first whenever a CAN node sends a message. One important thing in CAN protocol is that 0 bit overpowers a 1 bit. Assume there are two nodes trying to access the bus. They both will start by transmitting their IDs. Since a 0 bit overpowers a 1 bit, the CAN node with a lower ID will always overpower the node with a higher ID. (the lower the ID, the higher the priority).

![[Pasted image 20231102142333.png]]

Let’s say there are two nodes: Node 15 and 16. They initiate transmitting, and their ID will start to be different by the time they get to bit 4. Since node 15 has a lower ID on bit4 than node 16, it will overpower node 16.

Every node can _try_ to transmit onto the bus, but they only will be able to when they win the CAN message arbitration. Upon successful transmission of a node, it can read the message that it has transmitted, and that’s one way to check if that node won the CAN message arbitration.

### CAN Signal

![[Pasted image 20231102141730.png]]

In the physical layer, CAN is consisted of two wires: CAN-High and CAN-Low. The voltage difference between the determines the bit. If there is a voltage difference of 2V between CAN-High and CAN-Low, it becomes a dominant voltage which yield bit 0. On the other hand the bit is 1 if there is a little or no difference a.k.a recessive voltage.


### Remote Transmission Request (RTR)

RTR is a mechanism within the CAN protocol that allows a node on the network to request data from another node. Here's how it works:

1. **RTR Flag**: A specific bit in the CAN frame, known as the RTR bit, indicates whether the frame is a data frame or a remote frame. A dominant (0) RTR bit signifies a data frame, which contains data to be transmitted. A recessive (1) RTR bit indicates a remote frame, which is a request for data.
    
2. **Data Request**: When a node needs data from another node, it sends a remote frame with the RTR bit set to recessive. This frame includes the identifier of the data it is requesting but does not contain any data payload itself.