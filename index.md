# Third Eye for the Blind

My project is the Third Eye for the Blind. Its main objective is to help visually impaired people help have an idea of their surroundings, acting as a working eye for them. It works through an ultrasonic sensor that senses the distance of objects, then through code, will let the person know how close they're getting to an object by either a noise or vibration. This device would not only improve the quality of life for visually impaired individuals but also open up new opportunities for them to explore the world around them.
<!--Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails! !-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Arnav B | Mission San Jose Highschool | Electrical Engineering and Computer Science | Incoming Freshman



<img src="https://github.com/arnavb231/arnavb_BSE_Portfolio/assets/114638407/07f91db5-203b-48ae-8f78-b2569310af4e" width="50%" height="50%">




  
# Third Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/28ylkUqHDpI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
My project is the Third Eye for the Blind. My third milestone was to solder all the parts from the completed prototypes onto a perf board to make it permanent and portable and add a strap to make it wearable. How the project works is, the HC-SR04 ultrasonic sensor sends out an ultrasonic wave at 40KHz through its Trig pin out output which bounces off an object and then is received back by the ultrasonic sensor through the echo pin and then calculates the distance by the time it took for the wave to come back. Through the wiring connecting the ultrasonic sensor to the Arduino, the hub for the microcontroller, which is basically the brain of the device, receives the information and interprets that with the code in the Arduino. The code, which is an if statement, would let the other components, like the vibration motor, LED, and buzzer, know how to react to the object's position. If the object gets closer to the ultrasonic sensor, it will respond faster, and the rate at which they reach will get slower as the object gets farther. The device can switch from either warning from vibration or a warning from sound, controlled by a sliding switch. The primary use for that is just so the user is constantly bombarded by the loud noise from the buzzer and has a choice based on their situation. 


The main problem I had when making this final design was reliability. When I soldered all the parts on, at first, nothing was working. I had to go through many iterations, each with a bit of change, but some features didn’t work each time. The ultrasonic sensor was often not connected properly, which led to the entire device not working as it was the component that controlled everything. Many times the wiring for the pins weren’t connected well as there was either too much solder which caused the wire to touch when they were not supposed to or sometimes the connection of the wire to the exact pin was bad and didn’t touch it and causing the ultrasonic sensor giving random inputs which confused me. And occasionally, the ultrasonic sensor would work for a second and cause the rest of the system to work, but that wasn’t good enough for the final design. So I had to look at the wiring design and learned how to manage the wire better. So, in the end, I solder the pins for the ultrasonic sensor directly to points on the Arduino, which managed to get it working, which I was happy about. So I velcroed it onto tape at first to make a quick handl,e and that is what was shown in the video, but later I changed it to a buckle so it looked better and was more reliable. My next steps, if I had more time at BlueStamp, would be to add a speaker to the device so it could read the exact distance of objects, as that information is only shown in the Serial Monitor on the Arduino IDE app used for coding the Arduino. Additionally, I would like to add object recognition to the device, which would say what the object is through the speaker so the user would know exactly what object is in front of them and make everyday things like shopping easier for the visually impaired or whoever needs it. 


Overall, I enjoyed BlueStamp it was great to learn about electrical engineering, coding, and arduino, and the talks the guest speakers gave. The program was informative, and the instructors were terrific and did a fantastic job helping me through the program. I would recommend this camp to anyone who likes engineering and wants to get real-life experience of going through the engineering process and building a final product.

# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/AxO99hXYjkE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

 My project is the Third Eye for the Blind. My second milestone was to make a buzzer, vibration motor and LED react similarly to the distance of an object from the ultrasonic sensor in two devices so they could be implemented on each hand for the final design. How it works is the HC-SR04 ultrasonic sensor locates the distance of an object by first transmitting an ultrasonic wave at 40KHz, which then bounces off an object. The ultrasonic sensor would then receive the wave through its receiver or Echo pin, which, based on how long the wave took to be obtained, would calculate the object's distance. Then, the buzzer, LED, and vibration motor would react accordingly through the new code. As an object gets closer, the components respond faster and faster, warning the user an object is getting closer to them or they are approaching an object. A switch controls the buzzer and vibration motor so the user can choose between vibration and sound due to the volume the buzzer is set at, which is very loud and can be annoying to the user and people around them. The main problem I faced while making this was with the code. I had to figure out how to use the code properly as the sample code given in the project instructions was uncompleted and was not set to the Arduinos I had, so I had to add extra code to make it compatible with all the new parts I added, the custom wiring I implemented for simplicity, and the different Arduinos. But in the end, I got it working by finding resources to learn about C++ to understand and code the problem. My next step would be to solder all the components to a perf board to finalize the design and make it portable by adding it to a strap or glove to make it wearable by the user.

# First Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/FJMfOTjolzM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My project is the third eye for the Blind. My first milestone was to connect and make my ultrasonic sensor work alongside my buzzer and LEDs as a prototype so I could understand how all the parts work. The HC-SR04 ultrasonic sensor works by transmitting sound waves through the Trig pin at 40KHz. Those sound waves hit the object and come back, and the receiver(Echo pin) of HC-SR04 gives you the total time taken by the sound waves from the transmitter to reach the receiver. The LEDs would turn on through code for a certain distance away from the object. Specifically, the red LED would turn on if the thing was 15 or fewer centimeters away from the device, and the green one would turn on at any other distance in the ultrasonic sensor’s 400-centimeter range. Additionally, the buzzer would beep at a specific frequency if the ultrasonic sensor could sense anything signaling it was working, but it would make a long solid noise if the sensor couldn't sense anything. The main problem I faced while prototyping was initially with the code. It was an online code that I found to prototype, and it was set for a different kind of Arduino and used other pins, so I had to change it to fit my Arduino and the pins it had, as well as add code for a buzzer as it was not counted in the online code. Another problem was with the wiring. The Arduino Nano Every is not meant to be used with a breadboard, but I had to use it to understand how it worked. So many times, the metal pins on the Arduino did not connect properly with the metal rows on the bottom of the breadboard, so sometimes the other parts, like the LEDs, didn’t work even though the code was working correctly. So, in the end, I just had to push down on the Arduino constantly so that its pins were touching the metal and sending power to the other parts through the jumper cables. My next steps would be replicating this prototype with other project parts, like a vibration motor and a switch to change between the buzzer and the motor. Additionally, I would like to start using the actual code that lets the project react to objects getting closer to the ultrasonic sensor by responding faster and faster as the thing gets closer


<!--iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe!-->
# Starter Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/XJPtsFAbf1M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My starter project was TV-B-Gone. All the parts were soldered onto a perf board which was powered by two double AA batteries. All the code the device needed to work was stored in a microcontroller. The way the project worked was first a button would be clicked, that would let the microcontroller know that it had to tell the transistors, which control the IR LED lights, to turn the LEDs on. Then the IR lights in the front of the device would flash in different ways because TVs turn off to different signals, so to be able to turn off any TV the IR lights would have to flash in different ways. This would be indicated by a smaller LED in the back of the device. I enjoyed learning how to solder components to the perf board and learning what each part does. Something I struggled with while building was soldering the small parts because of the precision required and finding the problem with certain parts.




# Schematics 

<img src="https://github.com/arnavb231/arnavb_BSE_Portfolio/assets/114638407/e9cb2f57-a15c-4b7a-9d89-b5c5cdd78cff" width="70%" height="70%">





<!---Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser.-->

# Code

```c++

  const int pingTrigPin = 19; //Trigger connected to PIN A5  
  const int pingEchoPin = 16; //Echo connected to PIN A3  
  #define led 7 // LED to PIN D7
  int buzz = 9; //Buzzer & Vibration Motor to PIN D9
  void setup() {   
  Serial.begin(9600);   
  pinMode(buzz, OUTPUT); 
  pinMode(led, OUTPUT);
  }   
  void loop()   
  {   
  long duration, cm;   
  pinMode(pingTrigPin, OUTPUT);   
  digitalWrite(pingTrigPin, LOW);   
  delayMicroseconds(2);   
  digitalWrite(pingTrigPin, HIGH);   
  delayMicroseconds(5);   
  digitalWrite(pingTrigPin, LOW);   
  pinMode(pingEchoPin, INPUT);   
  duration = pulseIn(pingEchoPin, HIGH);   
  cm = microsecondsToCentimeters(duration);   
  if(cm<=50 && cm>0)   
  {   
  int d= map(cm, 1, 100, 20, 2000);   
  int pch = 4000; 
  tone(buzz, pch);
  delay(d);
  noTone(buzz);    
  delay(d); 
  digitalWrite(led, LOW);
  delay(d);
  digitalWrite(led, HIGH);
  }   
  Serial.print(cm);    
  Serial.print("cm");   
  Serial.println();   
  delay(100);   
  }   
  long microsecondsToCentimeters(long microseconds)   
  {   
  return microseconds / 29 / 2;   
  }   
```


# Bill of Materials
<!---Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs.-->

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Nano Every | It is the microcontroller board for the project | $13.70 | <a href="https://store-usa.arduino.cc/products/arduino-nano-every/"> Link </a> |
| Arduino Nano | It is the microcontroller board for the project | $24.90 | <a href="https://store-usa.arduino.cc/products/arduino-nano/"> Link </a> |
| 2 Ultrasonic Sensors | These devices look for the distance of objects | $9.19(for 5) | <a href="https://www.amazon.com/HiLetgo-HC-SR04-Ultrasonic-Distance-MEGA2560/dp/B00E87VXH0/ref=sr_1_4?crid=C7QH3O2MI588&keywords=hcsr04+ultrasonic+sensor&qid=1689190342&sprefix=ultrasonic+sensor+hc%2Caps%2C229&sr=8-4/"> Link </a> |
| 2 Buzzer | These devices make a buzzing noise  | $7.28(for 10) | <a href="https://www.amazon.com/Gikfun-Terminals-Passive-Electronic-Arduino/dp/B01GJLE5BS/ref=sr_1_2_sspa?crid=2DHWNU6FUR4VO&keywords=buzzer+for+arduino&qid=1689190503&sprefix=buzzer+for+arduino%2Caps%2C222&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link 
| 2 Vibration Motor | These devices rotate at high speeds causing a vibration effect | $17.99(for 15) | <a href="https://www.amazon.com/BestTong-Miniature-Vibrating-Vibration-Coreless/dp/B073NGPHDR/ref=sr_1_3_sspa?crid=3RU4WULUPY8KL&keywords=vibration+motors&qid=1689190876&sprefix=vibration+motor%2Caps%2C165&sr=8-3-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link 
| 2 Switch | It allows the user to switch between the buzzer and vibration motor | $8.99(for 100) | <a href="https://www.amazon.com/DIYhz-100Pcs-Position-Vertical-Arduino/dp/B07BD1SPYG/ref=sr_1_10?crid=29IKC87IO7NOF&keywords=sliding+switch&qid=1689700232&sprefix=sliding+switch%2Caps%2C142&sr=8-10/"> Link </a> |
| 2 LEDs | Small lights that in this project help visually indicate distance | $11.99(for box with 500) | <a href="https://www.amazon.com/dp/B09XDMJ6KY/ref=twister_B09XD74GNQ?_encoding=UTF8&th=1/"> Link </a> |
| Header Pins | A socket to place importants parts so they don't touch the board | $12.78(for a boz with 120) | <a href="https://www.amazon.com/Glarks-Straight-Connector-Assortment-Prototype/dp/B076GZXW3Z/ref=sr_1_1_sspa?crid=FTDP4J35R1H7&keywords=header+pins&qid=1689700837&s=industrial&sprefix=header+pins%2Cindustrial%2C160&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link </a> |
| Perfboard | A board to solder all connection for the device | $8.49 | <a href="https://www.amazon.com/10-Pieces-Perfboard-Universal-Stripboard-Prototyping/dp/B019Q14GRQ/ref=sxin_16_pa_sp_search_thematic_sspa?content-id=amzn1.sym.1c86ab1a-a73c-4131-85f1-15bd92ae152d%3Aamzn1.sym.1c86ab1a-a73c-4131-85f1-15bd92ae152d&crid=1S4CV20I5EFC3&cv_ct_cx=perfboards&keywords=perfboards&pd_rd_i=B019Q14GRQ&pd_rd_r=19b77302-1506-498a-856c-9ac68f269a3f&pd_rd_w=px6Ct&pd_rd_wg=Fef3A&pf_rd_p=1c86ab1a-a73c-4131-85f1-15bd92ae152d&pf_rd_r=4277GF1B8GMA45HQBE0S&qid=1689701179&s=industrial&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=perfboard%2Cindustrial%2C161&sr=1-3-364cf978-ce2a-480a-9bb0-bdb96faa0f61-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&psc=1/"> Link </a> |
| Solid-Core Wire | Used for making connections between parts | $6.86(for 25ft spool) | <a href="https://www.amazon.com/Adafruit-Solid-Core-Wire-Spool-ADA290/dp/B00KAE3NTQ/ref=sr_1_7?crid=2QI4ZH6KTWJUD&keywords=solid+core+wire&qid=1689701288&s=industrial&sprefix=solidcore+wire%2Cindustrial%2C167&sr=1-7/"> Link </a> |
| Tape| can be uses for holding wires or making a strap | $6.99(for 2 rolls) | <a href="https://www.amazon.com/LICHAMP-Masking-General-Purpose-Beige/dp/B08T6186TG/ref=sr_1_5?crid=3TMYB8XPQQHYV&keywords=masking+tape&qid=1689703358&s=industrial&sprefix=masking+tape%2Cindustrial%2C200&sr=1-5/"> Link </a> |
| Velcro | Used to stick parts together or can be used in strap for hand | $9.99 | <a href="https://www.amazon.com/Melsan-inch-Hook-Loop-Tape/dp/B07Y3VDPLF/ref=sr_1_2_sspa?crid=BZNUU40E2GXU&keywords=velcro&qid=1689703447&s=industrial&sprefix=velcro%2Cindustrial%2C160&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link </a> |
| Jumper Cables | Can connect header pins to other devices | $6.98 | <a href="https://www.amazon.com/Melsan-inch-Hook-Loop-Tape/dp/B07Y3VDPLF/ref=sr_1_2_sspa?crid=BZNUU40E2GXU&keywords=velcro&qid=1689703447&s=industrial&sprefix=velcro%2Cindustrial%2C160&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link </a> |



<!---# Other Resources/Examples-->
<!---One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.-->
