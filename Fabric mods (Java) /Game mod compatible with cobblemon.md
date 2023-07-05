# Games Mod
## Description
This is a mod I made for a Minecraft Cobblemon (fabric) server. I had to learn lots of skills in the creation of this project. The games stored inside the single .jar file were Bingo, Hunts and Community Events, each of which were easily created and modifiable through json config files. Code snippets can be requested to be viewed, but as the mod was made for a closed source server, I cannot share all the code here. 

### Bingo
Bingo was initialized by a player through the command "/bingo". The command opens a customized GUI with two buttons; *Free* and *Donor* bingo. Both, when clicked, open a GUI filled with cobblemon sprites (obtained through the API). The mod got a list of pokemon names through a JSON config file, converted them to the Pokemon type through the cobblemon API then converted them to ItemStack types as sprites, compatible with the GUI.
<br />
When a player has a bingo card active and catch a pokemon on the card, it gets marked off. When they complete a row, column or diagonal, they get a reward. They get an extra reward for completing the card.

### Hunts
Hunts was similar to bingo. The player can open the GUI through "/hunts", giving them a choice between three specific pokemon they can hunt for. When they accept the hunt, the GUI changes to a single button; with the icon of the pokemon that they're hunting for. Subsequent uses of /hunts opens the second GUI. They can either cancel the hunt through the GUI or catch the correct pokemon and hand it in (also through the GUI). They are given rewards specified in config upon handing in a valid pokemon.

### Community Events
The command "/community start [name]" searches classes containing config data for a specific event specified in config. It runs the event as customized in the config json files. Administrators can specify specific pokemon species to catch (or just have any pokemon be caught), specify specific aspects such as natures, specify specific pokemon types, etc. Players can catch or kill pokemon, depending on the event, contributing to a final prize. The mod then calculates the player's top percentage and gives rewards to the top 3 players and top percentages from config (any top percentages can be specified).

## What I learnt
In this project, I had to learn about lots of things I've never had to use before. I had to become confident with 2D arrays for bingo, learn how to make modifiable GSON classes for config and concentrate on switching between threads to prevent lag. 
