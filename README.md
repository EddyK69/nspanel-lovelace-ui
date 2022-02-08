# NSPanel Lovelance UI
This is a custom UI for the NSPanel, with HomeAssistant Lovelance UI Design.

The general idea is that the Nextion Display cycles though a page counter and the esp32 tells the display what to do.
If you are changeing the page the nextion display will send and event to the esp32 and it has to answer with the messages, that will update the current page with it's desired components. This enables easy changes, without touching the HMI Project.

# How to install

## Install Nextion Tasmota Berry Driver

Create and edit new file named autoexec.be with a line load("nextion.be") and upload nextion.be from tasmota folder of this repo.

or

Upload "nextion.be" from tasmota folder of this repository and rename to "autoexec.be"

## Setup Node-Red Flow

Import the example node-red flow from "node-red-example-flow.json" file and adjust to your needs.

# Screens from UI

The following screenshots are from the custom NSPanel UI that will be displayed on NSPanel.

![screen_cardEntities](doc-pics/screen_cardEntities.png)
![screen_popupLight](doc-pics/screen_popupLight.png)
![screen_popupShutter](doc-pics/screen_cardEntities.png)
![screen_cardThermo](doc-pics/screen_cardThermo.png)


# Message Flow

HomeAssistant / NodeRed -- MQTT -- Tasmota -- Nextion Screen

See the following picture to get an Idea for the messages send and recived from the screen during cycling though pages.

![image](https://user-images.githubusercontent.com/29555657/153079843-8d1eb5ab-059a-444e-a4da-008edc425606.png)


# Custom Protocol

See Readme in HMI Folder for more details on HMI Project / Custom Protocol
