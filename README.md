
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) 

# Prophet Algorithm using Decision Engine in DTNs

<p align="justify">
The Prophet algorithm is a probabilistic routing protocol designed for intermittently connected networks—networks where a fully connected path between source and destination might not always exist. In such networks, traditional routing methods fail because they rely on continuous paths. The Prophet algorithm solves this by using probabilities to decide the best path to deliver a message. It calculates a "delivery predictability" for each node, indicating how likely it is that a message will reach its destination through that node.
</p>

![image](https://github.com/user-attachments/assets/3463f2b0-7871-4b25-b056-412abdf5dbd9)

There are 3 propeties in this algorithm, such as:
- **Delivery Predictability**: Each node in the network stores a value that indicates how likely it is that it can deliver a message to a particular destination node. This value is updated every time two nodes meet, based on how often they met in the past. The more often they meet, the higher the probability of message delivery.
- **Aging** : If two nodes do not meet for a certain period of time, the delivery probability value between them will decrease. This reflects that nodes that meet infrequently may no longer be a good route to send messages.
- **Transitivity**: If Node A frequently encounters Node B, and Node B frequently encounters Node C, then Node A considers Node C as a good candidate for sending messages to Node B. In other words, if A frequently encounters B, and B frequently encounters C, then A may also be able to send messages to C through B.

# Forwarding Strategy
Messages are forwarded to nodes with higher delivery predictability, making it more likely that the message will reach its destination efficiently, even if the network is not fully connected.
This approach allows messages to be passed through the network, even with intermittent connectivity, by leveraging historical encounter data and probability to choose the best routes.








