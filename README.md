<img width="1546" height="1057" alt="image" src="https://github.com/user-attachments/assets/99ab0a4f-1bdc-49ee-9cff-3317d0dfef27" /><img width="671" height="572" alt="image" src="https://github.com/user-attachments/assets/4f331c47-8c11-44d9-aa90-6307cf6217eb" />


Update 10-2-2025

# Device is found on Amazon: 
   - https://www.amazon.com/dp/B0FQNNVV36?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1

# Templated install
   - Download the templates folder and put in the esphome folder that is in the config directory.
   - put the main.yml into the base esphome folder.
   - everything that needs changes for your setup is "change-me"
   - Easiest way is to use the add device, create but dont flash. paste the 'main.yml below and copy over your settings deleting everything above once you've added.

# Buttons of opperation: Buttons are multi assigned
### (**Left button:**) 
   - Momantary silences alarm
   - 10 seconds held reboots device
   - **If on battery pack can be used to cold start the device(turn on)
### (**Right button:**)
   - momentary mutes the mic and turns screen/led off **led will change to on if battery is connected after for finished charging.
   - 3 second hold when on battery pack will turn off the device. 


# Some of the insides and how it works:
This is for the Xorigin aipi. The chip is an esp32-s3-16MB. I looked high and low to find info on the display, other than it using common controller driver it does work. 

128x128 full RGB screen with white led.
3 buttons on the board. 2 external that you can click on and one internal for GPIO0(dont need to flash.
Single speaker
single MIC
Device has magnets so you potentially be put on a fridge is you like.
RGB Led that can be tiggered during listening  or whatever you want.

The device has ability to have battery pack to have it wireless. There is no logic in the battery attachment and could be run from a 18650 or other 4.2v lixx battery



Flashing is pretty straight forward. Get the file, put in your variables and plug in, no button pressing nothing just flash it and off to the races. The base yml is based off the S3 box but it's price point is $16.99 currently. I spent some time figuing out the pins(FML) and getting the LA to figure out what line did what and the start sequence of the screen.

Currently compared to the s3-box the text on screen was running off so I removed that for now.

# ⚠️ Disclaimer

Educational Use Only. The code, documentation, and examples in this repository are provided for educational and research purposes. They may involve firmware modification and battery-charging configurations that are experimental and not certified, endorsed, tested, or warranted by me or by any manufacturer.

No Warranty. The project is provided “AS IS” and WITHOUT ANY WARRANTY—express or implied—including but not limited to merchantability, fitness for a particular purpose, and non-infringement. I make no representation that the instructions or code are safe, correct, or compliant with any standard.

Assumption of Risk. You assume all risks associated with using this project. Firmware changes and hardware work can brick devices, void warranties, cause data loss, property damage, electric shock, overheating, fire, or injury. Lithium-based batteries are hazardous if misused; improper charging can cause fire or explosion.

No Certification of Battery Charging. Any battery-charging information herein is not validated or certified by me. You are responsible for ensuring proper protection circuitry, safe charging profiles, thermal management, and compliance with relevant standards (e.g., UL/IEC/CE) and local regulations.

Limitation of Liability. In no event shall I be liable for any claims, damages, losses, or other liability—whether in contract, tort, or otherwise—arising from, out of, or in connection with this project or its use.

Indemnification. By using this repository, you agree to indemnify and hold me harmless from any claims or damages resulting from your use, misuse, distribution, or modification of the code or instructions.

Compliance & Qualifications. Only qualified individuals should attempt firmware or hardware work. You are responsible for complying with all applicable laws, regulations, export controls, and safety standards in your jurisdiction. I am not affiliated with nor endorsed by any product or brand mentioned.





