# User Stories and Acceptance Criteria

We divided by user we want to analyze. The format followed for this was:
- User Story: “As a [persona], I [want to], [so that].”
    - Acceptance Criteria
        - [Objective Criteria that could be tested later]

## Victim
- "As a victim of a flood, I want to be able to communicate with a rescue team even if the conventional communitacion infrastructure is damaged, in order to ask for help and be rescued"
    - Acceptance Criteria:
        - the victim's smartphone must be able to communicate, using our app, with a drone that is close enough.

- "As a victim of a natural disaster, I want to send a message to my emergency contact and also to the emergency services, so that they can assistant me as soon as possible"
    - Acceptance Criteria
        - Using MySQL we can create data bases where we can collect the emergency services around the world
        - Using MySQL we can create data bases where we can collect the emergency contact of the users

## Network Administrator
- "As a network administrator, I want drones to communicate with themselves and the cloud, to provide real time information to rescue"
    - Acceptance Criteria:
        - The drones will communicate with themselves via mininet wifi.
        - Real time means that they will try to exchange messages every 10 seconds.
        - The drones must communicate when other drones are in their range.
        - At least a drone or a central must have access to the internet.

## Drone
- "As a drone, I want to communicate the message to the central, in order to rescue the victim"
    - Acceptance Criteria:
        - The drone must communicate itself or to another drone via MQTT with cloud service


## Team Leader
 - "As a rescue team leader, I want to receive information about the distribution of positions and the severity of the situation of the survivors, in order to manage the rescue team optimally."
    - Acceptance Criteria:
        - The message received by the central of rescue must present information about the position, and the severity of the situation of the victim depicted in a map. 

## Rescue Team Operator
 - "As a rescue team operator, I want to receive information about the position, severity, and description of the situation of a target survivor, in order to be prepared to accomplish the operation successfully."
    - Acceptance Criteria:
        - The message received by the central of rescue must present information about the position, the severity of the situation of the victim, and the description of the situation for each victim. 


## Mayor
 - "As the mayor of the city in which the flood happened, I want to have a database with information about the disaster in order to make political actions to avoid the bad effects of future disasters that may happen."
    - Acceptance Criteria:
        - The information received by each victim must be stored in a database and may be retrieved in the future.

## Crisis Management Center Operator
 - "As a crisis management center operator, I want to receive information about the survivors in order to organize this information and send it to other interested stakeholders, like the rescue team or the mayor of the city." 
    - Acceptance Criteria:
        - The information that is received by the crisis management center must be in a format that makes it easier to be stored in a database, or handled for visualization by other actors. 
        - The format of the message must be universal like JSON.

- User Story: As an crisis management center operator, I want to map out the zones of less risk of flooding, so that the government can site refuges there
    - Acceptance Criteria
        - Using Mosquitto and SIG´s we can found the zones of less risk
        - Using Mosquitto we can map that zone and send this to the government 

## Resident of the region of flood
- User story: As a Resident of the region of flood, I want a device that can monitor me when if I am in the risk zone, so that I can be protected by the emergency services
    - Acceptance criteria
        - Need to create a dashboard in order to help the decision