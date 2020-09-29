# Group-2-Project-Tic-Tac-Toe

Multiplayer Tic Tac Toe

Create a multiplayer, client-server Tic Tac Toe game.

Client

The client will be a simple JavaFx program with a user input textbox and a data received output textarea
or command line program. It will know nothing about the game but merely:

1. Send a String message to the server from the user input textbox.
2. Receive a String message from the server and display in the textarea.

You may create two clients with different class names, such as Player1 and Player2, just for testing in the
IDE, but all the code, other than the name, should be the same in both.

Game

Create a TicTacToe class to be used by the server. All game rules should be handled inside this class.

Server

The server will be a JavaFx program with a simple textarea to display communication with the various
clients` or a command line program. It should be multithreaded, but limit connected clients to two
players at a time.

Use a shared instance of the TicTacToe class to manage the game once started. The server should know
nothing about game rules other than how to interpret results, such as knowing if the game should
continue or is complete.

The server should record users and game results in an Access database.

Upon connection by a client, ask for a username, then lookup the user in the database. If not found, add
them to the user list and create a unique int ID. (This should be the primary key.) If found tell them
their won/loss game history.

Wait until a second client connects. If communication comes from a client when only one is connected,
respond that you’re waiting on a second player. When two clients are connected, start the game.

Pick one of the two clients at random to be X and the other is O. X goes first.

When it is a player’s turn, ask them to give you their move in the form of row comma column (row,
column). Enter the move in the TicTacToe class. If a valid move, display the board to both clients. If not
valid, display the error message to the player who made the move and wait for them to provide a new
move.

Once a player has a valid move, let the other player know it is their turn. If the first player “interrupts”,
respond that it is not yet their turn.

Repeat getting moves from the alternating players until the game is over as a win or tie, then display the
results to both.

You may display the board as text, such as  X * X
                                            O O *
                                            X O X
where * means open space.

Database

The database will be an Access database with at least two tables, one to store usernames, and one to
store game information, such as date, usernames of the two users, and the results. The two tables
should have a relation based on the primary key of the user table.

Name the database TicTacToe.accdb and store it at C:\Data\Test
