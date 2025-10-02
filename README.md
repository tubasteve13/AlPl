<img width="1546" height="1057" alt="image" src="https://github.com/user-attachments/assets/99ab0a4f-1bdc-49ee-9cff-3317d0dfef27" /><img width="671" height="572" alt="image" src="https://github.com/user-attachments/assets/4f331c47-8c11-44d9-aa90-6307cf6217eb" />


Update 10-2-2025

# Templated install
   - Download the templates folder and put in the esphome folder that is in the config directory.
   - put the main.yml into the base esphome folder.
   - everything that needs changes for your setup is "change-me"
   - Easiest way is to use the add device, create but dont flash. paste the 'main.yml below and copy over your settings deleting everything above once you've added.

This is for the Xorigin aipi. The chip is an esp32-s3-16MB. I looked high and low to find info on the display, other than it using common controller driver it does work. 

128x128 full RGB screen with white led.
3 buttons on the board. 2 external that you can click on and one internal for GPIO0(dont need to flash.
Single speaker
single MIC
Device has magnets so you potentially be put on a fridge is you like.
RGB Led that can be tiggered during listening  or whatever you want.

The device has ability to have battery pack to have it wireless. There is no logic in the battery attachment and could be run from a 18650 or other 4.2v lixx battery

Device is found on Amazon: https://www.amazon.com/dp/B0FQNNVV36?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1

Flashing is pretty straight forward. Get the file, put in your variables and plug in, no button pressing nothing just flash it and off to the races. The base yml is based off the S3 box but it's price point is $16.99 currently. I spent some time figuing out the pins(FML) and getting the LA to figure out what line did what and the start sequence of the screen.

Currently compared to the s3-box the text on screen was running off so I removed that for now.

# Buttons of opperation: Buttons are multi assigned
### (**Left button:**) 
   - Momantary silences alarm
   - 10 seconds held reboots device
   - **If on battery pack can be used to cold start the device(turn on)
### (**Right button:**)
   - momentary mutes the mic and turns screen/led off **led will change to on if battery is connected after for finished charging.
   - 3 second hold when on battery pack will turn off the device.


