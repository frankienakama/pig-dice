player constructor = score, name?
(remember to think of constructors as blueprints)

dice constructor = methods to roll,

random numbers -
  Example
  Return a random number between 1 and 6:

  Math.floor((Math.random() * 6) + 1);
  (math.floor cuts off decimals)

when click submit, if not a one, add to player.score

maybe reverse arrays to toggle between players

## global
var player1 = {score: 0}
var player2 = {score: 0}
var players = [player1, player2]

## in game logic, always act upon players[0], the player in the first spot is the "active" player
## the other one is at index 1. then to change turns, you reverse the players array
## and the old active player is now at 1 and the old inactive player is now at 0.

players[0].score += 2
players[0].score += 3
players[0].score += 5
players[0].score
10

# oh no player1 rolled a 1
players.reverse() # NOW players[0] is player2

players[0].score += 2
players[0].score += 2
players[0].score += 4
players[0].score
8

# oh no player2 rolled a 1
players.reverse() # NOW players[0] is player1 again





## EXAMPLE THING

function Player(name) {
  this.name = name;
  this.score = 0;
}

function Dice() {}

Dice.prototype.roll = function() {
  return Math.floor(Math.random() * 6) + 1;
}

var player1 = new Player("face")
var player2 = new Player("butt")
var players = [player1, player2]


# in that ther game somewheres
var d = new Dice()

d.roll()
5
d.roll()
4
d.roll()
4
d.roll()
4
d.roll()
5
d.roll()
6
d.roll()
1
d.roll()
1




players[0].name
"face"
var roll = d.roll()
2
if (roll > 1) {players[0].score += roll} else {players.reverse() }
2
var roll = d.roll()
1
if (roll > 1) {players[0].score += roll} else {players.reverse() }

Reversed!

roll
3
if (roll > 1) {players[0].score += roll} else {players.reverse() }
3
var roll = d.roll()
5
if (roll > 1) {players[0].score += roll} else {players.reverse() }
8
if (roll > 1) {players[0].score += roll} else {players.reverse() }
1

Reversed!

players.forEach(function(p) { console.log(p.name + " " + p.score) })
That'll print the names and scores
