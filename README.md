# Themes Pack 2.0 - by caulecriativo.com
[English version](README.md)

Created by Ricardo Correia for the Home Assistant Brasil community.
<br> There are 10 modern cores, totaling 40 different themes!

I want to ask only 2 things for those who benefit from these themes:

1) Join the HABR community on Discord: [habr.ml](http://habr.ml)
2) Follow my creative studio on instagram: [caulecriativo.com](http://caulecriativo.com)

Make good use of themes ☺️


![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/pack1.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/pack2.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/pack3.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/pack4.png)



![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/01-rose.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/02-purple.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/03-blue.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/04-aqua.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/05-green.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/06-yellow.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/07-orange.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/08-coral.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/09-pink.png)
![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/10-gray.png)


# Installation of themes

## If you already have a themes.yaml file

So just copy the code or download **themes.yaml** [**clicking here**](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/src/en/themes.yaml).


## If you DO NOT STILL have a themes.yaml file

Then you need to configure your **configuration.yaml** file, adding the code below for your Home Assistant to search for themes in the **themes.yaml** file:

```
frontend:
  themes: !include themes.yaml
```

After entering the configuration in your **configuration.yaml**, download the file **themes.yaml** [**clicking here**](https://raw.githubusercontent.com/orickcorreia/ha-themes -pack-2.0/master / src / en-us / themes.yaml) and copy this file to your ** config ** folder. The ** themes.yaml ** file must be in the same folder as the ** configuration.yaml ** file.


## Download backgrounds
10 of the 40 themes have backgrounds that need to be downloaded and copied to your Home Assistant server. Download the backgrounds [**clicking here.**](https://github.com/orickcorreia/ha-themes-pack-2.0/raw/master/src/backgrounds.zip) Extract the file **.Zip** and copy the **backgrounds** folder into the **/config/www/** folder. The final path to the file folder should be **/config/www/backgrounds/**


*ATTENTION! If your **www** folder does not yet exist, create it within the **config** folder.*


Now **restart your Home Assistant** and the themes will be available for use.



# Creating an automatic theme selector for the interface (optional)

We will create a theme selector to be implemented in your user interface. It is a practical way to change the theme instantly on all devices connected to your Home Assistant. See how it works in the gif below:

![](https://github.com/orickcorreia/ha-themes-pack-2.0/blob/master/images/seletor.gif)

## 1ª Etapa - Criando o input_select
O input_select será usado para criar a lista de seleção com os temas que eu criei.<br>
Se você nunca usou input select, [saiba mais clicando aqui.](https://www.home-assistant.io/integrations/input_select)<br><br>
```
input_select:

  themes:
    name: 'Temas'
    icon: mdi:format-paint
    options:
      - Black Rose - Flat
      - Black Purple - Flat
      - Black Blue - Flat 
      - Black Aqua - Flat
      - Black Green - Flat
      - Black Yellow - Flat
      - Black Orange - Flat
      - Black Coral - Flat
      - Black Pink - Flat
      - Black Gray - Flat
      - Dark Rose - Flat
      - Dark Purple - Flat
      - Dark Blue - Flat 
      - Dark Aqua - Flat
      - Dark Green - Flat
      - Dark Yellow - Flat
      - Dark Orange - Flat
      - Dark Coral - Flat
      - Dark Pink - Flat
      - Dark Gray - Flat
      - Light Rose - Flat
      - Light Purple - Flat
      - Light Blue - Flat 
      - Light Aqua - Flat
      - Light Green - Flat
      - Light Yellow - Flat
      - Light Orange - Flat
      - Light Coral - Flat
      - Light Pink - Flat
      - Light Gray - Flat
      - Black Rose - Transparent
      - Black Purple - Transparent
      - Black Blue - Transparent 
      - Black Aqua - Transparent
      - Black Green - Transparent
      - Black Yellow - Transparent
      - Black Orange - Transparent
      - Black Coral - Transparent
      - Black Pink - Transparent
      - Black Gray - Transparent      
      - Default
```
Reinicie o seu Home Assistant para que o input_select seja criado.


Resultado:
* input_select.themes



## 2ª Etapa - Automação do seletor de temas no Node-RED

**ATENÇÃO!** Se você nunca usou o Node-RED, [saiba mais clicando aqui.](https://github.com/hassio-addons/addon-node-red)


Vamos criar um flow no Node-RED para definir o tema automaticamente toda vez que você escolher um tema na sua interface. É bem simples! Basta fazer o download do arquivo .json ou copiar o código e colar na janela de importação do Node-RED.

[Clique aqui para copiar ou fazer download do código dos fluxos do Node-RED](/src/seletor_theme_nodered.json)


Após importar o flow para o seu Node-RED, clique em **Deply**<br><br>

## 3ª Etapa - Implementando o seletor na sua interface

Agora é só inserir o código do seletor na sua interface.
* Se você usa a interface no Modo YAML, copie o código e insira no seu **ui-lovelace.yaml**
* Se você usa a interface no modo automático, vá até o modo de edição da sua interface, escolha a opção "manual" lá no final, depois copie e cole o código abaixo.

``` 
- type: entities
  show_header_toggle: false
  entities:
    - entity: input_select.themes

``` 

### Agora é só aproveitar!
### Se tudo der certo, [mande um print](http://api.whatsapp.com/send?phone=5565999593909) ☺️
