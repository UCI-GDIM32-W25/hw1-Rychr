[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity
Game world objects:
- Bunny/player
   -  Movement with WASD
   -  Plant seeds, can’t plant seeds if no more are left, updates UI to reflect seeds left and 
      how many are planted
- Seeds/plants
   -  Planted by player
- Seed amount and seeds planted UI
   -  Updated to reflect how many seeds the player can plant that are left, and how many        
       are planted

How these objects are acted on or affect each other:
- The player can plant seeds, which affects the UI by updating how many seeds are planted and how many are left.

## Devlog
The first part of the HW1 breakdown plan that I did in class mentions WASD movement for the player. This is exactly what I coded in using if statements with GetKey in the update
method to constantly check if the player was holding down WASD and transform the players position in the corresponding direction with the _speed given to me. The plan then says that
the player can plant seeds when space is pressed, which updates the UI count to reflect remaining seeds and how many seeds are planted. The player also cannot plant seeds when there 
are 0 seeds remaining. To code this, I first made another if statement in the update method but instead of using GetKey, I used GetKeyDown to make sure that space is only recognized
once until it is lifted up again. I then called the PlantSeed() method in that if statement. I created a prefab with a plant sprite in unity, and called Instantiate in the PlantSeed()
method on the plant prefab while also adding the players coordinates at the end so it always spawns on the player. I then also updated the seeds remaining and seeds planted count,
then called the UpdateSeeds() method in the plantUI script to update the text on screen. The plan then says the seeds can be planted by the player, which was gone over previously
where I stated how I coded the plants to instantiate on the player. The plan now says that the UI needs to update the text on screen. I first began by adding the UI script to the
canvas in unity as a component, and attaching that canvas component to the player script. In the UpdateSeeds() method, I simply wrote two lines that would update the number on the
text displaying on the UI to reflect the remaining seeds and planted seeds count that is indicated in the player script.

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites

## Prof comments
Thank you for making the connection between your plan and your code clear!

Next time, please put your HW break-down activity in the Devlog itself instead of just linking the Google doc. Also, consider formatting your break-down activities with the hyphen '-' symbol as suggested above, and remove the prompt text. This will make it a lot easier for me to read. See the [README formatting guide here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
