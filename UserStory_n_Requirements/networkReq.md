# Network related user stories and acceptance criterias/requirements

- "As a victim of the flood, I want to comunicate with anybody, in order to be rescued"
    - Acceptance Criteria:
        - As described in the project, usually communication in flood is lost, in order to communicate victim must have a phone with wifi.
        - The phone for instant must have the app that we're going to develop.
        - The app must communicate via MQTT protocol to the drone via mininet wifi.
        - The drone must communicate via mininet wifi with other drones and the central of rescue.
        - The central of rescue must be on a place with access to internet.
        - The central of rescue will send a message via internet to the cloud.
        - The arrived at the cloud must report the request from the victim.