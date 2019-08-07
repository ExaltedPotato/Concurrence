# Concurrence
A game stat tracker for a custom turn based D&amp;D inspired strategy game of mine. WPF UI, 
separate logic in core library in case I ever expand. 

VERY OPEN TO CRITICISM ON MY OVERALL DESIGN, I'M NEWISH TO SOFTWARE ENGINEERING.


This project's archetecture is going to mostly follow that of a modular monolith, desktop UI only, 
mostly consiting of basic text document IO, user interaction, and thats about it.

A few rules I have for myself with this project, is that the instal is limited to 1 file, 1 exe,
a uniform primitive-only based communication between libraries to promote clean long term change,
and finally, code that's absolute PRIMARY focus is adaptability, as there are many routs that 
the project could go and I have absolutly no idea how the games internal balancing, unit interaction,
or even definition of a "unit" or "game" will develop. 

Because of this, most classes will be 
generic, nearly abstract in nature, with the "definition" of each item being determined by discription
files in the programs folder and imported on each load. For example:

    "Units" will always have "weapons" and "upgrades." However a "unit" might also be a "weapon."
    A upgrade can change the stats of a unit its part of, or of weapons said unit holds. Upgrades
    and weapons on each unit must be hotswappable post game initialization. Weapons will always
    be able to be "used" (and change stats of the target and source unit), but upgrades may or 
    may not be "usable" depending on their discription. Weapons may hold other weapons to 
    represent a "multi-tool" function, and an upgrades purpose might be able to be also the 
    functionality, as a bypass to a units equpment restriction.
    
