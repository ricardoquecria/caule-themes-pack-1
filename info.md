# Caule Themes Pack 1 - by caulecriativo.com
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=flat-square)](https://github.com/custom-components/hacs)
[![ha brasil](https://img.shields.io/static/v1?label=HA%20Brasil&message=forum&color=green&style=flat-square)](https://forum.homeassistantbrasil.com.br/t/caule-themes-pack-1-by-caulecriativo-com/1422)
[![ha brasil discord](https://img.shields.io/static/v1?label=HA%20Brasil&message=discord&color=blueviolet&style=flat-square)](http://habr.ml)
[![homeassistant_community](https://img.shields.io/badge/HA%20community-forum-brightgreen?style=flat-square)](https://community.home-assistant.io/t/caule-themes-pack-1-by-caulecriativo-com/209436)
[![Github Stars](https://img.shields.io/github/stars/orickcorreia/caule-themes-pack-1?logo=github&style=social)](https://github.com/orickcorreia/caule-themes-pack-1)
[![Github Follow](https://img.shields.io/github/followers/orickcorreia?logo=github&style=social)](https://github.com/orickcorreia)

Created by Ricardo Correia for the Home Assistant Brazil community.
* 10 modern colors;
* 4 categories of styles;
   - Black Glass
   - Black
   - Dark
   - Light
* 40 themes in total;
* Animated icons for the weather forecast card;
* And a bonus automatic theme selector for your interface with Node-RED.

I want to ask only 2 things if you like my work:

1) Contribute to my work! [Buy Me A Coffee](https://www.buymeacoffee.com/orickcorreia)
2) Follow my creative studio on instagram: [caulecriativo.com](http://caulecriativo.com)

Make good use of themes ☺️

<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/pack.gif?raw=true">

<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/01-rose.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/02-purple.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/03-blue.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/04-aqua.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/05-green.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/06-yellow.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/07-orange.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/08-coral.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/09-pink.png?raw=true">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/10-gray.png?raw=true">


# Animated icons included
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/animated-icons.gif?raw=true">


<div>
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/clear-night.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/sunny.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/cloudy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/fog.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/hail.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/lightning-rainy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/lightning.svg?raw=true" width="100px"><br>
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/partlycloudy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/pouring.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/rainy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/windy-variant.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/windy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/snowy.svg?raw=true" width="100px">
<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/themes/snowy-rainy.svg?raw=true" width="100px">
</div>

## If you STILL DON'T have the "themes" folder

Then you need to configure your **configuration.yaml** file, adding the code below for your Home Assistant to search for themes in the **themes** folder:

```
frontend:
  themes: !include_dir_merge_named themes
```
(reboot required)


# Creating an automatic theme selector for the interface (optional)
We will create a theme selector to be implemented in your user interface. It is a practical way to change the theme instantly on all devices connected to your Home Assistant. See how it works in the gif below:

<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/seletor.gif?raw=true">

## 1st Step - Creating the input_select
The input_select will be used to create the selection list with the themes that I created. <br>
Insert this code into your file **configuration.yaml**<br>
If you've never used input select, [learn more by clicking here.](https://www.home-assistant.io/integrations/input_select)<br><br>

```
input_select:

  themes:
    name: 'Themes'
    icon: mdi:format-paint
    options:
      - Caule Black Rose
      - Caule Black Purple
      - Caule Black Blue 
      - Caule Black Aqua
      - Caule Black Green
      - Caule Black Yellow
      - Caule Black Orange
      - Caule Black Coral
      - Caule Black Pink
      - Caule Black Gray
      - Caule Dark Rose
      - Caule Dark Purple
      - Caule Dark Blue 
      - Caule Dark Aqua
      - Caule Dark Green
      - Caule Dark Yellow
      - Caule Dark Orange
      - Caule Dark Coral
      - Caule Dark Pink
      - Caule Dark Gray
      - Caule Light Rose
      - Caule Light Purple
      - Caule Light Blue 
      - Caule Light Aqua
      - Caule Light Green
      - Caule Light Yellow
      - Caule Light Orange
      - Caule Light Coral
      - Caule Light Pink
      - Caule Light Gray
      - Caule Black Rose Glass
      - Caule Black Purple Glass
      - Caule Black Blue Glass 
      - Caule Black Aqua Glass
      - Caule Black Green Glass
      - Caule Black Yellow Glass
      - Caule Black Orange Glass
      - Caule Black Coral Glass
      - Caule Black Pink Glass
      - Caule Black Gray Glass      
      - Default
```
Restart your Home Assistant so that the input_select is created.


Result:
* input_select.themes



## 2ª Stage - Automation of the theme selector in Node-RED

**WARNING!** If you've never used Node-RED, [learn more by clicking here.](https://github.com/hassio-addons/addon-node-red)


We will create a flow in Node-RED to define the theme automatically every time you choose a theme in your interface. It's very simple! Just download the .json file or copy the code and paste it into the Node-RED import window.

<img src="https://github.com/orickcorreia/caule-themes-pack-1/blob/master/docs/nodered.gif?raw=true">

[Click here to copy or download the code for Node-RED flows](https://raw.githubusercontent.com/orickcorreia/caule-themes-pack-1/master/src/seletor_theme_nodered.json)

After importing the flow to your Node-RED, click **Deploy**<br><br>

## 3rd Step - Implementing the selector in your interface

Now just insert the selector code in your interface.
* If you use the interface in YAML Mode, copy the code and insert it into your **ui-lovelace.yaml**
* If you use the interface in automatic mode, go to the editing mode of your interface, choose the "manual" option at the end, then copy and paste the code below.

``` 
  type: entities
  show_header_toggle: false
  entities:
    - entity: input_select.themes

``` 

## 4th Step - Configuring the "Backend-selected" theme

Change the theme in the user's profile to "Backend-selected". This way, all connected devices with the theme "Backend-selected" will have their themes changed synchronously with the theme selector you just created.



### Now just enjoy it!
### If everything goes well, [send a print](http://api.whatsapp.com/send?phone=5565999593909) ☺️

<a href="https://www.buymeacoffee.com/orickcorreia" target="_blank">
<img src="https://cdn.buymeacoffee.com/buttons/lato-black.png"  width="200px" alt="Buy Me A Coffee" ></a>

Icons created by [amCharts](https://www.amcharts.com/free-animated-svg-weather-icons/) and modified by me.




