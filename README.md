# nation-war-game
GA-SEI-CC-5 JavaScript Video Game

https://combatd.github.io/nation-war-game/

HTML5
CSS3
JavaScript
jQuery
Bootstrap

## Things to do

- Build Player class and Game object.
- Build basic constructors, attack methods, build methods
- Gather image(s) and coordinate numbers for area and map
- Test if onClick functions will work on hot spots.
- Make onClick methods call attack functions.
- Switch activity between players correctly after each player attacks.

### User Stories
- The game gives an alert which starts the game.
- Two players can play the game, clicking buttons to interact.
- Buttons will send infantry, aircraft, missile attacks to certain cities.
- Buttons can build more infantry, aircraft, and missiles to continue attacks.
- If no infantry/aircraft/missiles are left, the player receives an alert stating that they have none left.
- Once both players make a move, a turn is iterated. It does not matter the player order.
- Even on last turn where one player has no population, they are still allowed to continue attacking. This allows for a possible tie where a "Mutually Assured Destruction" has occurred. The end is when all cities are gone and all attacks are exhausted.

### Class Player 
```
constructor {
    this.cityOne = 100; 
    this.cityTwo = 75; 
    this.cityThree: 50;
    this.infantry = 3;
    this.aircaft = 1;
    this.missles = 0;
}
```

On the DOM, the attack method will need to somehow allow the player to select an attack, and the click will grab a target.

```
attackInfantry(target) {
    * We will use a Math.random() and Math.floor() to initiate an attack value that has a maximum of 5.
    * This method will also decrement (-1) this.infantry
}
```

```
attackAircraft(target) {
    * We will use a Math.random() and Math.floor() to initiate an attack value that has a maximum of 10.
    * This method will also decrement (-1) this.aircraft
}
```

```
attackMissiles(target) {
    * We will use a Math.random() and Math.floor() to initiate an attack value that has a maximum of 20
    * This method will also decrement (-1) this.missiles
}
```

```
buildInfantry() {
    * Player is able to build between 3 to 10 infantry
}
```

```
buildAircraft() {
    * Player is able to build between 3 to 5 aircraft
}
```
```
buildMissiles() {
    * player is able to build between 1 to 3 missiles
}
```

## game object
```
isGameOver() {
    * We must check if the game has ended on each and every turn.
    * This method will need to run on each turn.
    * if Player 1 and Player 2 cities drop to 0, the game is now ended.
    * An alert or modal should appear on screen to let the players know that the game is now over.
    * All setInterval() related methods should no longer initiate.
}
```
```
addAttack() {
    * We must give players more uses of infantry, aircraft, and missiles.
    * Perhaps infantry, aircraft, and missiles can regenerate at different rates. 
}
```
