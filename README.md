# SiConnect
Application for connection to Siemens SIMATIC S7-1200 and S7-1500 PLCs via internal web-server

## Development stage:
Pre-reliase, testing before upload app to AppStore

## Technical description:

Getting data from Siemens SIMATIC S7-1200/1500 PLCs is a very necessary, but confusing task. This PLC-s dont have any API and 
there isn't public librarys of Siemens S7 protocol for iOS. Any other supported protocols (e.g Modbus TCP, MQTT) do not 
provide simple data acquisition, but require laborious UI creation.

SiConnect is mobile application which used to visualize data from a PLC. The application constantly communicates with the PLCs web-server and does not require the development of UI on the side of the iOS end-user. The connection takes place over the WiFi network.

## Benefits:
1. Absolute protection of the PLC program from external impact
2. Very fast data preparation into PLC program
3. There isn't time-consuming development of the user interface for the end user

## Deployment

1. Create JSON files that describe the system - [manual](https://github.com/StanislavTeslenko/SiConnect/blob/main/01%20Create%20JSON%20files%20for%20PLC)
2. Configure PLC program - [manual](https://github.com/StanislavTeslenko/SiConnect/blob/main/02%20Create%20PLC%20Program)
3. Configure application

## Application configuration

1. "Server List" screen. This is the main screen of the application. 

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105578482-31108100-5d89-11eb-908d-c5468d0432ab.png"></td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105580384-bf3e3480-5d94-11eb-81d8-abeaebc6f1f9.png"></td>
    <td width="300">
          <p> On this screen, user can create a new connection ("Add" button) to a PLC (so-called "Server"). </p>
          <p> With 3D-touch is possible to: </p>
          <p> - edit the server; </p>
          <p> - delete the server; </p>
          <p> - mark (and unmark) server as the default server. Default server mark with symbol "Star". </p>
          <p> If server mark as default, application load this server after start. </p>
    </td>
  </tr>
 </table>
 
 
2. "Add" ("Edit") screens. Into this screens create new or edit existing server is possible.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105578524-98c6cc00-5d89-11eb-81bf-8f86eec00623.png"></td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105580882-c286ef80-5d97-11eb-8014-a052665e13f4.png"></td>
    <td width="300">
          <p> Valid IP Address of the PLC is necessary </p>
          <p> "Username" and "Password" fields are required for authentication to PLC's web-server </p>
    </td>
  </tr>
 </table>
 
 
 3. After tapping on the created server cell will open the screen with the data downloaded from the server. The displayed data is fully described in the server configuration file.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105578526-9d8b8000-5d89-11eb-98f9-526ab609724f.png"></td>
    <td width="300">
          <p> Valid IP Address of the PLC is necessary </p>
    </td>
  </tr>
 </table>

## Built With

* [Alamofire](https://github.com/Alamofire/Alamofire) - Elegant HTTP Networking in Swift

## Authors

* **Stanislav Teslenko** - *Developer* - [Stanislav Teslenko](https://github.com/StanislavTeslenko)
