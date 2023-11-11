# Envoys
## Description
This mod was relatively challenging. The goal of it was to force certain chest blocks to open a completely separate gui to normal. To do this, I had to use mixins and listeners. Upon opening the correct gui, a spin animation had to be played, giving the player a reward based off weighted chances. It also had to allow the player to be given custom items so they can spin crates remotely.


The main challenge was getting the animation to work. Changing a gui so often could cause issues, so I managed to extract the actual gui object and directly change the items inside it to make it look like it was rolling for a reward.
