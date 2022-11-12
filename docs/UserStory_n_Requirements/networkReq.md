# Network related user stories and acceptance criterias/requirements

- "As a victim of a flood, I want to be able to communicate with a rescue team even if the conventional communitacion infrastructure is damaged, in order to ask for help and be rescued"
    - Acceptance Criteria:
        - the victim's smartphone must be able to communicate, using our app, with a drone that is close enough.
        - The drones must create a network that makes it possible for the message sent by the victim to reach the internet.
        - The network formed by drones must be resilient. Even if some of the drones fail, the network may be able to work properly.
        - The app must communicate via MQTT protocol to the drone via mininet wifi.
        - The drone must communicate via mininet wifi with other drones and the central of rescue.
        - The central of rescue must be on a place with access to internet.
        - The central of rescue will send a message via internet to the cloud.
        - The arrived at the cloud must report the request from the victim.

 - "As a rescue team leader, I want to receive information about the distribution of positions and the severity of the situation of the survivors, in order to manage the rescue team optimally."
    - Acceptance Criteria:
        - The message received by the central of rescue must present information about the position, and the severity of the situation of the victim depicted in a map. 


 - "As a rescue team operator, I want to receive information about the position, severity, and description of the situation of a target survivor, in order to be prepared to accomplish the operation successfully."
    - Acceptance Criteria:
        - The message received by the central of rescue must present information about the position, the severity of the situation of the victim, and the description of the situation for each victim. 

 - "As the mayor of the city in which the flood happened, I want to have a database with information about the disaster in order to make political actions to avoid the bad effects of future disasters that may happen."
    - Acceptance Criteria:
        - The information received by each victim must be stored in a database and may be retrieved in the future.

 - "As a crisis management center operator, I want to receive information about the survivors in order to organize this information and send it to other interested stakeholders, like the rescue team or the mayor of the city." 
    - Acceptance Criteria:
        - The information that is received by the crisis management center must be in a format that makes it easier to be stored in a database, or handled for visualization by other actors. 
        - The format of the message must be universal like JSON. 
