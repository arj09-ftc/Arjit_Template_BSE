Gesture Controlled Robot
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Arjit S | Issaquah Highschool | Electrical Engineering | Incoming Sophomore

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight: (BLUETOOTH MODULE)

In this milestone, I decided that there were two main components I wanted to complete for it: the gesture component and the BlueTooth module pairing. Arguably, the BlueTooth module pairing is the most significant, as it is a huge part in the communication between the gesture component and the robot. To create the gesture control portion, I wired up all the components together to make them work. Once I plugged in the batteries, I knew that my wiring was successful because of the red glow of the LED's. Now, this is where the complicated stuff came into place. BlueTooth wiring. First, I had to correctly wire the BlueTooth modules (Specifically RX and TX pins --- related to transmission and receival of digital signals) to the Arduino Nano and Uno, forcing me to change my wiring. I struggled to fit my fingers through the gaps of all my other wiring, shoving Ohms resistors into the correct pins to have a good voltage for the BlueTooth module. I even had to demolish my gesture component and move it to a longer breadboard, since the one I wanted to use it on was too tiny to fit the correct wiring for the BlueTooth module. After getting the base wiring complete, I needed to figure out why my BlueTooth modules weren't remaining in AT command mode, which was essential to move forward with my pairing. It turns out, however, I needed to adjust my wiring of the BlueTooth module connected to my Arduino Uno, because the ground voltage for the power module and the Uno were actually slightly different, creating discrepancies in power that was received. Once I made that fix, the BlueTooth module started flashing properly, signaling a correct connection. After confirming correct wiring and code, I managed to synthesize a proper connection between the modules, confirming it with the simple message "hi" displaying in the opposite Serial Monitor! For my final milestone, I really want to complete my code and modifications, since they are the last remaining steps for me to take before I can truly call this project complete.

- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="879" height="494" src="https://www.youtube.com/embed/O0JBTSoajUw" title="Arjit S Milestone 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:

As I started trying to comprehend the massive project I chose, I decided to set my first milestone to something simple: build my robot. I gathered up the courage to lift open the lid to the medium size box, revealing the chassis just waiting for me to assemble it. I grabbed the two bases and poured out all the shafts, screws and wheels. It seemed so simple, yet it took me almost 2 hours just to assemble it. I started by first getting the motors on, but after I did that, I realized I used the wrong motors. They didn't have wires that I could connect to my motor drivers. I disassembled the pieces holding the motors one by one, glad my teacher helped me catch this mistake before I essentially closed off that area of the chassis. Another small issue I faced after the motor disaster was the 2nd base of the chassis. I put it the wrong way, almost cracking the plastic, before realizing that I had it flipped. I noticed this because I saw 4 holes on the left side, whereas there were 3 on the right, signs that suggested the correct way to assemble it. After getting over the kinks, I started placing my Arduino Uno, breadboards, and motor drivers, using my past experiences with wiring in FTC Robotics to avoid poor wire management. After getting the Arduino set up, I decided to tackle the task of wiring the BlueTooth module and the motor drivers. After much trial and error of moving around components for ease of mind, I decided on a layout that placed the Arduino and breadboard on opposite sides, while the motor drivers stayed on the sides. After wiring up everything, I ran the code and saw that my wiring had been successful in moving the motors! I decided that the next logical step for me would be to start building the gesture component and managing the BlueTooth connections between modules.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
