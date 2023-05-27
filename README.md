[![hacs][hacsbadge]][hacs]
![License](https://img.shields.io/github/license/alexgraupera/ha-eess-cheapest-prices.svg?style=for-the-badge)
![Release](https://img.shields.io/github/downloads/alexgraupera/ha-eess-cheapest-prices/latest/total?style=for-the-badge&color=f55041)

_Integration created with templates [integration_blueprint](https://github.com/ludeeus/integration_blueprint)._

# EESS Cheapest prices

This integration allow to create sensors for a given location (spain only) and show the best price for a fuel type and the station service details.

The locations (municipalities) and service stations are collected through the public rest service: https://sedeaplicaciones.minetur.gob.es/ServiciosRESTCarburantes/PreciosCarburantes/help

You can create multiple sensors for (by the moment) three fuel types (95, 98 and diesel) in a given location.

> ℹ️: This integration has been created for learn how to build a custom Home Assistant integration, to learn Python and its workflows, and also for fun.

# Installation

## Using [HACS](https://github.com/dolezsa/thermal_comfort#:~:text=Using-,HACS,-(recommended)) (Recomended)

This integration can be installed using HACS.

## Manual

- Using git:

```
git clone https://github.com/alexgraupera/ha-eess-cheapest-prices.git
cd thermal_comfort
# if you want a specific version checkout its tag
# e.g. git checkout 1.0.0

# replace $hacs_config_folder with your home assistant config folder path
cp -r custom_components $hacs_config_folder
````

- Manual: Download this repo, extract the `eess_cheapest_prices` into the custom_components folder of your HA installation

After doing this, remember that you need to restart HA before you can use it.

# Adding new sensors

Go to Configuration > Devices & Services > + Add integration.

Search by name "Cheapest fuel prices by location" and select.

Then select a location in drop down selector, select the fuel type and press "send".

If everything went well, the sensor have been created.


[releases-shield]: https://img.shields.io/github/downloads/alexgraupera/ha-eess-cheapest-prices/latest/total
[releases]: https://github.com/alexgraupera/ha-eess-cheapest-prices/releases
[hacs]: https://github.com/hacs/integration
[hacsbadge]: https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge
