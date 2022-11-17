# JMC client scripts for ArcticMUD
Welcome to Arctic and enjoy your stay.

Arctic has now been updated to use full ANSI coloring. TinTin++ and JMC are
the recommended MUD clients of choice as they support extended colours.
Instructions for using TinTin++ are available in a separate repository.

Within this package, you will find comments on what the cause is for each
highlight, trigger, and sub. Please review these messages as they will help
you along your adventure.

Within the Arctic_Aliases file, each class with spellcasting ability has
aliases already created. You should find these aliases at the very least 
somewhat intuitive and easy to work with. Become familiar with these aliases
to better hone your skills and more comfortable with your chosen class!

If you are playing a class that has the ability to 'refresh' others, there is
an auto-refresh trigger included in this package which is triggered when other
characters use the "pant" emote, but it is commented out as the action the 
trigger takes depends on your class. If you play a class that can make use of 
this trigger and you would like to have it enabled, remove the #nop comment 
from the appropriate line in the JMC_Arctic_Actions file.

# How to use  
### WARNING: If you are already using JMC, this will replace your current setup.

1. Update JMC to the latest version
   (https://github.com/konelav/jmc/releases/)
2. Unzip this file pack to your default JMC folder
3. Open two copies of the JMC client
4. In your alternate character's window, type "#read JMC_Win2.txt" and press
   enter
5. In your primary character's window, type "#read JMC_Win1.txt" and press
   enter
6. Create your character or log in to a character you've already created

The latest versions of JMC can regularly be found at:
https://github.com/konelav/jmc/releases. 

Please complete the following steps on your first time login to JMC. It will
make your experience more enjoyable.

1) Open JMC
2) Click Options
3) Click Scroll Buffer
4) Set the value to 30000
5) Press OK

1) Click Options
2) Click Setup
3) Click off "Clean Input" in the bottom right quadrant
4) Click on "Autoreconnect"
5) Close JMC

# How to control both characters from your first window
With the setup provided, you're able to control both windows by typing in one.
There are three different scenarios in which you can input commands.
These are:
   1) Type normal text or a command
      - This will send the command to your first window
   2) Start your command with "t" (not including the quotation marks)
      - This will send the command to your second window
   3) Start your command with "f" (not including the quotation marks)
      - This will send the commands to both windows

Examples:
```
say Hello sir!
Window says "Hello sir!"
```

```
t say How are you today?
Window 2 says "How are you today?"
```

```
f say I'm doing fine, thanks.
Window 1 AND Window 2 say "I'm doing fine, thanks."
```

# Creating your own triggers, aliases, highlights, and substitutions

SYNTAX:
|Alias|#alias  {keyword} {output text}|
|-----|-------------------------------|
|Example|#alias  {mm} {cast 'magic missile'}|

|Trigger|#action {line to trigger} {what you want to do}|
|-------|-----------------------------------------------|
|Example|#action {^There were %0 coins.}  {get all.coins corpse}|

|Substitutions|#sub {line to substitute} {replacement message}|
|-------------|-----------------------------------------------|
|Example|#sub {You eat some bread} {You eat some gnome.}|

|Highlights|#highlight {color} {Line to highlight}|
|----------|--------------------------------------|
|Example|#highlight {cyan} {You have been blinded! %1}|

If there are aliases, triggers, substitutions, or highlights you do NOT
want to keep, whether they're your own, or those included in this package,
you can use #unalias, #unaction, #unsub, and #unhighlight respectively.
Alternatively, you can use your mouse to click into "Edit JMC Objects"
in the menu bar and remove them manually.


Ensure you click the save icon in the top left of your window after making
changes.

If you already have a text file with subs you would like to import:
1) Place the file in your JMC folder
2) Enter: #read FILENAME
