# Installation
1. Go to releases and download the most recent version from this github repo.
2. Download Concorde TSP solver, this will be used for finding the optimal path.
   - [Direct Download for Windows Users](https://www.math.uwaterloo.ca/tsp/concorde/downloads/codes/win/concorde1.1.exe)
   - [Alternative Downloads](https://www.math.uwaterloo.ca/tsp/concorde/downloads/downloads.htm)

# Usage
1. Run the exe found after unzipping the most recent release from this repo. 
2. It will ask you to first input a stronghold in each ring. Once that is done it will calculate an approximate location of all the other strongholds in each ring. From here the program will create a `stronghold.qs` file. 
3. You will open this file with the Concorde TSP solver you downloaded earlier and then hit the solve tab at the top and use the default solving parameters. 
4. Once it is done solving, hit save on Concorde.
5. Hit enter within the exe to tell it you are done solving in Concorde and have saved. 
6. The exe will now start displaying coordinates to build nether portals to find strongholds, and will follow the optimal path made by Concorde. Every time you complete a stronghold you can hit enter to progress to the next one. 

## Alternative Commands
(These commands can only be used after finding the first stronghold in each ring)
- `h`: displays a list of all the commands
- `0`: marks that there was no stronghold in the point you visited. This command should be used when you find the empty sector in the 8th ring.
- `d`: tells the program you forgot to set your spawn and will restart the pathfinding from 0 0. You will need to reopen the `.qs` file in Concorde (make sure you hit "New" then "Open", don't immediately hit "Open") and solve it again using the same method you used earlier.
- `d*`: does same thing as `d` except you can use coordinates anywhere in the world.
- `e`: allows you to edit the number of strongholds you've completed. This will only affect the counter and not the visualization of all the strongholds.

## OBS Setup
The program will generate 3 different files you can display on your stream. You can use text capture and image capture to display them on stream.

![image](https://user-images.githubusercontent.com/80478795/149217848-c62b779f-2208-4ead-9bfe-c19b7322c4c1.png)

### sh_count.txt
This is a basic text file that says how many strongholds you have completed out of 128.

### fun_facts.txt
This text file will show random facts about the numbers. Such as number is prime or 69 nice. Very silly.

### output.png
A picture of all the strongholds you've visited. Blue lines and dots indicate the stronghold you are going to, green is strongholds you have already gone to, and grey are ones you have not gone to yet.
Note: there is an OBS bug where sometimes the image will disappear when updated. This will naturally fix itself once you finish the next stronghold as the image will update again. You can also go into OBS and refresh the source by reselecting the png file.

