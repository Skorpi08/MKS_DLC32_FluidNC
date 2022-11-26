# This Tutorial is nothing more than an English translation of work already previously done

This Tutorial is also based on Flashing FLUIDNC to MKS DLC32 board, however the firmware can be replaced independently and the board can also be changed out to any of the family of ESP32 based board from MKS as of the time of this writting.

## MAKE SURE TO CHOOSE A FIRMWARE THAT CORRESPONDS TO YOUR SPECIFIC BOARD

****** Instructional Video on how to use: https://www.youtube.com/watch?v=7F5B0GkXDqY  ********

**Instructions:**

1. Extract Contents to their own directory

2. Extract **CH340G_USB.zip** and **MKSLasertool_setupV1.0.6.zip**
   * 2A. Install **CH340G_USB** contents.  This installs the usb driver for communications.
   * 2B. Install **MKSLasertool** contents.  This is in not in English but uses the typical prompts.  
    
3. Launch MKSTools from install directory : C:\Program Files (x86)\MKSLaserTool\
   * 3A. Plug in your MKS laser board (various) through usb and supply power to it as USB will not power it.    
   * 3B. Choose the first promt from the *MKSLaserTools* menu **"MKS ESP32 Download Tool"**.    
     * a. Choose your selected firmware file (the included firmware file has an included basic config.yaml file for the MKS DLC32) 
     * b. Choose the COM Port Associated with your Board (check Device Manager if you are unsure of which one)        
     * c. Choose Start to Start flashign your firmware.  The included firmware in this package is FluidNC. Feel free to use others or compile your own.
                
   * 3C. Exit this sub Menu of *MKSLAserTools* and Choose **"Wifi Configuration Tool"** from main menu.    
     - a. Choose the COM Port Associated with your Board (Again check Device Manager if you are unsure of which one)        
     - b. Click on *"CONNECT"*        
     - c. If you are on your own wireless already, you can click *"Get Local Wifi"* and type in the password or: Type in both your SSID for your wireless and your password. Click *"Connect WiFi*"
        
        - If either use special characters beyond alphanumeric you must use the HEX  value for that character (Example:  SSID= "FRITZ!BOX 99200" you must type it in as "FRITZ%21BOX 99200"  the "21" indicated the HEX value for "!" and the "%" indicates that it will be a special character.  For a comprehensive list of the HEX values visit (https://www.ascii-code.com/) or search for ascii code.  The special charater you use will be listed in the symbols column, and your input will be in the HEX column.            
     - d. This will program it with your SSID and your wireless password.  If done correctly it will start the wireless on your MKS board and automaticly connect and launch the WebUI.          
     - e. For your convinience you can click on *"Get IP"* to retreive your now assigned IP for the board, and also click *"Copy IP"* to Copy the IP to the clipboard.
        
        
4. Launch your favorite web browser, and paste the aquired IP from the previous Step.


5. Future updates can be done within the Web GUI


# Note: As of the Included firmware, changes made to the config file are not saved unless you return to the *"Dashboard"* TAB and also apply *"save"* from the movement section.

# TFT Display for MKS DLC32 is also not working in the included Firmware.  Please see FluidNC's github for newer firmware that may/may not include Display files.

