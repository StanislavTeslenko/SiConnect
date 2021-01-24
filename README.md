# SiConnect
Application for connection to Siemens SIMATIC S7-1200 and S7-1500 PLCs via internal web-server

## Development stage:
Pre-release, testing before upload app to AppStore

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
3. Create connection to PLC into application
4. Enjoy :)

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
          <p> All displayed data is cyclically loaded from PLC  </p>
          <p> Orange backgound color - unit has a warning state  </p>
          <p> Red backgound color - unit has a alarm state  </p>
    </td>
  </tr>
 </table>
 
4. After tapping on the unit cell will open the screen with the peripheral stations that belong to the unit (For example ET200SP stations). The displayed data is fully described in the server configuration file. In this example, the unit has only one peripheral station ET200SP.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105578564-ecd1b080-5d89-11eb-980d-42b8c46e30ee.png"></td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629024-4cdb5c00-5e49-11eb-87ad-fecce95a33e3.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC  </p>
          <p> Station state is displayed into right-up cell corner </p>
          <p> If station has a channel whitch is Forced, a "Force" symbol is displayed </p>
          <p> If station has a channel whitch is in Error state, a station cell have a Red border </p>
          <p> If all modules of station are "Checked", the "Checked" symbol is displayed </p>
    </td>
  </tr>
 </table>
 
5. After tapping on the station cell will open the screen with the station's modules. The displayed data is fully described in the server configuration file. In this example, the station has AI (Analod Input), AO (Analog Output), DI (Discrete Input) and DO (Discrete Output) modules.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105578567-ef340a80-5d89-11eb-96d7-a48997e2bcd7.png"></td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629450-a3499a00-5e4b-11eb-8539-0cdeb22604d9.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC  </p>
          <p> If module has a channel whitch is Forced, a "Force" symbol is displayed </p>
          <p> If station has a channel whitch is in Error state, a station cell have a Red border </p>
          <p> If all channels of module are "Checked", the "Checked" symbol is displayed </p>
    </td>
  </tr>
 </table>
 
6. After tapping on the module cell will open the screen with the module's channels. The displayed data is fully described in the server configuration file. In this example, the AO module has two channels.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629573-7053d600-5e4c-11eb-8668-8f568c6805b5.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC  </p>
          <p> If channel is Forced, a "Force" symbol is displayed </p>
          <p> If channel is in Error state, a channel cell have a Red border </p>
          <p> If channel is "Checked", the "Checked" symbol is displayed </p>
    </td>
  </tr>
 </table>
 
6. After tapping on the channel cell will open the screen with the channel's data. The displayed data is fully described in the server configuration file. There are 4 channel types: 2 input channels (AI and DI) without user control, and 2 output channels (AO and DO) with user control.

<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="80"> <b> AI channel </b> </td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629786-cbd29380-5e4d-11eb-8ec9-68c8a4ea4761.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC </p>
          <p> To mark channel as "Checked" tap on "Channel Checked" switch </p>
    </td>
  </tr>
  <tr>
    <td width="80"> <b> DI channel </b> </td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629789-cd9c5700-5e4d-11eb-803a-a42385706c50.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC </p>
          <p> To mark channel as "Checked" tap on "Channel Checked" switch </p>
    </td>
  </tr>
  <tr>
    <td width="80"> <b> AO channel </b> </td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629790-cf661a80-5e4d-11eb-92ee-7528259d94bb.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC </p>
          <p> To enable Forced control tap on "Control enable" switch </p>
          <p> After activating Forced control set desired value via slider and press "Set" button </p>
          <p> To mark channel as "Checked" tap on "Channel Checked" switch </p>
    </td>
  </tr>
  <tr>
    <td width="80"> <b> DO channel </b> </td>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105629795-d42ace80-5e4d-11eb-94dc-1104d9696d3d.png"></td>
    <td width="300">
          <p> All displayed data is cyclically loaded from PLC </p>
          <p> To enable Forced control tap on "Control enable" switch </p>
          <p> After activating Forced control set desired value via buttons "On" and "Off" </p>
          <p> To mark channel as "Checked" tap on "Channel Checked" switch </p>
    </td>
  </tr>
 </table>
 
 From each screen of the unit, you can open a hierarchical table indicating the checked channels
 
 <table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105630673-2d493100-5e53-11eb-9e3a-551779992fc7.png"></td>
    <td width="300">
          <p> Table with check status of channels </p>
    </td>
  </tr>
 </table>
 
 This message will display if there is network or connection error:
 
<table width="100%" cellspacing="0" cellpadding="4" border="0">
  <tr>
    <td width="270"><img src="https://user-images.githubusercontent.com/49919277/105630654-1571ad00-5e53-11eb-981a-997ef1a6090e.png"></td>
    <td width="300">
          <p> Network or connection error </p>
    </td>
  </tr>
 </table>

## Built With

* [Alamofire](https://github.com/Alamofire/Alamofire)
* [IQKeyboardManager](https://github.com/hackiftekhar/IQKeyboardManager)
* [MultiSlider](https://github.com/yonat/MultiSlider)
* [LMGaugeViewSwift](https://github.com/lminhtm/LMGaugeViewSwift)

## Authors

<script type="text/javascript" src="https://platform.linkedin.com/badges/js/profile.js" async defer></script>
<div class="LI-profile-badge"  data-version="v1" data-size="medium" data-locale="ru_RU" data-type="horizontal" data-theme="dark" data-vanity="stanislavteslenko"><a class="LI-simple-link" href='https://ua.linkedin.com/in/stanislavteslenko?trk=profile-badge'>Станислав Тесленко</a></div>

* **Stanislav Teslenko** - *Developer* - [LinkedIn](www.linkedin.com/in/stanislavteslenko)
