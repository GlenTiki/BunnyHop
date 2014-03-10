Glen Keane 20057974
My bunny hop contains all features from the practical.
I have implemented 3 addition gameplay features:
Additional levels.
Ability to get more lives.
Time limit for a level.

Additional levels - I made so you can place a new level in the levels
folder and then its file path must be added in the constants, it must
be initialised in the WorldController.initLvl() method as the first
and second level are, and the NUM_LEVELS in the Constants must be updated.

Ability to get more lives - I made it so wherever there is a (0, 255, 255)
pixel on the level map, it renders a carrot, which must be collected to
increase your current amount of lives.

Time limit for a level - I made it so whenever a level is loaded, a level
timelimit is initialised, and this counts down until zero, at which point,
a life is lost and the level must be restarted. If the goal has been 
collected, the timer stops counting down. I also display the timer to the
player, so they can see the time they have left.

I considered adding the feature of a coin limit per level,but I thought
it didn't fit the feel of the game well. However, to implement this 
feature, it would simply be 2 int fields in the WorldController, 
curCoinsCollected && curLvlCoins. With those implemented I would initialise 
the curLvlCoins to be whatever I wanted for the level in the initLvl() 
method, and I would increment curCoinsCollected by 1 per coin collected, 
and not render the goal item in the worldRenderer unless 
curCoinsCollected == curLvlCoins.
