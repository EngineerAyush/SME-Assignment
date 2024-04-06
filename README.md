# SME-Assignment

Project Setup (20 minutes)

Successfully installed Visual Studio Community 2022.
Configured SFML headers and library by copying the header and lib folders from the SFML zip file to the designated sfml folder within your project directory.
Opened and ran the .sln file in Visual Studio, encountering two deliberate errors as expected.


Error Resolution (2 hours)

Missing Semicolon: In the PlayerController.h file, there was a typo where a semicolon was missing. Easy fix! Just add a semicolon where it belongs.
Missing Friends: The error message also mentioned some unexpected tokens. Turns out, the code was missing instructions on where to find some important files (like PlayerView.h and PlayerModel.h). We added them using #include statements, like calling in backup from friendly spaceships.
The Missing Blaster: This one took a bit longer to track down. While checking things out, I noticed there wasn't an executable file (the .exe file that actually runs the game) in the x64/debug folder. This could be another clue for why things weren't working quite right. Even after carefully following the setup steps, the executable file might be missing. Here's the key: Double-check your Visual Studio 
configuration to ensure it's set to build an executable file. Without this file, you won't be able to copy the required DLL files.

Adding Weaponry (1 hour)

Now that everything's shipshape, let's give our player some serious firepower!

Fire at Will!: In the PlayerController.cpp file, I found a function called processPlayerInput() that seemed perfect for handling player firing. I uncommented it and added a new function called processBulletFire() to make those bullets fly.
Unique Arsenals: Each of our spaceships has their own special weapon:
Subzero: This icy warrior can unleash a freezing frost beam with the fireFrostBeam() function. Brrr!
ThunderSnake: This heavy hitter packs a punch with its fireTorpedoes function, launching powerful torpedoes that can even destroy bunkers!
Zapper: This agile ship deploys heat-seeking missiles with the fireLockedMissiles() function that track down the player wherever they go!
