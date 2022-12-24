<p align="center">
  <img width="70%" alt="Happy Station" src="https://user-images.githubusercontent.com/4536448/209449386-b2f83e8b-0001-45ac-b1be-aec7ee83cb32.jpg">
</p>

# X4 Foundations: Happy Station
This extension for X4 Foundations will detect when a player-owned station falls below its production budget, and automatically transfer funds from the player's account in order to keep the production budget at or above its recommended minimum.

I know some people like to build mega-stations (and this extension will work for those as well), but I created this for the way I play the game; construct small "feeder" stations whose output goods are only allowed to go to my other stations as inputs.  In that configuration, "feeders" can easily run short of funds and need fairly frequent attention.

## Information is power
As funds are transferred, the player will be notified, both in the log book and via a "ticker" notification, that funds were transferred, how much, to which station, and what that station's current balance is.

![20221224115338_1](https://user-images.githubusercontent.com/4536448/209448816-b7f3bc54-96ab-4f27-bfb3-7eccf85e03fe.png)

## Grants
Each station that falls behind its production budget will be given a "grant" from the player's funds.  This grant is first calculated to be twice the current deficit--in other words, if a station's minimum production budget is 1,000,000 credits, and it now finds itself with only 982,000, the extension will first try to provide it with 36,000 credits (18,000 deficit x 2).

However, if the player's account lacks that amount, it will then try just the deficit amount itself (18,000 credits) in order to bring the station back to the break-even point.

Lastly, if the player is having to molest passing gate traffic for handouts, the extension will fall back to displaying the vanilia "Insufficient funds" nag notifications while factory workers slowly starve to death.

## TODO
I tried to figure out how to allow players to configure an extension, but Egosoft's mod documentation is kind of crappy and lacks cohesion.  It appears to be a collection of loosely related subjects thrown together on a reference web site.  Seems you're largely expected to learn from the unpacked game files.

If I end up understanding how to do it (if it can be done at all), I will update the extension to allow the player to configure settings via a UI.

## Installing
You can do a git clone of this repo into a folder called "HappyStation" in your game's local `extensions` folder, or you can simply extract the provided release into the same location (it's already bundled in its target folder).
