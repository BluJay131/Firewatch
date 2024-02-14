# Firewatch
[![Official Website](https://img.shields.io/badge/Official%20Website-blujay131.com-blue?style=flat&logo=world&logoColor=white)](https://blujay131.com/)
[![Socials](https://img.shields.io/badge/Socials-linktr.ee/blujay131-purple?style=flat&logo=world&logoColor=white)](https://linktr.ee/blujay_131)
[![GitHub Repo stars](https://img.shields.io/github/stars/BluJay131/Cost-Effective-Twitch-Chat-Controlled-Lights?style=social)](https://github.com/BluJay131/Firewatch/stargazers)

<hr/>

### ![image](https://github.com/BluJay131/Cost-Effective-Twitch-Controlled-Lights/assets/80910384/346dc2a9-45f3-4372-8e4c-de62a3bc5e3f) Thanks for checking out my project!

**(Youtube video coming)**

## Description

A robot that automatically detects fires using `opencv-python` and <a target="_blank" href="https://github.com/ultralytics/yolov5">YoloV5</a> and shoots them with a water cannon! All powered by Raspberry Pi.

## Parts List 

- <a target="_blank" href="https://www.amazon.com/Rain-Bird-CP100-Automatic-Sprinkler/dp/B00002N8NN/ref=sr_1_2?keywords=Rain+Bird+1+in.+In-Line+Irrigation+Valve&amp;qid=1697400901&amp;sr=8-2&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=8dd2c6495d3c867894930b61098f4147&camp=1789&creative=9325">Solenoid</a>
(Make sure to get fitting pieces for adaption to water source, in my case it was a garden hose)
- <a target="_blank" href="https://www.amazon.com/dp/B07TC2BK1X?ref=ppx_yo2ov_dt_b_product_details&amp;th=1&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=f549b43aa240aa0dd22116254840e7ee&camp=1789&creative=9325">Raspberry Pi</a>
- <a target="_blank" href="https://www.amazon.com/dp/B08Y59P6D1?psc=1&amp;ref=ppx_yo2ov_dt_b_product_details&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=c7ab0c2729683f65fdccaf7b9d32193f&camp=1789&creative=9325">Adhesive Breadboards and Jumpers</a>
- <a target="_blank" href="https://www.amazon.com/dp/B0BRTHR2RL?ref=ppx_yo2ov_dt_b_product_details&amp;th=1&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=ebdc43949775f6e025d13bbef7e2621e&camp=1789&creative=9325">FTM Jumpers</a>
- <a target="_blank" href="https://www.amazon.com/dp/B0BRXVFCKX?psc=1&amp;ref=ppx_yo2ov_dt_b_product_details&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=bfaac1681e342dc3672bfba647a477ff&camp=1789&creative=9325">Pan and Tilt Kit</a>
- <a target="_blank" href="https://www.amazon.com/dp/B00VRUAHLE?psc=1&amp;ref=ppx_yo2ov_dt_b_product_details&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=c79fece967790766ef38f0fd70a48fb7&camp=1789&creative=9325">Relays</a>
- <a target="_blank" href="https://www.amazon.com/Tubing-Flexible-Hybrid-Lightweight-10-Feet/dp/B09V6WZCST/ref=sr_1_3?crid=VT314Z2TK1E0&amp;keywords=1%252F2%252Binch%252Btubing&amp;qid=1697420218&amp;s=industrial&amp;sprefix=1%252F2%252Binch%252Btubing%252Cindustrial%252C154&amp;sr=1-3&amp;th=1&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=2e5969bce631563fa633bf545da5ebfe&camp=1789&creative=9325">Tubing</a>
- <a target="_blank" href="https://www.amazon.com/Logitech-Desktop-Widescreen-Calling-Recording/dp/B004FHO5Y6/ref=sr_1_3?keywords=logitech%252B720p%252Bwebcam&amp;qid=1697420279&amp;sr=8-3&amp;th=1&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=c170c8059448bfa96468dec7793a7f50&camp=1789&creative=9325">Webcam</a>
- <a target="_blank" href="https://www.amazon.com/Adafruit-2028-Assembled-T-Cobbler-Plus/dp/B00OG4X0DK/ref=sr_1_3?crid=3B7Y1L30H4WDQ&amp;keywords=gpio+breakout+board&amp;qid=1697422612&amp;sprefix=gpio+brea%252Caps%252C146&amp;sr=8-3&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=5baa54b4b3613d0f922b5f5d069b8a5d&camp=1789&creative=9325">GPIO Breakout Board</a>
- <a target="_blank" href="https://www.amazon.com/Noctua-redux-1700-high-Performance-Award-Winning-Affordable/dp/B07CG2PGY6/ref=sr_1_2_sspa?crid=CU15JJDHJWNX&amp;keywords=120+mm+fan&amp;qid=1697422042&amp;sprefix=120+mm+fan%252Caps%252C161&amp;sr=8-2-spons&amp;sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&amp;psc=1&_encoding=UTF8&tag=blujay131-20&linkCode=ur2&linkId=0ed19b6d7787e5f2c1ba20ce4e2e7ae3&camp=1789&creative=9325">120mm Fan</a>
- Access to a 3d Printer and preferably PLA+

## Software Setup

1. Install the (Legacy, 64-Bit) Debian Bullseye OS off of the official <a target="_blank" href="https://www.raspberrypi.com/software/">Pi Imager</a>
2. Install Python 3.10+ on the Pi (tested on 3.11 & 3.10)
3. Clone <a target="_blank" href="https://github.com/ultralytics/yolov5">YoloV5</a> and cd into the folder
4. Clone this repository and/or add these files to the YoloV5 folder
5. Install the required Python libraries using the following command:
   ```
   pip install -r requirements.txt
   pip install RPi.GPIO
   ```
6. Edit the `Start.sh` file to cd to your own directory
7. (Optional) Create a .desktop file in the autorun folder to launch on boot (exec=YOUR_PATH_TO_FOLDER/Start.sh)

## Hardware Setup
(Good luck lol)

1. Start off by printing the two files in the `Print Files` folder
2. Mount the Pan and Tilt Frame to the top of the Pi case lining up the close right riser to the close right hole and drilling the other 3 as shown
<img src="https://github.com/BluJay131/Firewatch/assets/80910384/191249d1-8c56-4a9a-9d84-7ae1ae6e69a4" data-canonical-src="https://github.com/BluJay131/Firewatch/assets/80910384/191249d1-8c56-4a9a-9d84-7ae1ae6e69a4" width="250" height="500" />

3. Mount the Pi to the case and attach the breadboard and relay as shown in the image below, along with this, place your GPIO breakout evenly on the breadboard
<img src="https://github.com/BluJay131/Firewatch/assets/80910384/77f847d9-93e2-4d6f-bc92-b80bb9f67aa4" data-canonical-src="https://github.com/BluJay131/Firewatch/assets/80910384/77f847d9-93e2-4d6f-bc92-b80bb9f67aa4" width="250" height="250" />

4. As for the jumper setup, reference diagram below
<img src="https://github.com/BluJay131/Firewatch/assets/80910384/dcd35a9e-b3df-4971-9804-af0bd4291762" data-canonical-src="https://github.com/BluJay131/Firewatch/assets/80910384/dcd35a9e-b3df-4971-9804-af0bd4291762" width="300" height="300" />

5. After the internals are neatly managed (for the most part) screw on 120mm fan to case with chassis retaining screws
6. Attach the nozzle to the top of the frame using 2 screws, there is a notch at the base which you align to the hole on the frame.
7. The physical order for the flow of the water should be source -> solenoid -> vinyl tube -> printed nozzle
8. I used two steel zip ties to fix the webcam to the nozzle attached frame
<img src="https://github.com/BluJay131/Firewatch/assets/80910384/01785701-8f89-4d6b-8267-c48f1ee8994c" data-canonical-src="https://github.com/BluJay131/Firewatch/assets/80910384/01785701-8f89-4d6b-8267-c48f1ee8994c" width="300" height="500" />

9. If all done correctly, your build should look something like this minus the plywood baseplate I added for stability
<img src="https://github.com/BluJay131/Firewatch/assets/80910384/61b5f07f-0db7-4f35-8c2a-7896c8139619" data-canonical-src="https://github.com/BluJay131/Firewatch/assets/80910384/61b5f07f-0db7-4f35-8c2a-7896c8139619" width="500" height="250" />

## Turret In Action


https://github.com/BluJay131/Firewatch/assets/80910384/18919a4b-ea64-47a8-9dee-25821a107867



https://github.com/BluJay131/Firewatch/assets/80910384/e7cc6c9b-56a0-472d-a966-12713702e0be


