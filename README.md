# bataille_navale
Projet de jeux bataille navale

#Algo initiale
```javascript
// ressources: https://www.freecodecamp.org/news/javascript-hash-table-associative-array-hashing-in-js/

// dimenseions 10 by 10, A to J and 1 to 10
// 4 maps is required, 2 sets of 2
// a set is compose of a map with player' ships and a map for battle and foe' ships
// personal map is where we can see our ships locations and where the foe attacked
// battle map is where we attack and display our attacks
class NavalMap {
    _tiles=new Map(); //hash => key: value ("a1":state, "a2":state, ..., "j9":state, "j10":state)
    // states possible => fogOfWar, empty, ship, destroyed 
    constructor() {
        // Init NavalMap
        // loop foreach A to J, loop foreach 1 to 10 concat and push  as key to _graph with value set at fogOfWar
    }
    displayMap() {
        // print the battlefield with different tiles depending of state
        // fogOfWar=" ", empty="X", ship="O", destroyed="%"
        //    1 2 3 4 5 6
        //  A| | | | | | |
        //  B| | |O| | |X|
        //  C| | |O| |X| |
        //  D| | |%| | | |
        //  E| | |X| | | |
        // 
    }
}
class ShipMap extends NavalMap {
    constructor(){super()}
    addShip() {
        // STARTING POINT
        // 
        // ORIENTATION
        // horizontal 1 to 10
        // vertical A to J
        // - create hash for ship coordinates
        // - - ex: B3, vertical, 3 tiles > [B3, B4, B5]
        // - - ex: E6, horizontal, 4 tiles > [E6, F6, G6, H6]
        // - if the last coordinates is out of bound, drop and retry 
        // - if one key/value is not empty with map, drop and retry
    }
}
class BattleMap extends NavalMap {
    constructor(){super()}
    launchAtt() {

    }
}


// 4 types of ships, size ranging from 2 to 5
class Vessel {
    _size;
    _position;
    constructor(size) {
        this._size=size;
    }
    setPosition(position) {
        this._position=position;
    }
}

// # Process # //
// Init game
// - prompt to set position for each ship
// - - prompt by ship'size
// - - prompt starting point and direction
// - - check for collision, if not, proceed to next ship
//
// Init bot NavalMap
// - generate randomly ships location
//
// Start game
// - prompt attack's coordinates
// - feedback on tile'state and if it's a hit check if sunk
// - refresh NavalMaps
//
// Bot's turn
// - random attack on fogOfWar tiles
// - make an algo to seek already hit ship
// - refresh NavalMaps
//
// repeat till one player no longer have ships
```
