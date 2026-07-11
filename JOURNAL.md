title: Posture-Tracker 

author: Tomer! 

description: A posture tracker that alerts users with a vibration when posture gets bad 

created_at: 06/25/2026

## This is in addition to the timelapse logs :)

## June 25/26
In these days I began the project by brainstorming what I want it to actualy be, what constraints and requirenments I have, etc. In order to fully flesh out the idea and prepare for coming days.
Some issues I ran into:

-picking a name (this was the hardest part, evident by the fact that I landed on "Posture-Tracker"

-making the README (I know, super exciting stuff)

This was difficult because I dont really use github, and I always thought you needed to use a terminal, so I spent way too much time trying to figure that out until I did it manualy on the site.

## July 5/6 ( i need to write more abt the part finding, like how I came to chose stuff)
After coming back from vacation, I began working on the BOM, keeping in mind hackclub constraints. This part was very hard as many of the parts I wanted where cheap up front, but where 40+ with shipping through 
AliExpress, so I now have to find better ways to source these parts. 

These prices are crazy, especially considering the fact that I dont expect to get too much funding for this :\. Regardless, it shouldnt be too much of an issue as these components are not very expensive, its just a matter of looking in the right places.

## July 9
After a quick break, I decided to work a bit more on the BOM, and deciding where I could get each part. 

I ended up landing on digikey and adafruit(after a long time of research) This is because I wanted to consolidate the parts vendors as much as possible, to reduce delivery fees, and I think it turned out great! Finaly, I can now get started on the schematic which I will do on KiCad!

In order to get this process started, I needed to find the footprints/symbols needed, presenting so many issuess.

1. What even is a footprint or symbol
2. how do i input them
3. What parts of mine even have footprints by default on KiCad
4. How can I find the ones that dont?

All of these questions where answered in due time however! (about 2 hours).

Great progress has been made so far, and next time I will get startted on the schematics (hopefuly accompanied by a cool timelapse and pictures oooh)

## July 10th - Schematics!!

### Goal
Today, I wanted to finalize the BOM and get everything on to the KiCad Schematic, (making sure nothing gets fried :)

### My Circuitry
Throughout this whole learning experience of creating the BOM, researching electronics, and so much more, I found it helpful to explain things so a 5 year old can understand it, so hopefully my explanation of this circuit does it justice :)

My design works by taking power from a battery, not shown on the schematic, and controlling it with a sliding switch. For a microcontroller, I used an ESP32S3. To track posture, I used an IMU, with a super long name that if you care for, you can find it as the big square at the bottom of the schematic
I also used a simple coin motor.

Ultimately, this monstrosity was formed, with those key components and a whole bunch of researching in regards to capacitors, resistors, and so much more. (Any "pause" in the timelapse was me researching what to do because I didnt want to screw it up)

### Some stuff I found along the way
I had to learn how to import footprints, and what to do when there arent any to be found.
I ended up having to  use the command prompt and a tool called easyeda2kicad to find footprints for the slide switch.

### Issues and Problems i encountered, because of course there are.
Although I found out that I had to use easyeda2kicad, I ran into problems with it. Most notably was that it didnt work lol. This had a simple fix of just adding a python -m command to the beginning of the command. Worked like a charm after that.

When doing the electrical check, I ran into a whopping 18 ERC Errors!!!
15 of these where solved simply with a cool feature that most people already know but I didnt, called the No Connect flag, which marked that I didnt use some of the pins on the XIAO and IMU. I guess they want me to use all of them :/
The last 3 occured because I did not include the battery in the schematic, so there was no power. (the battery would be connected through a cable, not soldering, so it didnt matter). I used another flag tool called the Power Flag to fix this.

Of course, there where so many more problems, but I dont want to bore anyone reading this, so just enjoy the pictures (I hope it looks cool)

### Next Time
Next up is the PCB itself, how exciting!

