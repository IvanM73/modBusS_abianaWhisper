# modBusS_SabianaWhisper
package to support remote control of sabiana whisper fancoil via modbus on Home Assistant

############## HARDWARE CONFIGURATION #####################
here the schema for wiring the thermostat highlided in yallow the modbus connector:
![image](https://github.com/user-attachments/assets/e931e7d0-1206-4331-8189-ba6b65181d10)

#below the TCP=>Modbus HW used and how is wired to a single fancoil
![image](https://github.com/user-attachments/assets/e741361e-d3d1-4612-999e-c0376a234c6a)

#here how to connect the modbus cable to the fancloil. Currently I've connected a single fancoil, TBD how to connect multiple fanclois.
![image](https://github.com/user-attachments/assets/d34e49a4-3f9b-4f09-ab92-7e6be7a6da4e)


##### HW configuration
#Each Fancoil need to be configured to have a unique address, here the swicth to set the fancoil address
![image](https://github.com/user-attachments/assets/c80c30e4-9b4d-475a-a032-46dece8f4baa)

#here the schema that define the address for each deep switch combination
![image](https://github.com/user-attachments/assets/76ab72b6-8a8c-41ba-9d96-bbba848bc3a3)

############## SOFTWARE CONFIGURATION #####################
#To integrate sabiana whisper via mod bus to home assistant you have to:
1- Connect the TCP=>modus rtu module to your lan and retrive the ip from your modem
2- Connect the modbus cable (any twisted cable is fine for a first test) between modbus rtu and sabiana module
3- Configure the HW switch and identify the fancoil unquique address
4- copy the modbusthermostat.yaml to your package diurectory
5- configure the package with the correct IP address (host) and slave (or use 1 for testing)

That configuration will create a climate.fc_test_climatetemplate entity from where you can control the fancoil
![image](https://github.com/user-attachments/assets/c133bd70-fc14-4618-95c5-1a6e61ecbe20)


############## DOCUMENTATION #####################
# Sabiana Up touch documentation:
[up-touch-up-eco-4051361-man-rev-04-2021_ITALIAN.pdf](https://github.com/user-attachments/files/20709677/up-touch-up-eco-4051361-man-rev-04-2021_ITALIAN.pdf)

# Sabiana ModBus Manual:
[modbus sabiana MB EXT v0.20_ENG.pdf](https://github.com/user-attachments/files/20709681/modbus.sabiana.MB.EXT.v0.20_ENG.pdf)
