# Third Eye for the Blind

My project is the Third Eye for the Blind. Its main objective is to help visually impaired people help have an idea of their surroundings, acting as a working eye for them. It works through an ultrasonic sensor that senses the distance of objects, then through code, will let the person know how close they're getting to an object by either a noise or vibration. This device would not only improve the quality of life for visually impaired individuals but also open up new opportunities for them to explore the world around them.
<!--Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails! !-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Arnav B | Mission San Jose Highschool | Electrical Engineering and CS | Incoming Freshman

<!--**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**!-->

<img src="https://github.com/arnavb231/arnavb_BSE_Portfolio/assets/114638407/644b1686-d73e-4a32-b26f-601aac8dc901" width="50%" height="50%">


<!---![Headstone Image](logo.svg)
  
<!---# Final Milestone
<!--For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<!---iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe!--->

# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/AxO99hXYjkE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My project is the Third Eye for the Blind. My second milestone was to make a buzzer, vibration motor and LED react similarly to the distance of an object from the ultrasonic sensor in two devices. How it works is the Ultrasonic sensor locates the distance of an object from itself, and through the code, the buzzer, LED, and vibration motor would react accordingly. As an object gets closer, the components flash faster, warning the person an object is getting closer. A switch controls the buzzer and vibration motor so the user can choose between vibration and sound. The main problem I faced while making this was the code because it was unresponsive throughout the build. But I was able to learn to code better and to fix errors in code better. My next steps would be to solder all of these parts onto a perf board and begin adding on mods to my project.


# First Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/FJMfOTjolzM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

 My project is the third eye for the Blind. My first milestone was to connect and make my ultrasonic sensor work alongside my buzzer and LEDs. It works by the ultrasonic sensor sending out a wave through the Trig pin, which bounces off an object and would then be received again by the ultrasonic sensor through the Echo pin. It would then tell Arduino how far an object is based on what the ultrasonic sensor received, and through the code, the LEDs would turn on for a certain distance away from the object. Specifically, the red LED would turn on if the object was 15 or fewer cm away from the device, and the green one would turn on at any other distance in the ultrasonic sensor’s 400cm range. Additionally, the buzzer would beep a certain way if the ultrasonic sensor could sense anything signaling it was working, but it would make a long solid noise if the sensor couldn't sense anything. The main challenges I faced were the code which had many errors which caused the device not to work properly, and the breadboards which sometimes did not have good connections, which made some parts not correct with the Arduino. From this, I learned how to troubleshoot a lot better for the next part of my project, which would be to make the buzzer buzz louder when getting closer to an object,  start implementing the other features of my project like my vibration motors to do the smae thing as the buzzer and a switch to control the buzzer and vibration, and to begin duplicating it on another breadboard.


<!--iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe!-->
# Starter Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/XJPtsFAbf1M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My starter project was TV-B-Gone. All the parts were soldered onto a perf board which was powered by two double AA batteries. All the code the device needed to work was stored in a microcontroller. The way the project worked was first a button would be clicked, that would let the microcontroller know that it had to tell the transistors, which control the IR LED lights, to turn the LEDs on. Then the IR lights in the front of the device would flash in different ways because TVs turn off to different signals, so to be able to turn off any TV the IR lights would have to flash in different ways. This would be indicated by a smaller LED in the back of the device. I enjoyed learning how to solder components to the perf board and learning what each part does. Something I struggled with while building was soldering the small parts because of the precision required and finding the problem with certain parts.




# Schematics 

<img src="https://github.com/arnavb231/arnavb_BSE_Portfolio/assets/114638407/e9cb2f57-a15c-4b7a-9d89-b5c5cdd78cff" width="70%" height="70%">

<!---Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser.-->

# Code

```c++
  const int pingTrigPin = 13; //Trigger connected to PIN 12  
  const int pingEchoPin = 14; //Echo connected to PIN 10  
  #define led 6
  int buzz = 3; //Buzzer to PIN 3
  int vMotor = 4; //Vibration Motor to PIN 4 
  void setup() {   
  Serial.begin(9600);   
  pinMode(buzz, OUTPUT); 
  pinMode(vMotor, OUTPUT); 
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
  tone(vMotor, LOW);
  delay(d);
  noTone(vMotor);
  delay(d);
  tone(vMotor, HIGH); 
  digitalWrite(led, LOW);
  delay(d/2);
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

<!---#random
# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs.>

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|-->

<!---# Other Resources/Examples-->
<!---One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.-->
