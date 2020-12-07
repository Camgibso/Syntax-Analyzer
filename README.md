This project is for Concepts of Programming Languages CS3361
This project makes use of multiprocessing and other concepts we learned in class.
I am running the larger jobs on the High Performance Computing Center(HPCC) at Texas Tech University, in the Quanah cluster. Throughout this project, apart from the main goal of the project, I have learned to use Quanah, as well as request jobs by creating my own testing shell scripts.

How to run:
python CellSimulator.py

Description
The cell simulation will go through 100 steps, and during each step, each cell is evaluated against its neighbors to determine if the cell is alive or dead.

Cell States:
Dead:   .
Alive:   O
 

Cell Neighbors:
C is the current cell
X are the neighboring cells

    XXX
    XCX
    XXX
 

Determining Factors:
 Alive cell stays alive if:
	Has 2 - 4 alive neighbors
 Dead cell becomes alive if:
	Has an positive non-zero even number of alive neighbors
Otherwise:
	The cell dies
 

Example:

Starting Colony:
    ........O..OO...O.................O.OO...
    ..O............O..O.O..OO...............
    .......O.......O.....O...........O...OO.
    ....O..O.........O......O.............O.
    ........O.....O.O......O.......O........
    .......O.....O..........................
    .O...........O............O.......OO.O..
    ..O....O...O....OO......................
    .O.O...........O................O.......    
    O..........O.........O.............O....
    ......O........O.......O..........O.....
    ..OO..............O.........O...O.O...O.
    .....OO.O..O.O.....O.O..................
    O........O....OO.....O.....OO.O.........
    O............O............O..O......O...
    ...OO.......O...............O.........O.
    O.............O............O.........O..
    .........O.....O..............O...O.....
    ........................................
    .O........O...............O......O.O....


After 100 Steps:
    OOOOOOO.O..OOOO..OOO..OOOOOOOO...O...OOO
    .OO.OO.OOO.OO.OOO.OO..OOO...O.OO.OO..O..
    ....OOO..OOOOOO.......OOOO.......O...OO.
    .OOO..OO.....OO.......O.OO.O....OOOOOO..
    ..O..OOOOOO.O.OO...OOO..O.OOO..O..OO.O..
    ..O...O.O.O.O.OOO...O..OO.OO...OO...OO..
    OOO.O...OOO....OOOOOO..O.OO...OO..OOOO.O
    ..........O.OO..OO...O..OOOO.O....OOOOOO
    OOOO.O.OOOO.OOOOO.O.....O.OO..O...OOO.OO
    O..OO..OO.OOOOOO.O...OO.OOO..OO..O.O....
    OO.....OO..OOOOOOOO...O......O.OOO.OO...
    OO..OOOOOO.OOO.O.OO....O..O..OO....O.OO.
    OO.OO..O.OOOO.OOOOO...OOOOO..OO....OO..O
    .O..OO.OOO..O.O...O....OO...OO....O.O...
    O.O.O.OOO..OO..OO.O.O.O.OOOO.OO...OO...O
    .O...OOOO.OO..OO...O.OO.OOOO........O..O
    OOOOO...OO.OO.....OO..O.OO......OOOO....
    .OO.O..OO.OO.O.O.OOO....OOO.....OOOO....
    O.OOO.O...O.OOO..OOO...O.O.O....O.OOO...
    OO.OOO.O..O.OOOOO..O..OOOOOO.....O.O.O..
