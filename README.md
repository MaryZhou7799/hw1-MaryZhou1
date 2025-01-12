[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

UI
    Seeds remaining (start with 5): 
        - Reduces by one when player plants
        - Attribute: text
    Seeds planted (start with 0)
        - Increases by one when player plants
        - Attribute: text
Player
    - Moving
    - Planting (this affects the UI and creates plants) (Cannot plant when seeds remaining is zero)
    - Attribute: sprite
Plants
    - A new plant appears on player's location when player plants
    - Attribute: sprite


TEST

## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


First, I played the example game and analyzed its components by breaking it down into UI, player, and plants. 
I started from the player object, which has a sprite renderer and a script with a class called Player. In the script, I wrote code that handles the movement of the player, which achieves the moving of player in my break-down. 
Then I moved to the planting of the player, the main gameplay that connects player, UI, and plants. I first created a plant prefab with a sprite and assigned it as player's plant prefab. According to my break-down, the plant should appear on player's location when player plants. To achieve that, in PlantSeed function, I use the Instantiate method to create a new plant object on player's transform and rotation. The PlantSeed function is called when the player presses space.
The final step is to update the UI. From my observation, UI includes seeds remaining and seeds planted, both have the text attribute. I put them under an empty object called PlantCountUI in unity, which has the PlantCountUI script. In the script, the PlantCountUI class has a method called UpdateSeeds, which can update both seed counts based on the input arguments. Back to the player script, in the Start function, I assigned the two seeds variables to their default value as my break-down writes and called the UpdateSeeds function. In the PlantSeed function, I increase seeds planted and decrease seeds left both by one, and call the UpdateSeeds. Finally, I put an if statement at the start of PlantSeed, so nothing happened when no seeds left.



## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
