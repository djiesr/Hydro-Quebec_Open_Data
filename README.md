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
  
You can paste the "dashboard.yaml" content in a empty card of your dashboard for this result.
<img width="378" alt="image" src="https://user-images.githubusercontent.com/31359825/216863968-79cf5e81-05a3-4c84-aafc-86fcb512c205.png">

But the gap between the value and the real time can be 2 hours for the production and half a hour for the consummation.
For an more realistic graph, you can use the Apex Charts Card to set a table with a correction for this gap.
https://github.com/RomRider/apexcharts-card

After install apexcharts-card, you can paste the "apexcharts.yaml" content in a empty card of your dashboard for this result.
<img width="379" alt="image" src="https://user-images.githubusercontent.com/31359825/216863948-a3030e72-83e4-4832-97f8-f6372e48e57e.png">


