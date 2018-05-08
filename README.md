# AR-Project-IoT
An Internet-of-things game that mimics the Star Wars Universe, by modeling invisible light sabers and visors. Topics include: Localization, Speech Recognition and Motion Classification.

## Understanding Game Play
1. Two Player Game (D. Vader (Red) and Luke (?) (Blue))
2. Each Player equipped with 
    1. 1 IMU (Edison) with custom-designed sabre hilts (C)
    2. 1 VISOR (Edison) with WebCam AND LED Strip attached and configured (Python)
3. Quick Actions performed by either player (asynchronously) involving Stabbing, Blocking and other more complex motions
4. *AIM: To avoid losing by preserving health... beat your opponent over 5 rounds of increasing difficulty in a duel*

![](https://github.com/pholur/AR-Project-IoT/blob/master/Images/GamePlayScreenShot.png)

## How The Game Works
1. Each player exerts an action on the sabre hilt (IMU) and the Edison relays the classified action to server. (Yoda?)
2. VISOR determines if the opponent is within HIT-RANGE (observes the glowing LEDs)
3. MIC on VISOR also catches the voice commands intended to increase or decrease health points per player during a level.
4. Server receives these signals and has designed game states to determine the health and level (Status) of either player at any point during game play.
5. We use WiFi to communicate with Server (TCP-IP) (C).

![](https://github.com/pholur/AR-Project-IoT/blob/master/Images/TrainingScreenShot.png)

## The Training Phase
1. To train the duellists, the feedback-based training module is built separately on UNITY (acting as a separate server)
2. The UNITY server classifies mis-actions to train the players to play the game within the scope of the rules.

Details about specifics in design can be understood in the comments in the code (or post an issue).
