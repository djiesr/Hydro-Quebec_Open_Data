# Add Open Data from Hydro-Quebec

Add production or consummation of electricity from Hydro-Québec to Home Assistant.
The production is updating every hour and the consummation, every 15 minutes.

## Instructions

Copy the hq_open_data.yaml file with your other package file.

If you didn't configure packages file before, follow these steps:

1. Add these lines in your configuration.yaml. If you already have a line "homeassistant:", just copy the "packages" line.

> homeassistant: <BR>
> &nbsp;&nbsp;packages: !include_dir_named packages/
  
2. Create the "packages" folder in your "config" folder in Home Assistant.    
2. Download or copy the hq_open_data.yaml file in your "HA"/config/packages/ folder.
3. Reboot HA
4. All sensor start by "Hydro-Québec Demande" or "Hydro-Québec Production"
  
![image](https://user-images.githubusercontent.com/31359825/216670708-8f10c75a-950f-4f8e-86b8-76322bf1350f.png)

But the gap between the value and the real time can be 2 hours for the production and half a hour for the consummation.
For an more realistic graph, you can use the Apex Charts Card to set a table with a correction for this gap.
https://github.com/RomRider/apexcharts-card

Paste the content of apexcharts.yaml in a empty card of your dashboard.

![image](https://user-images.githubusercontent.com/31359825/216670487-d964d539-a2d7-4c67-b0df-c38698cc6bd2.png)

