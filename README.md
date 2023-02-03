# Add Open Data from Hydro-Quebec

Add production or consummation of electricity from Hydro-Québec to Home Assistant.
The production is updating every hour and the consummation, every 15 minutes.

But, the gap between the value and the real time can be 2 hours for the production and half a hour for the consummation.
For a more realistic graph, you can use the Apex Charts Card to set a table with a correction for this gap.
https://github.com/RomRider/apexcharts-card

![alt text](https://github.com/djiesr/Hydro-Quebec_Open_Data/blob/main/apexcharts.png?raw=true)

## Instructions

Copy the yaml file with your other package file.

If you didn't configure package file, follow these steps.


1. Add these lines in your configuration.yaml. If you already have a line "homeassistant:", just copy the package line.

homeassistant: <BR>
packages: !include_dir_named packages/
  
2. Download or copy the hq_open_data.yaml file in your "HA"/config/packages/ folder.
3. Reboot HA
4. All sensor start by "Hydro-Québec Demande" or "Hydro-Québec Production"

![alt text](https://github.com/djiesr/Hydro-Quebec_Open_Data/blob/main/hqcode.png?raw=true)
