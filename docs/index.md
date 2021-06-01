[Link to Test Page](./cows.md)



# QR Control Panel 

## Goal

I'm going to develop a QR code and web interface on the Pimoroni RaspPi Growhat module.  This will enable me to scan a QR code on the LCD and access a web page that allows me to configure the device settings.  The QR code will be generated automatically providing a physical layer of security. You will only need access to the physical device to configure it. 

## Approach

1. The standard QR Python library is overweight as it is designed to output a graphic. I only need a bitmap that I can output directly onto the LCD screen.  I'll need to find and extract the QR gen code from somewhere.
2. Outputing the QR code directly to the LCD won't be super difficult
3. Running a lightweight web server on the Raspberry Pi is not very hard in itself but I want to make it appropriately coupled with the code that runs the LCD and Growhat functionality.
4. The coupling mechanism could be a local or remote queue which would allow the applications to be deployed differently if desired.

## Stretch Goals

1. Implement some functionality in AWS Lightsail to provide a publically accessible (although still secure) UI. This would be important for situations where the IoT device is on a private network (i.e. Zigbee)
2. Try using PHP Lambda functionality as an alternative to Python on Lightsail
