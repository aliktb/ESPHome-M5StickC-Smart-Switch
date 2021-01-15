# ESPHome-M5StickC-Smart-Switch
Simple toggle switch for ESPHome and HomeAssistant using M5StickC and optional ENV sensor hat. Control a switch, light, group of devices or run any automation with the press of a button. The automation and config yaml files allow the M5StickC to toggle between an 'ON' and 'OFF' state. The state of the button will be updated in Home Assistant. Also, if the state of the switch is changed from another device or via the Home Assistant front-end, the M5StickC's status will also change to reflect the status of the switch.

The power symbol reflects the state of the 'dummy_toggle' template switch. This will update with the button press without intervention of Home Assistant in case of a loss in connection. This is to let the user know what state the ESP device thinks the state is. Once the automation runs on Home assistant, the switch/light associated with the automation will change state and the built-in LCD of the M5 will change to 'OFF' or 'ON' respectively. There may be a tiny delay while this happens depending on your Home Assistant's Hardware and add-ons or docker containers etc.  

#Usage
1. Copy custom files to corresponding direectories within ESPhome. Both axp192 and st7735 folders are needed for the M5Stick-C to operate.
2. If using ENV hat make sure I2C is enabled. If not, omit the I2C, dht12 and bmp280 entries in the ESPHome config yaml
3. Flash a M5StickC with the esphome yaml configuration. The name is 'node_4' but this can be renamed. 
4. Append the Home Assistant automations.yaml config file with the automations from the file in this repository. Modify the automations for your devices

# Credits
Based on this project found in ESPhome's cookbook : https://esphome.io/cookbook/leak-detector-m5stickc
Learn more about ESPhome: https://esphome.io/index.html
Learn more about Home Assistant: https://www.home-assistant.io/

# Issues
Flag any issues you find by using the [Issue tracker](https://github.com/aliktb/ESPHome-M5StickC-Smart-Switch/issues)
