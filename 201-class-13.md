# Class 13 Reading Notes

### Article: "The Past, Present, and Future of Local Storage for Web Applications"

#### Diving In

Persistent local storage is one of the areas where native client applications have held an advantage over web applications. Historically, web applications have had none of the luxuiries enjoyed by local storage systems. Cookies were invented early in the web's history, and they can be used for persistent local storage of small amounts of data. But Cookies also have three potentially dealbreaking downsides:

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
- Cookies are limited to about 4 KB of data - enough to slow down your application, but not enough to be terribly useful

What we really want is
- a lot of storage space
- on the client
- that persists beyond a page refresh
- and isn't transmitted to the server


#### Introducing HTML5 Storage

HTML5 Storage is a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, and etc.. Unlike cookies however, this data is never transmitted to a remote web server.

The latest version of pretty much every browser supports HTML5 Storage: IE 8.0+, Firefor 3.5+, Safari 4.0+, Chrome 4.0+, Opera 10.5+, iPhone 2.0+ and Android 2.0+

From JavaScript, you access HTML5 Storage through the `localStorage` object on the global window object.

```function supports_html5_storage(){
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}```

Instead of writing this function yourself, you can use Modernizr to detect support for HTML Storage.

```if (Modernizr.localStorage){
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party
}```


#### Using HTML5 Storage

HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retreiving anything other than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected JavaScript datatype.


#### Limitations in current browsers

"5 megabytes" is how much storage space each origin gets by default. "QUOTA_EXCEEDED_ERR" is the exception that will get thrown if you exceed your storage quota of 5 megabytes. "No" is the answer to the next obvious question, "Can I ask the user for more storage space?"


#### HTML5 Storage in Action

With HTML5 we can save game progress locally, within the browser itself. If your browser supports HTML5 Storage, a live demonstration should magically remember your exact position within a game, including the number of moves you made, the position of each of the pieces on a board, or even whether a particular piece is selected.

How does it work? Every time a change occurs within the game, we call this function:

```function saveGameState() {
  if (!supportsLocalStorage()) {return false; }
  localStorage["halma.game.in.progress"] = gGameInProgress;
  for (var i = 0; i < kNumPieces; i++) {
    localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
    localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
  }
  localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
  localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
  localStorage["halma.movecount"] = gMoveCount;
  return true;
}```

On page load, instead of automatically calling a `newGame()` function that would reset these variables to hard-coded values, we call a `resumeGame()` function instead. Using HTML5 Storage, the `resumeGame()` function checks whether a state about a game-in-progress is stored locally. If so, it restores those values using the `localStorage` object.

```function resumeGame() {
  if (!supportsLocalStorage()) { return false; }
  gGameInProgress = (localStorage["halma.game.in.progress"]) == "true");
  if (!gGameInProgress) { return false; }
  gPieces = new Array(kNumPieces);
  for (var i = 0; kNumPieces; i++) {
    var row = parseInt(localStorage["halma.piece." + i + ".row"]);
    var column = parseInt(localStorage["halma.piece." + i + ".column"]);
    gPieces[i] = new Cell(row, column);
  }
  gNumPieces = kNumPieces;
  gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
  gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
  gMoveCount = parseInt(localStorage["halma.movecount"]);
  drawBoard();
  return true;
}```

*Data is stored as strings. If you are storing something other than a string, you'll need to coerce it yourself when you retrieve it.*